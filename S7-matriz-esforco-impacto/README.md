## Matriz de Esforço × Impacto — Priorizando onde usar IA

Uma matriz para decidir qual tarefa da rotina vale uma solução com IA, e a validação da tecnologia antes de construir, que trocou um agente autônomo por uma automação simples e mais segura.

```
FICHA DO PROJETO ──────────────────────

Semana ...... 07
Módulo ...... Matriz de Esforço × Impacto
Tipo ........ Individual
Meu papel ... Inventário, pontuação, priorização e validação da tecnologia
Ferramentas . Planilha · IA generativa
Status ...... Concluído
```

### 1. Problema
Muitas tarefas da rotina parecem boas candidatas a IA. Sem critério, a tendência é começar pela mais interessante, e não pela que mais rende.

### 2. Objetivo
Pontuar as tarefas, escolher a prioridade e confirmar se a tecnologia pensada é a certa antes de investir tempo.

> Se eu automatizar a tarefa de maior impacto e menor esforço, então o ganho aparece rápido, com pouco risco.

### 3. Processo
1. **Inventário:** listei 8 tarefas e dei notas de 1 a 5 para volume, risco de erro e complexidade, com uma hipótese de tecnologia para cada.
2. **Pontuação:** **Impacto** = volume. **Esforço** = complexidade + (erro ÷ 2), com teto de 5.
3. **Matriz:** posicionei as tarefas nos quadrantes.
4. **Validação:** pedi a uma IA, no papel de especialista em soluções com IA, casos de mercado, perguntas críticas e uma avaliação da tecnologia escolhida.

| # | Tarefa | Tipo | Tecnologia (hipótese) | Impacto | Esforço |
|--:|--------|------|-----------------------|:-------:|:-------:|
| 1 | Buscar e filtrar vagas de Moda e UI/UX | Braçal | Agente | **5** | **2,5** |
| 2 | Adaptar CV e carta para cada vaga | Mental | RAG | 4 | 4 |
| 3 | Treinar respostas para entrevista | Mental | LLM | 2 | 2 |
| 4 | Atualizar planilha de candidaturas | Braçal | LLM | 3 | 2,5 |
| 5 | Buscar freelas (Upwork, 99Freelas, Workana) | Braçal | Agente | 3 | 3 |
| 6 | Reuniões de planejamento (Discovery e Refinamento) | Mental | RAG | 1 | 1,5 |
| 7 | Buscar recrutadores e networking | Braçal | LLM | 1 | 1,5 |
| 8 | Acompanhar inscrições de hackathons | Braçal | LLM | 1 | 1,5 |

<details>
<summary>Ver o prompt de validação</summary>

```text
Você é um especialista em soluções com Inteligência Artificial.
Estou analisando o seguinte problema do meu dia a dia para criar uma solução com IA:
Buscar e filtrar vagas de Moda e UI/UX.
A tecnologia que estou pensando em usar inicialmente é: Agente de IA.

Com base nessas informações:
- Apresente 3 exemplos reais ou casos de uso semelhantes no mercado que resolvem
  esse mesmo tipo de problema usando IA.
- Faça 3 perguntas críticas sobre a viabilidade técnica, disponibilidade de dados ou
  esforço de implementação que eu preciso responder antes de começar a desenvolver.
- Avalie se a tecnologia escolhida por mim é a ideal para este caso de uso ou se outra
  abordagem seria mais eficiente e simples. Considere que queremos focar em soluções
  de baixo risco e alto impacto.
```

</details>

### 4. Decisões
| Decisão | Por quê |
|---|---|
| Priorizar a tarefa 1 (buscar e filtrar vagas) | Maior impacto (5) com esforço baixo (2,5): ganho rápido |
| **Trocar o agente autônomo por automação + 1 chamada de LLM** | Os casos de mercado (LinkedIn, Jobright, Indeed) funcionam porque têm acesso próprio a bases enormes de vagas. Um agente individual navegando sites quebra com login e captcha, e scraping pode violar termos de uso |
| Usar os alertas de vaga que já chegam por e-mail como fonte | Não tem risco legal (é só ler o próprio e-mail) e o fluxo é previsível |
| Gravar todas as vagas, não só as aprovadas | Permite enxergar os falsos negativos |
| Validar a IA por 2 semanas numa coluna "minha avaliação" | Se ela errar mais de 20%, o ajuste é na rubrica, não na tecnologia |
| Sem candidatura automática | Cada candidatura precisa de contexto próprio |

| Critério | Agente autônomo | Automação + 1 chamada de LLM |
|----------|-----------------|------------------------------|
| Fonte de dados | Navega em sites; quebra com login, captcha ou mudança de layout | Alertas de vaga que os sites já mandam por e-mail |
| Risco legal | Scraping pode violar termos de uso | Nenhum |
| Previsibilidade | Baixa | Alta: só a classificação usa IA |
| Custo | Muitas chamadas por execução | 1 chamada por vaga |
| Tempo para funcionar | Semanas | Um fim de semana |

### 5. Resultado
![Matriz de esforço × impacto](./matriz-esforco-impacto.png)

*Gráfico refeito a partir dos valores da planilha original.*

**Arquitetura escolhida:**
1. **Entrada:** alertas de vaga (LinkedIn, Gupy, Indeed, Vagas.com, Catho) chegando no Gmail
2. **Automação:** Google Apps Script lê os alertas uma vez por dia
3. **IA, uma única tarefa:** o LLM recebe a vaga e uma rubrica escrita e devolve um JSON com trilha, se a senioridade serve, nota e motivo
4. **Saída:** planilha com todas as vagas e filtro para nota ≥ 7

A tarefa 4 (atualizar a planilha de candidaturas) já tinha sido automatizada na [S3](../S3-ia-na-rotina-automacao/).

### 6. Aprendizados
- **O que funcionou:** questionar a própria hipótese antes de construir. O "agente" virou uma automação simples, com IA numa etapa só.
- **O que eu faria diferente:** escrever a rubrica de filtro antes de escolher a tecnologia.
- **O que levo para os próximos projetos:** a tecnologia raramente é o gargalo; o critério é. Um agente só faz sentido depois que o fluxo simples estiver estável.

### 7. Próximos passos
- [ ] Testar a rubrica com 20 vagas reais e medir o acerto (meta: 80% ou mais)
- [ ] Implementar o Apps Script e rodar por 2 semanas com validação manual

---

← [Voltar para todos os projetos](../README.md) · [Portfólio](https://www.alexsandramoura.com.br) · [LinkedIn](https://www.linkedin.com/in/alexsandramoura)
