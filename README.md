# Solução de problemas Zebra

Documentação técnica desenvolvida para centralizar procedimentos de **configuração, manutenção e solução de problemas em impressoras Zebra**.

O conteúdo foi escrito em **Markdown utilizando o Obsidian** e publicado como um site de documentação utilizando o **Quartz**, permitindo transformar as notas em uma base de conhecimento navegável e acessível pelo navegador.

## 📌 Sobre o projeto

Este projeto surgiu com o objetivo de organizar procedimentos utilizados no diagnóstico e manutenção de impressoras Zebra em uma documentação centralizada.

A documentação reúne problemas recorrentes, procedimentos de configuração, manutenção preventiva e soluções que podem auxiliar durante atendimentos técnicos. Sempre que possível, os procedimentos são complementados com imagens, observações técnicas e referências à documentação oficial da Zebra.

---

## 🛠️ Tecnologias utilizadas

### Obsidian

Utilizado para criação e organização das notas em **Markdown**, permitindo manter a documentação de forma simples e facilmente versionável.

### Quartz

O **Quartz** é responsável por transformar os arquivos Markdown em um site estático de documentação.

Com ele é possível utilizar recursos como:

- Navegação entre notas;
- Links internos;
- Pesquisa de conteúdo;
- Organização hierárquica;
- Backlinks;
- Interface responsiva;
- Geração automática das páginas.

### Git e GitHub

Utilizados para versionamento da documentação e armazenamento do projeto.

---

## 🚀 Executando o projeto localmente

### 1. Clone o repositório

```bash
git clone <URL-DO-REPOSITORIO>
```

Entre na pasta:

```bash
cd zebra-sorocamp-troubleshooting
```

### 2. Instale as dependências

É necessário possuir o **Node.js** instalado.

Execute:

```bash
npm install
```

### 3. Execute o Quartz

Para gerar a documentação e iniciar o servidor local:

```bash
npx quartz build --serve
```

Após a compilação, o Quartz exibirá no terminal o endereço utilizado para acessar a documentação localmente.

Normalmente:

```text
http://localhost:8080
```

---

## ✏️ Adicionando novas documentações

Novos conteúdos devem ser adicionados dentro da pasta:

```text
content/
```

As páginas são escritas utilizando **Markdown (`.md`)**.

Exemplo:

```markdown
# Impressora não imprime

## Sintomas

A impressora está ligada e conectada, porém nenhum trabalho de impressão é realizado.

## Possíveis causas

- Fila de impressão travada;
- Driver incorreto;
- Porta configurada incorretamente;
- Problema de comunicação;
- Impressora pausada.

## Solução

Verifique inicialmente a comunicação com a impressora e posteriormente a fila de impressão do Windows.
```

Após salvar o arquivo, o Quartz será responsável por gerar a página correspondente.

---

## 🔗 Links internos

Como os arquivos são compatíveis com a organização utilizada no Obsidian, a documentação pode utilizar links entre diferentes procedimentos.

Exemplo:

```markdown
[[Calibração manual]]
```

Isso permite conectar problemas relacionados e criar uma base de conhecimento onde diferentes procedimentos podem ser acessados rapidamente.

---

## 📖 Referências

Parte dos procedimentos presentes nesta documentação utiliza como referência materiais técnicos e manuais oficiais disponibilizados pela **Zebra Technologies**.

As referências específicas utilizadas em cada procedimento são indicadas, quando aplicável, dentro da própria página.

> Esta documentação não substitui os manuais oficiais ou orientações fornecidas pelo fabricante.

---

## 🎯 Objetivo

O objetivo deste projeto é criar uma base de conhecimento que facilite o diagnóstico de problemas recorrentes em impressoras Zebra.

Ao centralizar procedimentos técnicos em uma documentação estruturada, torna-se mais fácil:

- Consultar soluções durante atendimentos;
- Padronizar procedimentos técnicos;
- Registrar conhecimento adquirido durante manutenções;
- Compartilhar soluções entre técnicos;
- Evitar a perda de conhecimento técnico;
- Atualizar procedimentos conforme novos problemas e soluções são identificados.

---

## 🔄 Status do projeto

🟢 **Em desenvolvimento**

A documentação continuará sendo expandida conforme novos procedimentos, problemas e soluções forem documentados.

---

## 👨‍💻 Autor

**Leonardo Adriano da Silva**

Projeto desenvolvido para organização e compartilhamento de conhecimento técnico relacionado à manutenção, configuração e troubleshooting de equipamentos Zebra.
