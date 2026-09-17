Quando o Windows apresenta a impressora como **Offline**, significa que o sistema não está conseguindo se comunicar corretamente com o dispositivo ou que a impressora foi identificada como indisponível.

Antes de realizar alterações no driver, verifique a conexão da impressora.

---

## 🔌 Verificar conexão

### Impressora USB

Verifique:

- Se o cabo USB está conectado corretamente;
    
- Se a impressora está ligada;
    
- Se o Windows reconhece o dispositivo;
    
- Se a porta USB está funcionando;
    
- Se possível, teste outro cabo USB ou outra porta USB.
    

### Impressora de rede

Verifique:

- Se o cabo de rede está conectado;
    
- Se o indicador de rede da impressora está ativo;
    
- Se a impressora possui um endereço IP;
    
- Se o computador está conectado à mesma rede;
    
- Se o endereço IP configurado na impressora está correto.
    

Consulte:

[[Configuração de IP]]

---

## 🖨️ Verificar o estado no Windows

1. Abra **Painel de Controle → Exibir impressoras e dispositivos**.
    
2. Localize a impressora.
    
3. Verifique se ela está definida como **offline**.
    
4. Caso exista a opção **Usar impressora offline**, verifique se ela está habilitada.
    
5. Se houver trabalhos pendentes, verifique a fila de impressão.
    

---

## 🧹 Verificar a fila de impressão

Uma fila de impressão travada pode impedir novos trabalhos de serem enviados.

Verifique se existem documentos pendentes ou com erro.

Consulte:

[[Fila de impressão travada]]

---

## 🌐 Teste de comunicação

Para impressoras conectadas à rede, teste a comunicação utilizando o endereço IP da impressora:

```text
ping IP_DA_IMPRESSORA
```

Exemplo:

```text
ping 192.168.1.100
```

Se o computador não conseguir se comunicar com o endereço IP, verifique:

- [[Configuração de IP]]
    
- [[Não está pegando IP]]
    
- [[Impressora não responde ao IP]]
    

---

## 🧪 Teste de impressão

Após verificar a conexão, realize uma impressão de teste pelo Windows:

[[Teste de impressão pelo Windows]]

Se a página de teste for impressa corretamente, a comunicação entre o Windows e a impressora está funcionando.

Caso o problema aconteça somente em um determinado sistema ou aplicativo, verifique a configuração desse software.

---

## 🛠️ Caso o problema continue

Verifique:

- Driver instalado;
    
- Modelo selecionado no driver;
    
- Porta configurada;
    
- Endereço IP da porta;
    
- Fila de impressão;
    
- Conexão USB ou de rede;
    
- Estado da impressora;
    
- Configurações de firewall ou rede, quando aplicável.