Em algumas situações, a verificação de status realizada pelo **ZDesigner Driver** pode interferir na comunicação com a impressora ou impedir determinados trabalhos de impressão.

Esse procedimento pode ser utilizado como alternativa de diagnóstico quando existem problemas relacionados à comunicação ou ao processamento das impressões.

> [!NOTE]  
> Essa opção está disponível em versões/configurações específicas do **ZDesigner Driver**, como o ZDesigner v8 e v10. A disponibilidade pode variar de acordo com o modelo da impressora e a versão do driver.

## ⚙️ Procedimento

1. Abra o **Painel de Controle** do Windows.
    
2. Acesse **Exibir impressoras e dispositivos**.
    
3. Localize a impressora Zebra.
    
4. Clique com o botão direito sobre a impressora.
    
5. Selecione **Preferências de impressão**.
    
6. Localize a opção **Desabilitar Verificação de Status da Impressora**.
    
7. Marque a caixa de seleção.
    

![[Desabilitar_Verificação_Status_impressora.png]]

8. Clique em **Aplicar**.
    
9. Clique em **OK** para salvar a configuração.
    
## 🧪 Teste

Após desabilitar a verificação de status:

1. Envie novamente um trabalho de impressão.
    
2. Verifique se a impressão é realizada normalmente.
    
3. Caso o problema persista, reative a opção e continue o diagnóstico.
    

> [!WARNING]  
> Desabilitar a verificação de status pode reduzir as informações de estado que o driver recebe da impressora. Utilize essa configuração principalmente como procedimento de diagnóstico ou quando houver uma necessidade específica.

## 🔗 Procedimentos relacionados

- [[Fila de impressão travada]]
    
- [[Impressora offline no Windows]]
    
- [[Configuração do driver Zebra]]
    
- [[Teste de impressão pelo Windows]]