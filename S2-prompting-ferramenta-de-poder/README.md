<img width="1280" height="640" alt="capa" src="https://github.com/user-attachments/assets/6691d4d1-94b7-4db1-9fd8-8c77baab851b" />

Um índice de vulnerabilidade habitacional criado com IA para ajudar o poder público a priorizar famílias no acesso à moradia, e uma comparação que mostra o que muda quando o prompt tem estrutura.

```
FICHA DO PROJETO ──────────────────────

Semana ...... 02
Módulo ...... Prompting como Ferramenta de Poder
Tipo ........ Em grupo (Leticia, Bea, Larissa Roberta, Larissa e Alexsandra Moura)
Meu papel ... Integrante da equipe: construção e teste dos prompts
Ferramentas . Claude · ChatGPT
Status ...... Concluído
```

### 1. Problema
Quem trabalha com política habitacional precisa decidir quem atender primeiro, e a fila não tem critério objetivo. Quem sente essa dor são as famílias em situação de rua, em ocupação, morando de favor ou com aluguel pesado demais.

### 2. Objetivo
Criar um critério objetivo para priorizar famílias em vulnerabilidade habitacional e recomendar encaminhamentos jurídicos, financeiros e urbanísticos.

> Se a equipe de habitação tiver um índice de vulnerabilidade com critérios claros, então consegue priorizar atendimentos de forma justificável, e não por ordem de chegada.

### 3. Processo
1. **Primeira tentativa:** uma pergunta solta sobre moradia. A IA não entendeu o que fazer e pediu o objetivo.
2. **Prompt estruturado:** reescrevemos o pedido com papel, escopo, requisitos, restrições, formato e objetivo.
3. **Índice:** definimos 7 critérios em 3 dimensões, somando até 100 pontos.
4. **Geração:** a IA montou uma planilha com 100 cadastros fictícios, ranking e recomendações, e uma apresentação de 7 slides.
5. **Teste de contraste:** rodamos um prompt sem estrutura em outra IA para comparar.

| Bloco | Conteúdo |
|-------|----------|
| **Papel** | Especialista em soluções habitacionais e planejamento urbano social |
| **Escopo** | Ranquear as pessoas em maior situação de vulnerabilidade |
| **Requisitos** | Índice de 0 a 100 em 3 dimensões e 7 critérios |
| **Restrições** | Não gerar imagens nem áudio |
| **Formato** | Planilha Excel com nome, idade, contato e pontuação |
| **Objetivo** | Cruzar dados de território, imóveis e famílias para recomendar encaminhamento jurídico, financeiro e urbanístico |

### 4. Decisões
| Decisão | Por quê |
|---|---|
| Três dimensões: socioeconômica, risco habitacional e vínculo territorial | Vulnerabilidade de moradia não é só renda: área de risco e rede de apoio também pesam |
| Pontuar o vínculo com o território (mora no entorno do imóvel) | Mudar a família para longe rompe a rede de apoio que ela já tem |
| Usar só dados fictícios | O índice é um protótipo de metodologia, não uma base real de pessoas |
| Levar para os slides as ressalvas que a IA apontou nos dados do IBGE | O dado de áreas de risco é de 2010, e a contagem de favelas mudou de metodologia em 2022 |

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

### 5. Resultado
📊 [Slides de apresentação (Google Drive)](https://drive.google.com/file/d/1VVfuL7sKiseBO60Ry7vc3osaiN_4ALT1/view?usp=sharing)

- **Planilha com 100 cadastros fictícios** em 3 abas:
  1. *Ranking de vulnerabilidade*: posição, pontuação e nível (Crítica, Alta, Média, Baixa ou Mínima)
  2. *Critérios detalhados*: quais critérios cada pessoa atende, com subtotal por dimensão
  3. *Resumo e recomendações*: distribuição por nível e encaminhamento sugerido para cada faixa
- **Consulta individual:** perguntamos a posição de uma pessoa no ranking, e a IA respondeu com posição, pontuação e nível.
- **Apresentação de 7 slides** para o poder público, incluindo dados de contexto:

| Indicador | Fonte |
|-----------|-------|
| 8,3 milhões de pessoas em áreas de risco | IBGE–Cemaden, Censo 2010 |
| 11 milhões de mães solo, 61% negras | PNAD/IBGE 2018 |
| 16,4 milhões de pessoas em favelas e comunidades urbanas (11,4 mi em 2010) | Censo IBGE 2022 |

**Prompt estruturado × prompt solto:**

| | Prompt 1 (estruturado) | Prompt 2 ("perguntas para avaliar a vulnerabilidade") |
|---|---|---|
| Foco | Vulnerabilidade habitacional | Vulnerabilidade em geral |
| Critérios | 7 critérios com pesos definidos | Nenhum |
| Saída | Planilha ranqueada, recomendações e slides | Perguntas soltas em 4 eixos e escala de 1 a 5 |
| Pronto para usar? | Sim, como protótipo | Não |

### 6. Aprendizados
- **O que funcionou:** papel, escopo, requisitos, formato e objetivo mudaram completamente a resposta. Sem eles, a IA devolveu uma lista genérica.
- **O que eu faria diferente:** validar os critérios e os pesos com quem trabalha com habitação antes de gerar a planilha.
- **O que levo para os próximos projetos:** iterar faz parte, e o primeiro pedido que falhou serviu de base para o bom. Todo número precisa de fonte e ano.

### 7. Próximos passos
- [ ] Validar os pesos do índice com especialistas em política habitacional
- [ ] Testar o índice com dados reais anonimizados (CadÚnico, mapeamento de risco)

---

← [Voltar para todos os projetos](../README.md) · [Portfólio](https://www.alexsandramoura.com.br) · [LinkedIn](https://www.linkedin.com/in/alexsandramoura)
