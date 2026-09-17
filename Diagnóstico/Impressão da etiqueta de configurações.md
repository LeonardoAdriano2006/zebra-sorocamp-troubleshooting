A etiqueta de configurações contém informações importantes para diagnóstico e manutenção da impressora, como modelo, versão de firmware, configurações de impressão, mídia e, dependendo do modelo e da configuração de rede, informações de comunicação.

Existem diferentes formas de imprimir as configurações, dependendo do modelo da impressora.

---

## 🖨️ Impressoras móveis

Em modelos que possuem apenas um botão, normalmente o botão **Feed**:

1. Ligue a impressora e aguarde até que ela esteja pronta.
    
2. Mantenha o botão **Feed** pressionado.
    
3. Aguarde até que o indicador da impressora pisque uma vez.
    
4. Solte o botão **Feed**.
    
5. A impressora realizará a impressão das configurações.
    

---

## 🖨️ Impressoras com dois ou três botões

Em modelos que possuem os botões **Feed** e **Pause**:

1. Ligue a impressora e aguarde até que ela esteja pronta.
    
2. Mantenha os botões **Feed** e **Pause** pressionados simultaneamente.
    
3. Aguarde o início da impressão.
    
4. Solte os botões.
    

> [!NOTE]  
> O procedimento pode variar de acordo com o modelo da impressora. Consulte o manual do modelo específico caso o procedimento não funcione.

---

# 🏭 Impressoras industriais

## Modelos com painel de botões

Alguns modelos industriais possuem um painel de controle com botões físicos.

Nesses modelos, acesse:

**Menu → Tools (Ferramentas) → Printer Setup (Imprimir Config.)**

> [!NOTE]  
> Em alguns modelos, é necessário pressionar o botão **Select** e, em seguida, o botão **+** para executar a opção selecionada.

### Exemplo

1. Acesse **Tools (Ferramentas)**.
    

![[20260914_124227 1.jpg]]

2. Selecione **Printer Setup (Imprimir Config.)**.
    

![[20260914_124235.jpg]]

---

## Modelos com painel e tela

Em outros modelos de impressoras industriais, a impressão das configurações pode ser realizada diretamente pelo menu do painel.

Acesse:

**Menu → Configurações → Imprimir Config. do Sistema**

### Exemplo

![[Tela_Configuração_ZT411.png]]
![[Imprimir_Configuração_ZT411.png]]

> [!NOTE]  
> A localização e o nome das opções podem variar de acordo com o modelo e a versão do firmware.

---

# 🌐 Impressão das configurações de rede

Em alguns modelos, a impressão das configurações da impressora **não inclui as informações de rede**.

Nesses casos, existem diferentes formas de consultar essas informações.

## 1. Rede integrada à impressora

Em modelos como a **ZT411**, as informações de rede podem ser impressas separadamente.

Acesse:

**Menu → Rede → Redes → Imprimir informações de rede**

### Exemplo:
![[Tela_Configuração_ZT411.png]]
![[Imprimir_Configuração_Rede_ZT411.png]]

---

## 2. Impressora utilizando PrintServer

Quando a impressora utiliza um **PrintServer**, as configurações de rede podem estar associadas ao próprio servidor de impressão, e não diretamente à interface de rede da impressora.

### Impressão das configurações do PrintServer

1. Localize o botão de reset na parte traseira do PrintServer.
    
2. Com um objeto fino, como um palito de dente, pressione o botão.
    

![[Foto_Botão_PrintServer]]

3. No painel da impressora, em vez de utilizar **Listar Config.**, procure pela opção **Listar Todos (Print All)**.
    
4. Execute a impressão.
    

> [!NOTE]  
> A nomenclatura das opções pode variar de acordo com o modelo do PrintServer e da impressora.

---

# 🌐 Acessando o PrintServer pela Web

Quando o PrintServer está conectado à rede, suas configurações também podem ser consultadas pela interface Web da impressora/servidor de impressão.

Consulte:

[[Acessando a impressora via web]]

Na interface Web, procure pelas configurações relacionadas ao servidor de impressão e à rede, como:

- **PrintServer**
    
- **TCP/IP Configuration**
    

Nessas opções é possível visualizar e, dependendo do modelo, modificar as configurações de rede.

> [!NOTE]  
> O acesso à interface Web pode solicitar autenticação. As credenciais padrão dependem do modelo e da configuração do dispositivo. Caso a documentação do equipamento indique credenciais padrão, utilize-as; caso contrário, consulte a documentação específica do modelo.

---

# ⚠️ Exibir e modificar configuração da impressora × Configuração do servidor de impressão

Quando a impressora utiliza um **PrintServer**, é importante diferenciar as configurações da própria impressora das configurações do servidor de impressão.

Na opção **Exibir e modificar configuração da impressora**, podem aparecer configurações relacionadas à rede. Entretanto, quando a comunicação de rede é realizada por meio de um PrintServer, o endereço IP exibido nessa seção pode **não ser o endereço IP utilizado para acessar a impressora pela rede**.

Da mesma forma, alterar o endereço IP nessa seção pode não alterar o endereço IP utilizado pelo PrintServer.

Nesse cenário, as configurações de rede devem ser verificadas diretamente na seção de configuração do **PrintServer/TCP-IP**.

---

# 📡 PrintServer Zebra

Um **ZebraNet PrintServer** é um dispositivo ou acessório de conectividade que permite que determinadas impressoras Zebra sejam conectadas a uma rede.

Entre suas principais funções estão:

- **Conectividade de rede:** permite a comunicação da impressora com a rede, dependendo do modelo e da interface utilizada.
    
- **Gerenciamento de rede:** possibilita o acesso e gerenciamento remoto da impressora por meio da rede.
    
- **Configuração TCP/IP:** permite configurar parâmetros como endereço IP, máscara de sub-rede e gateway.
    
- **Monitoramento:** alguns modelos e soluções permitem acompanhar o estado da impressora remotamente.
    

### Exemplos

Alguns exemplos de servidores de impressão ZebraNet incluem:

- ZebraNet 10/100 PrintServer;
    
- ZebraNet b/g PrintServer;
    
- ZebraNet Wireless PrintServer;
    
- ZebraNet Wireless Plus;
    
- ZebraNet PrintServer II.
    

> [!NOTE]  
> Os recursos disponíveis variam conforme o modelo do PrintServer, a impressora e a versão do firmware.


### Links

[[Acessando a impressora via web]]
[[Configuração de IP]]
[[Não está pegando IP]]
