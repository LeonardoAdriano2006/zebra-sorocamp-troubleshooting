As impressoras Zebra possuem diferentes parâmetros que controlam a impressão, detecção da mídia e comportamento do equipamento.

As configurações disponíveis e os caminhos para acessá-las podem variar de acordo com o modelo da impressora.

> [!IMPORTANT]  
> Antes de alterar uma configuração, verifique o valor atual. Alterações incorretas podem causar problemas de impressão, calibração ou detecção da mídia.
> Você pode [[Impressão da etiqueta de configurações|imprimir as configurações]] para depois voltar como era se necessário.

---
# ⚙️ Como alterar as configurações?

Uma mesma configuração pode ser alterada de diferentes formas, dependendo do modelo da impressora e do ambiente em que ela está sendo utilizada.

## 🖥️ Pelo painel da impressora

Quando o modelo possui painel de controle, diversas configurações podem ser alteradas diretamente na impressora.

[[Menu de configuração da impressora]]

---

## 💻 Pelo driver de impressão

Em impressoras instaladas no Windows, algumas configurações podem ser alteradas através do **ZDesigner Driver**.

[[Driver de impressão Zebra#🪟 Windows 11]]

> [!NOTE]  
> Nem todas as configurações disponíveis na impressora estão disponíveis pelo driver.

---

## 🏷️ Pelo ZPL

Comandos ZPL enviados para a impressora também podem alterar determinadas configurações.

Isso significa que uma etiqueta ou aplicação pode modificar parâmetros da impressora durante o envio de um trabalho.

[[ZPL#Por que o ZPL altera as configurações da impressora?]]

> [!WARNING]  
> Caso uma configuração seja alterada manualmente e volte ao valor anterior após uma impressão, verifique o ZPL enviado pelo sistema. O próprio código da etiqueta pode estar sobrescrevendo a configuração.

---

## 🛠️ Pelo Zebra Setup Utilities

O **Zebra Setup Utilities** permite configurar e diagnosticar impressoras Zebra através de um computador.

[[Driver de impressão Zebra#🛠️ Zebra Setup Utilities| Acessar o driver via Setup Utilities]]

---

## 🔗 Diagnóstico relacionado

Caso esteja alterando uma configuração para solucionar um problema, consulte também:

- [[Impressão desalinhada]]
    
- [[Problemas com sensor de mídia]]
    
- [[Problemas com Ribbon]]
    
- [[Impressora não imprime]]