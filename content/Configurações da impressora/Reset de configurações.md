# Reset de configurações

O reset de fábrica restaura as configurações da impressora para seus valores padrão.

Esse procedimento pode ser utilizado quando configurações incorretas estão causando problemas ou quando é necessário retornar a impressora ao seu estado padrão de configuração.

## 💻 Pelo ZDesigner Driver

### Driver antigo

Após abrir as configurações do **ZDesigner Driver**:

1. Acesse **Ferramentas (Tools)**.
    
2. Localize a seção **Ação (Action)**.
    
3. Selecione **Load Factory Defaults**.
    
4. Execute a ação para restaurar as configurações.
    

### Driver atualizado

Nas versões mais recentes do driver:

1. Acesse **Manutenção (Maintenance)**.
    
2. Selecione **Reset to Default Settings**.
    
3. Confirme o procedimento.
    

![[Reset_Config_Drivers.png]]

> [!DANGER]  
> **Antes de realizar um reset de fábrica, registre as configurações atuais da impressora.**
> 
> O procedimento pode restaurar diversas configurações, incluindo parâmetros de **rede**. Como consequência, a impressora pode perder o endereço IP utilizado e deixar de se comunicar com computadores ou sistemas até que a rede seja configurada novamente.
> 
> Também podem ser perdidos ajustes realizados anteriormente, como:
> 
> - Temperatura;
>     
> - Velocidade;
>     
> - Modo de impressão;
>     
> - Tipo de mídia e sensor;
>     
> - Ajustes de posicionamento;
>     
> - Configurações de rede;
>     
> - Outros parâmetros personalizados.
>     
> 
> Antes do reset, recomenda-se imprimir e guardar a configuração atual da impressora:
> 
> [[Impressão da etiqueta de configurações]]

> [!IMPORTANT]  
> Em ambientes corporativos, verifique as configurações de rede e, quando necessário, consulte o responsável pela rede antes de realizar o reset. Isso é especialmente importante em impressoras configuradas com **IP fixo**.

## Consulte também

- [[Impressão da etiqueta de configurações]]
    
- [[Configuração de IP]]
    
- [[Configurações da impressora]]
    
- [[Driver de impressão Zebra]]