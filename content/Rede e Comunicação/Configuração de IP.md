A configuração de IP permite que a impressora se comunique com outros dispositivos através da rede.

Dependendo do ambiente, o endereço pode ser atribuído automaticamente por **DHCP** ou configurado manualmente como um **IP fixo/permanente**.

Esta página reúne os principais procedimentos de configuração e diagnóstico relacionados à comunicação de rede da impressora.

---

# ⚙️ Configurar o endereço IP

## 🌐 Utilizar DHCP

No modo **DHCP**, um servidor DHCP da rede é responsável por fornecer automaticamente as informações de rede para a impressora.

Esse método é útil para verificar rapidamente se a impressora consegue obter comunicação com a rede.

Dependendo do modelo, a opção de obtenção do endereço pode aparecer como **DHCP**, **Todos** ou outra nomenclatura equivalente.

Após habilitar:

1. Aguarde a impressora obter um endereço.
    
2. Verifique o IP atribuído.
    
3. Teste a comunicação com a impressora.
    

> [!NOTE]  
> Um endereço recebido por DHCP pode mudar posteriormente. Caso sistemas ou computadores dependam diretamente do IP da impressora, considere a forma como o endereço será mantido antes de utilizá-lo permanentemente.

---

## 📌 Definir um IP fixo

Caso seja necessário manter um endereço específico na impressora:

1. Verifique a faixa de endereços utilizada pela rede.
    
2. Identifique um endereço disponível.
    
3. Configure o endereço IP.
    
4. Configure a máscara de sub-rede.
    
5. Configure o gateway, quando necessário.
    
6. Salve ou aplique as configurações.
    
7. Teste a comunicação.
    

> [!WARNING]  
> Antes de configurar manualmente um endereço IP, confirme com o responsável pela rede se o endereço pode ser utilizado.
> 
> Configurar um endereço já utilizado por outro dispositivo pode gerar **conflito de IP** e problemas de comunicação.

---

# 🔧 Como alterar a configuração?

A forma de configurar o endereço IP depende do modelo e da estrutura utilizada.

### Pelo painel da impressora

Em modelos que permitem configuração de rede diretamente pelo painel:

[[Menu de configuração da impressora#🌐 Rede]]

### Pelo computador

Dependendo do modelo e da conexão disponível, ferramentas da Zebra também podem ser utilizadas para realizar configurações de rede.

[[Driver de impressão Zebra]]

---

# 🔎 Está com problemas de rede?

Se o objetivo não é configurar um novo endereço, mas solucionar um problema de comunicação, identifique o sintoma apresentado.

### ❌ Impressora não recebe um endereço IP

A impressora está conectada à rede, mas não recebe um endereço válido ou permanece sem IP.

[[Não está pegando IP]]

---

### 📡 Impressora possui IP, mas não responde

A impressora apresenta um endereço IP, porém não é possível estabelecer comunicação com ela.

[[Impressora não responde ao IP]]

---

### 🧪 Testar a comunicação

Para verificar se existe comunicação entre o computador e a impressora:

[[Teste de conexão com a impressora]]

---

### 🔌 Impressora perde a comunicação

A impressora funciona normalmente, mas perde a conexão com a rede de forma intermitente.

[[Impressora desconectando da rede]]

---

# 🖨️ Como descobrir o IP da impressora?

Dependendo do modelo, o endereço IP pode ser consultado:

- Diretamente pelo painel;
    
- Pela etiqueta de configuração;
    
- Pela etiqueta de configuração de rede;
    
- Pela interface Web;
    
- Por ferramentas de configuração da Zebra.
    

Consulte:

[[Impressão da etiqueta de configurações]]

[[Acessando a impressora via web]]

---

## 🔗 Rede e comunicação

- [[Não está pegando IP]]
    
- [[Impressora não responde ao IP]]
    
- [[Teste de conexão com a impressora]]
    
- [[Impressora desconectando da rede]]
    
- [[Acessando a impressora via web]]