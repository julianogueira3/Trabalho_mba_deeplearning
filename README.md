# 📊 Sistema Inteligente de Diagnóstico Educacional com IA

## 🚀 Visão Geral

Este projeto tem como objetivo analisar dados educacionais reais e gerar **diagnósticos automáticos e acionáveis** para escolas, utilizando **Inteligência Artificial (LLM)** combinada com **análise de dados estruturados**.

A solução integra:

* 📂 Dados reais (CSV - SAEB)
* 📊 Processamento com Python (Pandas)
* 🧠 Modelo de linguagem (via Hugging Face)
* 📄 Geração automática de relatórios em PDF
* 🧾 Histórico de análises

---

## 🧠 O que o projeto faz

O sistema permite:

1. Ler dados educacionais de um CSV
2. Identificar o desempenho das escolas
3. Gerar um diagnóstico automático com IA
4. Transformar problemas em ações práticas
5. Exportar relatórios em PDF
6. Armazenar histórico de análasises

---

## 📂 Estrutura do Projeto

* `CSV`: Dados educacionais dos alunos
* `Processamento`: Agrupamento por escola
* `IA`: Geração de diagnósticos com modelo LLM
* `PDF`: Exportação dos relatórios
* `Histórico`: Armazenamento das análises feitas

---

## ⚙️ Tecnologias Utilizadas

* Python
* Pandas
* Hugging Face (`InferenceClient`)
* Requests
* ReportLab (geração de PDF)
* Dotenv (tokens de API)

---

## 📊 Etapas do Projeto

### 1. Leitura dos Dados

Os dados são carregados a partir de um arquivo CSV contendo informações como:

* ID da escola
* Proficiência em língua portuguesa (SAEB)
* Indicador de alfabetização

---

### 2. Processamento dos Dados

Os dados são agrupados por escola, gerando métricas principais:

* Média de proficiência
* Taxa de alfabetização

Isso permite identificar rapidamente escolas com baixo desempenho.

---

### 3. Geração de Contexto Automático

O sistema cria um contexto baseado nos dados:

* Classifica o nível de desempenho (baixo, médio, adequado)
* Avalia a taxa de alfabetização

Exemplo:

* "Desempenho muito baixo"
* "Baixa taxa de alfabetização"

---

### 4. Integração com IA (LLM)

Utilizando o modelo:

* `Qwen/Qwen2.5-7B-Instruct`

O sistema gera um diagnóstico educacional com base em:

* Nota da escola
* Infraestrutura (input do usuário)
* Contexto educacional

📌 O modelo é instruído a:

* NÃO ser genérico
* Gerar ações práticas
* Basear-se nos dados fornecidos

---

### 5. Geração de Relatório

O sistema cria um relatório contendo:

* Diagnóstico da escola
* Problemas identificados
* Sugestões de intervenção prática

---

### 6. Exportação para PDF

Os relatórios são automaticamente salvos em PDF usando:

* ReportLab

Nome do arquivo:

```
relatorio_<id_escola>_<hora>.pdf
```

---

### 7. Histórico de Execuções

O sistema mantém um histórico em memória contendo:

* ID da escola
* Relatório gerado
* Data da análise

---

## 💻 Execução do Sistema

O sistema roda em modo interativo no terminal:

1. Lista escolas mais críticas
2. Usuário escolhe o ID
3. Informa:

   * Infraestrutura
   * Contexto local
4. Sistema gera o diagnóstico automaticamente




