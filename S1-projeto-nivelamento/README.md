# S1 · Projeto de Nivelamento — O Inventário de Problemas

**Aluna:** Alexsandra Moura
**Tipo:** individual
**Arquivo da entrega:** [`S1-inventario-de-problemas.pdf`](./S1-inventario-de-problemas.pdf)

## Objetivo da atividade

Identificar tarefas do dia a dia que consomem tempo ou geram desgaste, filtrar quais delas a IA consegue resolver e construir um prompt estruturado para resolver uma delas.

## Entregáveis

### 1. Inventário de problemas

Levantei 4 problemas recorrentes da minha rotina:

| # | Problema | Contexto |
|---|----------|----------|
| 1 | Case de portfólio de UI/UX travado na etapa de pesquisa | Muito conteúdo, sem clareza do que priorizar nem de como usar o tempo |
| 2 | Onde estacionar a bike com segurança em São Paulo | Google Maps não tem a informação; as dicas ficam perdidas no grupo de WhatsApp de ciclistas |
| 3 | Encontrar oficinas de bike confiáveis por perto | Poucas avaliações no Google Maps; a recomendação circula só no boca a boca do grupo |
| 4 | Organizar a busca de emprego e freela | Falta um cronograma que junte busca de vagas, prática de entrevista e currículo adaptado a ATS |

### 2. Filtro de viabilidade

Critérios: o problema precisa ser baseado em texto, organização de dados, planejamento ou rascunho, e não pode depender de intervenção física.

**Problema escolhido: #1, o case de portfólio.** É um problema de planejamento e priorização, que é onde a IA funciona bem como apoio. Os problemas 2 e 3 dependem de dados de campo que a IA não tem (localização e segurança de bicicletários, reputação de oficinas).

### 3. Mapeamento de objetivo e resultado esperado

- **Problema detalhado:** o case está travado na pesquisa por acúmulo de estudos e falta de clareza sobre o que priorizar no tempo disponível.
- **Objetivo:** ter o case de portfólio pronto para mostrar em entrevistas de UI/UX, com uma estrutura de estudo e execução até o entregável final.
- **Resultado esperado:** um PDF com plano semanal até a data de entrega do case.

### 4. Prompt construído

Prompt estruturado em 5 blocos:

| Bloco | Conteúdo |
|-------|----------|
| **Papel** | Mentor sênior de produto digital (UI/UX) acompanhando uma designer júnior |
| **Contexto** | Tema "Jovens e o mercado de trabalho"; pesquisa qualitativa e desk research prontos até o Mapa de Empatia; prazo de 4 semanas; 3h/dia, segunda a sexta |
| **Tarefa** | Montar e manter um cronograma semana a semana até o case finalizado e apresentado |
| **Formato de saída** | (1) PDF estilizado para impressão, com checklists por semana, blocos diários de 3h e um entregável concreto por semana; (2) acompanhamento toda sexta, com ajuste de cronograma e corte de escopo do MVP em caso de atraso |
| **Tom e critérios** | Feedback direto, sem resposta mastigada; avaliação pelo olhar do recrutador (raciocínio crítico, definição do problema, validação rápida); case com início, meio e fim; fechamento semanal com resultado e aprendizado |

<details>
<summary>Ver prompt completo</summary>

```text
Papel:
Atue como um mentor de produto digital (UI/UX) sênior, experiente, paciente,
estratégico e alinhado ao mercado. Seu objetivo é me mentorar como designer
júnior, mantendo meu ritmo de execução diário (3h/dia, de segunda a sexta),
reduzindo a ansiedade de entregar tudo de uma vez e focando em pequenas
vitórias semanais até o case finalizado e a apresentação em 4 semanas.

Contexto do Projeto:
- Tema: Jovens e o mercado de trabalho
- Estágio Atual: Pesquisa qualitativa pronta, Desk Research feito até o Mapa de Empatia.
- Prazo Total: 4 semanas
- Disponibilidade: 3 horas por dia (Segunda a Sexta)

Sua Tarefa:
Monte e mantenha um cronograma semana a semana até o prazo final, partindo do
meu estágio atual até o case study finalizado e apresentado.

Formato de Saída & Entregas:
1. Cronograma Inicial: Disponibilizado em PDF estilizado para impressão,
   contendo marcas de seleção (checklists) por semana, divisão por blocos
   diários de 3h e entregável concreto semanal.
2. Acompanhamento Contínuo no Chat (Toda Sexta-feira): Eu reportarei o que foi
   executado na semana. Caso haja atrasos, você deve ajustar o cronograma e
   re-priorizar o escopo do MVP para não estourar o prazo final de 4 semanas.

Tom e Postura:
- Direto e objetivo: Se minha apresentação, fluxo de UI, raciocínio lógico ou
  entrega estiverem ruins, confusos ou genéricos, diga abertamente o porquê e
  onde errei.
- Não entregue a resposta mastigada: Faça-me pensar e entender a razão por trás
  de cada decisão de design. Explique por que algo funciona ou falha no mercado.

Critérios de Avaliação:
- Foco do Recrutador: Avalie cada entrega com base no que gestores de
  contratação buscam (raciocínio crítico, clareza na definição do problema,
  validação rápida e solução funcional dentro de restrições de tempo).
- Estrutura Completa: Garanta que o case tenha início (problema validado),
  meio (processo decisório e iterações) e fim (solução e métricas).
- Fechamento Semanal: Cada fase encerrará com uma análise crítica de
  Resultado e Aprendizado.
```

</details>

## O que aprendi

- Separar **problema**, **objetivo** e **entregável** antes de abrir a IA deixa o prompt muito mais preciso.
- Nem todo problema é "de IA": os problemas 2 e 3 precisam de dados coletados no mundo real, não de geração de texto.
- Pedir acompanhamento contínuo com regra de corte de escopo transforma a IA de gerador de resposta única em ferramenta de gestão do projeto.
