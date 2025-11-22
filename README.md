# 🎬 Recomendador de Filmes Baseado em Contexto

Este projeto é um sistema de recomendação de filmes inteligente que utiliza **Processamento de Linguagem Natural (PLN)** e **IA Generativa (Google Gemini)** para analisar o dia do usuário e sugerir filmes que correspondam à sua necessidade emocional e contexto.

## 🧠 Técnicas de PLN Utilizadas

Este projeto implementa um pipeline de PLN composto por duas técnicas principais exigidas:

1.  **Sumarização de Textos:** O sistema recebe um relato livre do usuário (muitas vezes longo e ruidoso) e o transforma em uma "Logline" (sinopse curta de cinema), extraindo apenas a essência narrativa do dia.
2.  **Análise de Sentimentos:** A partir do relato, o modelo classifica a polaridade do dia (Positivo, Negativo, Neutro, etc.) para guiar a escolha do gênero.

## 🚀 Como Funciona (Pipeline)

O fluxo de dados segue as seguintes etapas:

1.  **Input:** O usuário descreve seu dia em linguagem natural.
2.  **Processamento (LangChain + Gemini):**
    * *Agente de Sentimento:* Analisa a carga emocional do texto.
    * *Agente de Sumarização:* Condensa o texto em uma frase dramática ou cômica.
    * *Agente Recomendador:* Cruza o resumo e o sentimento para selecionar 2 gêneros cinematográficos ideais.
3.  **Filtragem por Popularidade:** O sistema consulta a API do TMDB utilizando os gêneros sugeridos e aplica filtros de qualidade (avaliação mínima) e popularidade para garantir que o        usuário receba apenas sugestões relevantes e bem avaliadas.

## 🛠️ Tecnologias Utilizadas

* **Python 3**
* **LangChain:** Para orquestração dos prompts e cadeias de pensamento da IA.
* **Google Gemini (via API):** LLM (Large Language Model) responsável pela interpretação de texto.
* **TMDB API:** Para busca de metadados reais de filmes (títulos, sinopses, avaliações).
* **Google Colab:** Ambiente de desenvolvimento.

---
*Projeto desenvolvido para a disciplina de Processamento de Linguagem Natural.*
