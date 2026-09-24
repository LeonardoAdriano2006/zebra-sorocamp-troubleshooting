As configurações de ajuste de impressão permitem **corrigir a posição da impressão na etiqueta e a posição em que a mídia para após a impressão**.

Essas opções são úteis quando a impressão está deslocada para cima, para baixo ou para os lados, ou quando a etiqueta não para corretamente na posição de destaque ou corte.

> [!NOTE]  
> Os nomes e ajustes disponíveis variam de acordo com o modelo da impressora e a versão do driver.

É possível encontrar opções como:

### ↕️ Top / Top Offset

Ajusta a posição da impressão no sentido do avanço da mídia.

Pode ser utilizado quando todo o conteúdo está sendo impresso **acima ou abaixo da posição desejada**.

---

### ↔️ Left / Left Position

Ajusta a posição da impressão lateralmente.

Pode ser utilizado quando todo o conteúdo está sendo impresso **muito para a esquerda ou para a direita** da etiqueta.

---

### 🏷️ Tear Off

Ajusta a posição em que a mídia para após a impressão no modo **Destacar (Tear Off)**.

Esse ajuste pode ser utilizado quando a linha entre as etiquetas não está posicionada corretamente na região utilizada para destacar a mídia.

> [!IMPORTANT]  
> O **Tear Off** não movimenta apenas o conteúdo impresso. Ele está relacionado à **posição de parada da mídia**.

---

### ✂️ Cut Position

Ajusta a posição da mídia em relação ao cortador.

Pode ser utilizado quando o corte está ocorrendo fora da posição desejada.

Esse ajuste é utilizado em impressoras configuradas para o modo **Cutter**.

---

### 📏 Gap/Mark Height

Está relacionado à dimensão utilizada para identificação do intervalo ou marca da mídia.

Deve corresponder às características da etiqueta utilizada para que o avanço e posicionamento ocorram corretamente.

---

## 📐 Unprintable Area

Em versões mais antigas do driver, podem existir configurações de **Unprintable Area (Área não imprimível)**:

- **Left**
    
- **Top**
    
- **Right**
    
- **Bottom**

Esses valores permitem definir áreas das extremidades da etiqueta que não serão utilizadas para impressão.

Em versões mais recentes do **ZDesigner Driver**, essas opções podem não estar disponíveis, sendo substituídas por controles individuais de posicionamento.

Por isso, dependendo da versão do driver, você pode encontrar:

**Drivers/modelos antigos:**

`Unprintable Area → Left / Top / Right / Bottom`

`Position Adjustment → Gap/Mark Height / Offset / Cut Position / Top Offset`

ou:

`Unprintable Area → Left / Top / Right / Bottom`

`Adjustment → Top / Tear Off / Left Position`

**Drivers mais recentes:**

`Offsets → Top / Left`

---

> [!IMPORTANT]  
> Antes de utilizar os ajustes de posição para corrigir uma impressão desalinhada, verifique se o **tamanho da etiqueta, tipo de mídia, sensor e calibração** estão corretos.
> 
> Os offsets devem ser utilizados para realizar ajustes de posicionamento e não para compensar uma configuração incorreta da mídia.

## Consulte também

- [[Impressão desalinhada]]
    
- [[Configuração do tamanho da etiqueta]]
    
- [[Configuração do tipo de mídia]]
    
- [[Configuração do tipo do sensor]]
    
- [[Calibração manual]]
    
- [[Configuração de modo de impressão]]