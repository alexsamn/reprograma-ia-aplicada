# S2 · Prompting como Ferramenta de Poder — Tema 4: Todos devem ter casa

**Equipe:** Leticia, Bea, Larissa Roberta, Larissa e Alexsandra Moura
**Tipo:** em grupo

## Links

- 📊 [Slides de apresentação (Google Drive)](https://drive.google.com/file/d/1VVfuL7sKiseBO60Ry7vc3osaiN_4ALT1/view?usp=sharing)

## Desafio

Usar IA para apoiar o acesso à moradia: criar um critério objetivo para **priorizar famílias em situação de vulnerabilidade habitacional** e recomendar encaminhamentos (jurídico, financeiro e urbanístico).

## Entregáveis

### 1. Teste do prompt 1 (estruturado)

Começamos com uma pergunta solta sobre moradia (situação de rua, ocupação, morar de favor, aluguel). A IA não entendeu o que fazer e pediu o objetivo. A partir daí reescrevemos o pedido com estrutura completa:

| Bloco | Conteúdo |
|-------|----------|
| **Papel** | Especialista em soluções habitacionais e planejamento urbano social |
| **Escopo** | Ranquear as pessoas em maior situação de vulnerabilidade |
| **Requisitos** | Índice de 0 a 100 em 3 dimensões e 7 critérios (tabela abaixo) |
| **Restrições** | Não gerar imagens nem áudio |
| **Formato** | Planilha Excel com nome, idade, contato e pontuação |
| **Objetivo** | Cruzar dados de território, imóveis e famílias para recomendar encaminhamento jurídico, financeiro e urbanístico |

**Índice de vulnerabilidade (0–100):**

| Dimensão | Critério | Pontos |
|----------|----------|-------:|
| Socioeconômica (até 40) | Extrema pobreza / renda per capita até ½ SM (Faixa 1 CadÚnico) | 20 |
| | Chefia familiar feminina | 10 |
| | Presença de PcD, idosos ou crianças de 0 a 6 anos | 10 |
| Inadequação e risco habitacional (até 35) | Moradia em área de risco geológico/hidrológico R3 ou R4 | 20 |
| | Coabitação excessiva ou aluguel acima de 30% da renda | 15 |
| Vínculo territorial (até 25) | Mora no entorno do imóvel mapeado (preserva a rede de apoio) | 15 |
| | Tamanho da família compatível com a tipologia do imóvel | 10 |

**O que a IA gerou:**

- **Planilha com 100 cadastros fictícios** em 3 abas:
  1. *Ranking de vulnerabilidade*: ranking, nome, idade, contato, pontuação e nível (Crítica / Alta / Média / Baixa / Mínima)
  2. *Critérios detalhados*: quais critérios cada pessoa atende, com subtotais por dimensão
  3. *Resumo e recomendações*: distribuição por nível e encaminhamentos sugeridos por faixa de pontuação
- **Consulta individual:** perguntamos a posição de uma pessoa específica no ranking e a IA respondeu com posição, pontuação e nível.
- **Apresentação de 7 slides** para o poder público: título, desafio, solução, metodologia, exemplo prático, próximos passos e um slide extra com dados de contexto.

**Dados de contexto incluídos no slide 7:**

| Indicador | Fonte |
|-----------|-------|
| 8,3 milhões de pessoas em áreas de risco | IBGE–Cemaden, Censo 2010 |
| 11 milhões de mães solo, 61% negras | PNAD/IBGE 2018 |
| 16,4 milhões de pessoas em favelas e comunidades urbanas (11,4 mi em 2010) | Censo IBGE 2022 |

A própria IA apontou ressalvas que levamos para o slide: o dado de áreas de risco é de 2010; o número de mães solo é de 2018; e a comparação de favelas entre 2010 e 2022 é afetada pela mudança de metodologia do IBGE (o limite mínimo caiu de 51 para 21 domicílios), então parte do aumento é território recém-mapeado, não favelização nova.

### 2. Teste do prompt 2 (sem estrutura)

Prompt: *"perguntas para avaliar a vulnerabilidade"*.

A resposta veio genérica: perguntas soltas em 4 eixos (financeiro, social, profissional e rede de apoio), uma escala Likert de 1 a 5 e um pedido para especificarmos que tipo de vulnerabilidade queríamos avaliar. Nada focado em moradia, sem pontuação nem formato utilizável.

## Comparação entre os testes

| | Prompt 1 (estruturado) | Prompt 2 (sem estrutura) |
|---|---|---|
| Foco | Vulnerabilidade habitacional | Vulnerabilidade em geral |
| Critérios | 7 critérios com pesos definidos | Nenhum |
| Saída | Planilha ranqueada, recomendações e slides | Lista de perguntas |
| Pronto para usar? | Sim, como protótipo | Não |

## O que aprendi

- Papel, escopo, requisitos, formato e objetivo mudam completamente a qualidade da resposta. Sem eles a IA devolve uma lista genérica ou pergunta o que você quer.
- Iterar faz parte: o primeiro pedido falhou e serviu de base para o prompt estruturado.
- Os dados da planilha são **fictícios**. O índice é um protótipo de metodologia e precisaria de dados reais (CadÚnico, mapeamento de risco) e validação técnica antes de qualquer uso de verdade.
- Dados estatísticos precisam de fonte e ano. Checar as ressalvas evita apresentar um número enganoso para a banca.
