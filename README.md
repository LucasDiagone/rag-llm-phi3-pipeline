# 📘 Projeto RAG com LLM Open-Source (Phi-3)

Este repositório contém um **projeto educacional de RAG (Retrieval-Augmented Generation)** desenvolvido com o objetivo de **aprender e demonstrar conceitos iniciais de LLMs e busca semântica**, no contexto de um **aprendiz em nível júnior**.

O projeto implementa um **pipeline completo** que combina **recuperação de informação** com **geração de texto**, utilizando apenas **ferramentas open-source amplamente adotadas no mercado**.

---

## 🎯 Objetivo do Projeto

O principal objetivo deste projeto é:

- Aprender na prática o **padrão RAG**
- Entender como **LLMs podem ser combinados com dados externos**
- Explorar conceitos fundamentais como:
  - Chunking
  - Embeddings
  - Vector Stores
  - Busca semântica
  - Prompting baseado em contexto

> ⚠️ **Importante:**  
> Este projeto foi desenvolvido com foco em **aprendizado**, e não como uma solução de produção.  
> As decisões técnicas refletem um **nível inicial/júnior**, priorizando **clareza e didática**.

---

## 🧱 Arquitetura do Pipeline RAG

O fluxo implementado segue o padrão clássico de RAG:

1. 📄 Ingestão de dados (TXT local + Web)  
2. ✂️ Divisão dos textos em chunks  
3. 🧠 Geração de embeddings  
4. 🗂️ Indexação em vector store (FAISS)  
5. 🔎 Recuperação semântica dos chunks relevantes  
6. 🤖 Geração de resposta com LLM condicionada ao contexto  

Todo o pipeline está documentado passo a passo no notebook:

📓 **`Projeto_RAG_Phi3_com_comentarios.ipynb`**

---

## 📂 Fontes de Dados Utilizadas

### 📁 Documento Local (TXT)

- Arquivo: `data/politica_reembolso.txt`
- Simula um **documento interno**, como políticas, manuais ou FAQs
- O arquivo TXT está incluído no repositório para facilitar a reprodução

---

### 🌐 Conteúdo Web

Fonte externa utilizada:

- **BBC News Brasil**  
- 🔗 https://www.bbc.com/portuguese/articles/cd19vexw0y1o

O conteúdo web é carregado dinamicamente e tratado da mesma forma que o documento local dentro do pipeline RAG.

---

## 🤖 Modelos Utilizados (Hugging Face)

### 🔹 LLM — Phi-3 Mini (Instruct)

- Modelo: **microsoft/Phi-3-mini-4k-instruct**
- Link: https://huggingface.co/microsoft/Phi-3-mini-4k-instruct

Utilizado para:
- Geração final das respostas
- Prompting baseado em contexto recuperado

---

### 🔹 Modelo de Embeddings

- Modelo: **sentence-transformers/all-MiniLM-L6-v2**
- Link: https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2

Utilizado para:
- Converter chunks de texto em vetores numéricos
- Permitir busca semântica eficiente

---

## 🧰 Principais Tecnologias

- Python  
- Hugging Face Transformers  
- LangChain (community + core)  
- FAISS  
- Sentence Transformers  
- Jupyter Notebook  

---

## ▶️ Como Executar o Projeto

1. Clone o repositório  
2. Crie um ambiente virtual (opcional, mas recomendado)  
3. Instale as dependências  
4. Abra o notebook:

```bash
jupyter notebook Projeto_RAG_Phi3_com_comentarios.ipynb
