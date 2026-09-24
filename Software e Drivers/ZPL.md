## O que é ZPL?

A **Zebra Programming Language (ZPL/ZPL II)** é uma linguagem utilizada pelas impressoras Zebra para definir o conteúdo e o comportamento de uma impressão.

Por meio do ZPL é possível criar etiquetas contendo:

- Textos;
    
- Códigos de barras;
    
- QR Codes;
    
- Linhas e formas;
    
- Imagens;
    
- Posicionamento dos elementos;
    
- Entre outras informações.

Além do conteúdo visual da etiqueta, comandos ZPL também podem definir ou alterar **configurações da impressora**, como temperatura, velocidade, dimensões da etiqueta, método e modo de impressão.

---

# 🧱 Estrutura básica

Um formato ZPL normalmente é delimitado pelos comandos `^XA` e `^XZ`.

```zpl
^XA

...

^XZ
```

- **`^XA`** — início do formato.
    
- **`^XZ`** — fim do formato.
    

Entre esses comandos são inseridas as instruções responsáveis pela criação e impressão da etiqueta.

Por exemplo:

```zpl
^XA
^FO50,50
^A0N,40,40
^FDTeste de impressão^FS
^XZ
```

Nesse exemplo, o ZPL define a posição do campo, fonte e o texto que será impresso.

---

# ⚙️ ZPL também pode alterar configurações da impressora

Um ponto importante durante o diagnóstico é entender que o ZPL enviado para a impressora pode conter **configurações além do conteúdo da etiqueta**.

Isso significa que determinadas configurações realizadas manualmente pelo:

- Painel da impressora;
    
- Driver de impressão;
    
- Zebra Setup Utilities;
    
- Interface Web;

podem ser **sobrescritas quando o sistema enviar uma nova impressão**.

---

# 🖥️ Sistema × Impressora

Durante um diagnóstico, é importante identificar **quem está definindo a configuração utilizada na impressão**.

Imagine a seguinte situação:

1. A temperatura da impressora está configurada como **20**.
    
2. Pelo painel, você altera para **15**.
    
3. A impressora permanece configurada como **15**.
    
4. O sistema envia uma etiqueta contendo um comando que define a temperatura como **20**.
    
5. A impressora recebe o comando.
    
6. A configuração volta para **20**.
    

Nesse caso, **alterar apenas a configuração diretamente na impressora não resolve o problema**, porque o sistema continuará enviando sua própria configuração.

```text
┌──────────────────────┐
│       SISTEMA        │
│                      │
│ Temperatura: 20      │
│ Velocidade: 5        │
│ Modo: Tear Off       │
└──────────┬───────────┘
           │
           │ Envia impressão / ZPL
           ▼
┌──────────────────────┐
│      IMPRESSORA      │
│                      │
│ Configuração manual  │
│ pode ser substituída │
└──────────────────────┘
```

> [!IMPORTANT]  
> Se você alterar uma configuração pelo painel ou driver e ela **voltar para outro valor logo após uma impressão enviada pelo sistema**, verifique se o próprio sistema ou o ZPL está definindo essa configuração.

---

# 🔎 Como identificar esse comportamento?

Um teste simples pode ajudar a identificar a origem do problema:

1. Altere a configuração desejada diretamente pelo painel da impressora.
    
2. Confirme que a alteração foi aplicada.
    
3. Verifique novamente a configuração.
    
4. Envie uma etiqueta pelo sistema utilizado pela empresa.
    
5. Confira novamente a configuração da impressora.

Se a configuração mudar **após a impressão enviada pelo sistema**, existe a possibilidade de o sistema, driver utilizado por ele ou o próprio ZPL estar enviando essa configuração.

> [!NOTE]  
> A alteração após a impressão é um indício importante, mas não significa necessariamente que o ZPL seja o responsável. O sistema também pode aplicar configurações através do driver ou de outros métodos de comunicação.

---

# 🔧 Como corrigir?

A solução depende de como o sistema realiza a impressão.

## 1. O sistema possui configurações de impressão

Alguns sistemas possuem uma área própria para configurar parâmetros da impressora.

Por exemplo:

- Temperatura;
    
- Velocidade;
    
- Tamanho da etiqueta;
    
- Método de impressão;
    
- Modo de impressão;
    
- Impressora utilizada.
    

Nesse caso, realize a alteração **nas configurações do próprio sistema**, quando essa for a origem dos parâmetros enviados à impressora.

---

## 2. O sistema abre as configurações do driver

Alguns sistemas possuem um botão ou opção que abre diretamente as **Preferências de impressão** do driver instalado no computador.

Nesse caso:

1. Acesse a configuração de impressão pelo sistema.
    
2. Abra as propriedades ou preferências da impressora.
    
3. Altere a configuração desejada.
    
4. Salve as alterações.
    
5. Faça uma nova impressão pelo próprio sistema.
    

Consulte:

[[Driver de impressão Zebra]]

---

## 3. O sistema está sendo utilizado em outro computador

Em alguns ambientes, o usuário acessa remotamente outro computador ou servidor no qual o sistema está instalado.

Nesse cenário, pode ser necessário alterar o driver **no computador que efetivamente executa e envia a impressão**, e não somente no computador utilizado para acessar o sistema.

Exemplo:

```text
Seu computador
      │
      │ Acesso remoto
      ▼
Computador / Servidor
      │
      │ Sistema + Driver
      ▼
Impressora Zebra
```

Se o trabalho de impressão é gerado pelo computador remoto, verifique as configurações de impressão existentes nesse ambiente.

---

## 4. O sistema permite alterar o ZPL

Alguns sistemas permitem visualizar ou modificar diretamente o código ZPL utilizado na impressão.

Nesse caso, determinadas configurações podem ser definidas diretamente no código, como:

- Temperatura;
    
- Velocidade;
    
- Método de impressão;
    
- Modo de impressão;
    
- Dimensões da etiqueta;
    
- Entre outros parâmetros suportados.
    

> [!WARNING]  
> Alterar um ZPL utilizado em produção pode afetar todas as etiquetas geradas pelo sistema. Antes de modificar o código, verifique como o sistema utiliza esse formato e se a alteração afetará outras impressoras ou processos.

---

# 🔄 Qual configuração prevalece?

Não considere a configuração exibida no painel como a única fonte de configuração da impressão.

Dependendo da aplicação, o fluxo pode ser:

```text
Configuração da impressora
          ↓
Configuração do driver
          ↓
Configuração do sistema
          ↓
Comandos enviados na impressão
          ↓
Resultado final
```

A configuração enviada mais tarde durante o processo pode alterar parâmetros que haviam sido definidos anteriormente.

Por isso, quando uma configuração **continua voltando**, procure descobrir primeiro de onde está vindo o trabalho de impressão.

---

# 🛡️ Antes de alterar sistemas de produção

> [!IMPORTANT]  
> Antes de modificar configurações dentro de um sistema utilizado pela empresa, principalmente em ambientes de produção, entre em contato com o responsável pelo sistema ou com o setor de **TI**.
> 
> Caso seja um sistema fornecido por outra empresa, consulte o **suporte responsável pelo software** antes de modificar configurações, templates ou códigos ZPL.
> 
> Uma alteração realizada no sistema pode afetar outras impressoras, usuários ou etiquetas que utilizem a mesma configuração.

---

# 💾 Configurações persistentes

Alguns comandos podem alterar configurações que permanecem ativas na impressora após o término da etiqueta.

O ZPL também possui comandos relacionados ao armazenamento de configurações, como o `^JU`, utilizado para salvar ou restaurar configurações conforme seus parâmetros.

Por isso, ao analisar um ZPL utilizado por um sistema, verifique não apenas os comandos responsáveis pelo conteúdo visual da etiqueta, mas também comandos relacionados às configurações da impressora.

---

# 🛠️ ZPL e SGD

Nem todas as configurações disponíveis em uma impressora Zebra são controladas exclusivamente por ZPL.

Além do ZPL, equipamentos Zebra podem utilizar comandos **SGD (Set-Get-Do)** para consultar ou alterar diferentes parâmetros do equipamento.

De maneira simplificada:

- **ZPL** — utilizado principalmente para criação de etiquetas e também para diversos parâmetros relacionados à impressão;
    
- **SGD** — utilizado para consultar e configurar diversos parâmetros do equipamento.
    

Para diagnóstico, o mais importante é identificar se algum comando enviado pelo sistema está sobrescrevendo a configuração realizada manualmente.

---

# 🏷️ ZebraDesigner

O [[Zebra Designer]] pode ser utilizado para criação e teste de etiquetas.

Durante a configuração da etiqueta e da impressão, também podem ser definidos parâmetros que influenciam o comportamento da impressora.

Por isso, ao realizar testes com o ZebraDesigner, verifique as configurações utilizadas antes de enviar a etiqueta.

---

## 🔗 Procedimentos relacionados

- [[Configurações da impressora]]
    
- [[Driver de impressão Zebra]]
    
- [[Menu de configuração da impressora]]
    
- [[Configuração de temperatura]]
    
- [[Configuração de velocidade de impressão]]
    
- [[Configuração de modo de impressão]]
    
- [[Impressão da etiqueta de configurações]]