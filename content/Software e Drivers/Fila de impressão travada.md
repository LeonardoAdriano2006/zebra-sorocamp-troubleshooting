A fila de impressão do Windows armazena os trabalhos enviados para a impressora. Em alguns casos, um trabalho pode permanecer preso na fila e impedir que novos trabalhos sejam processados.

## Sintomas

- Trabalho permanece em **Imprimindo**;
    
- Trabalho permanece em **Excluindo**;
    
- Novos trabalhos não são impressos;
    
- Vários trabalhos ficam acumulados na fila;
    
- A impressora aparece como **Offline** mesmo estando conectada;
    
- A impressão volta a funcionar após limpar a fila.
    

---

## 🧹 1. Cancelar o trabalho pela fila

Antes de realizar procedimentos mais avançados, tente cancelar o trabalho diretamente pela fila de impressão.

1. Abra a fila de impressão da impressora.
    
2. Selecione o trabalho que está travado.
    
3. Clique em **Cancelar**.
    
4. Aguarde alguns segundos e verifique se o trabalho foi removido.
    

Caso o trabalho não seja removido, prossiga para a limpeza do Spooler.

---

## 🖥️ 2. Limpar a fila do Spooler

Esse procedimento limpa os trabalhos armazenados no Spooler de Impressão do Windows.

### Parar o Spooler

1. Clique em **Iniciar**.
    
2. Digite `CMD`.
    
3. Clique com o botão direito em **Prompt de Comando**.
    
4. Selecione **Executar como administrador**.
    

Execute:

```cmd
net stop spooler
```

Pressione **Enter** e aguarde a confirmação de que o serviço foi interrompido.

### Excluir os trabalhos pendentes

Execute:

```cmd
del %systemroot%\System32\spool\printers\* /Q
```

Pressione **Enter**.

Esse comando remove os arquivos de trabalhos de impressão armazenados na fila do Spooler.

### Iniciar novamente o Spooler

Execute:

```cmd
net start spooler
```

Pressione **Enter**.

Após iniciar o serviço, a fila de impressão do Windows deverá estar limpa.

Para fechar o Prompt de Comando:

```cmd
exit
```

> [!WARNING]  
> O Prompt de Comando deve ser executado como administrador para que os comandos do Spooler funcionem corretamente.

---

## 🔄 3. Alterar o modo de impressão

Caso a fila continue apresentando problemas, uma alternativa é alterar a forma como o Windows processa os trabalhos.

Acesse:

**Propriedades da impressora → Avançado**

Procure as opções relacionadas ao Spooler de Impressão.

Dependendo da configuração atual, alterne entre:

- **Usar spooler de impressão**
    
- **Imprimir diretamente na impressora**
    

### Imprimir diretamente na impressora

A opção **Imprimir diretamente na impressora** pode ser utilizada como alternativa quando existem problemas relacionados ao Spooler.

> [!NOTE]  
> Essa alteração pode ser útil para diagnóstico. Se a impressão funcionar utilizando a opção de impressão direta, o problema pode estar relacionado ao processamento do trabalho pelo Spooler.

---

## ⚠️ Erro ao alterar o Spooler

Ao tentar alterar essa configuração, o Windows pode apresentar a mensagem:

> **"Não foi possível salvar as configurações da impressora. A operação solicitada não é permitida quando há trabalhos enfileirados na impressora."**

Nesse caso:

1. Reinicie o computador.
    
2. Verifique se não existem trabalhos pendentes na fila.
    
3. Acesse novamente as **Propriedades da impressora → Avançado**.
    
4. Tente alterar a configuração novamente.
    

---

## 🏷️ 4. Desabilitar verificação de status

Em algumas situações, o problema pode estar relacionado à verificação de status realizada pelo driver **ZDesigner**.

Esse procedimento é aplicável ao **ZDesigner Driver v8/v10**, dependendo do modelo e da configuração.

Consulte:

[[Desabilitar verificação de status do ZDesigner]]

> [!NOTE]  
> A opção é destinada às impressoras de etiquetas compatíveis com o driver ZDesigner. Não deve ser aplicada indiscriminadamente a todos os modelos ou tipos de impressora.

---

## 💳 5. Impressoras de cartão

Para impressoras de cartão, existe um procedimento diferente.

Acesse:

**Preferências de impressão**

Verifique se a janela de preferências é aberta normalmente.

Se aparecer uma mensagem informando que a impressora **não está conectada**, pode ser necessário reinstalar o driver.

Os drivers podem ser encontrados no suporte oficial da Zebra:

[Drivers e downloads — Zebra](https://www.zebra.com/br/pt/support-downloads.html?utm_source=chatgpt.com)

Consulte também:

[[Instalação da impressora no Windows]]

---

## 🔎 6. Se o problema continuar

Se a fila voltar a travar mesmo após a limpeza do Spooler, verifique outras possíveis causas:

- [[Impressora offline no Windows]];
    
- [[Configuração do driver Zebra]];
    
- [[Instalação da impressora no Windows]];
    
- [[Impressora não responde ao IP|Endereço IP incorreto;]]
    
- [[Configuração de IP|Problemas de comunicação com a impressora]];
    
- [[Instalação da impressora no Windows|Driver incompatível ou corrompido;]]
    
- Problemas no sistema que está enviando a impressão.
    

Após realizar as correções, execute:

[[Teste de impressão pelo Windows]]

---

## 🧪 Diagnóstico rápido

| Situação                                            | Procedimento                                                 |
| --------------------------------------------------- | ------------------------------------------------------------ |
| Apenas um trabalho está travado                     | Cancelar o trabalho pela fila                                |
| Vários trabalhos estão presos                       | Limpar o Spooler                                             |
| A fila não pode ser limpa normalmente               | Usar os comandos do Spooler                                  |
| Problema continua utilizando o Spooler              | Testar **Imprimir diretamente na impressora**                |
| Erro ao alterar o modo do Spooler                   | Reiniciar o computador e tentar novamente                    |
| Problema com ZDesigner v8/v10                       | Verificar [[Desabilitar verificação de status do ZDesigner]] |
| Impressora de cartão informa que não está conectada | Verificar/reinstalar o driver                                |
| Impressora de rede não responde                     | [[Configuração de IP]]                                       |

## 🔗 Links úteis

https://support.zebra.com/pt-BR/article/000019722

