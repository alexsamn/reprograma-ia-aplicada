## O Inventário de Problemas

<img width="1280" height="640" alt="capa" src="https://github.com/user-attachments/assets/4afaa31a-e2a3-4d89-832a-19ec2ee215e8" />


Um mapeamento de problemas da minha rotina para descobrir quais a IA consegue resolver, e um prompt estruturado para atacar o principal: o case de portfólio travado na fase de pesquisa.

```
FICHA DO PROJETO ──────────────────────

Semana ...... 01
Módulo ...... Nivelamento
Tipo ........ Individual
Meu papel ... Inventário, filtro de viabilidade e construção do prompt
Ferramentas . IA generativa (chat)
Status ...... Concluído
```

### 1. Problema
Tarefas do dia a dia que tomam tempo ou geram desgaste nem sempre são problemas "de IA". Levantei três situações da minha rotina:

| # | Problema | Contexto |
|---|----------|----------|
| 1 | Case de portfólio de UI/UX travado na etapa de pesquisa | Muito conteúdo, sem clareza do que priorizar nem de como usar o tempo |
| 2 | Onde estacionar a bike com segurança em São Paulo | O Google Maps não tem a informação; as dicas se perdem no grupo de WhatsApp de ciclistas |
| 3 | Encontrar oficinas de bike confiáveis por perto | Poucas avaliações no Google Maps; a recomendação circula só no boca a boca |

### 2. Objetivo
Escolher um problema que a IA consiga resolver e construir um prompt que entregue um plano executável.

> Se eu tiver um mentor de IA com um cronograma semanal e acompanhamento às sextas, então consigo terminar o case de portfólio em 4 semanas, trabalhando 3h por dia.

### 3. Processo
1. **Inventário:** listei os problemas recorrentes da rotina.
2. **Filtro de viabilidade:** mantive só o que é texto, organização de dados, planejamento ou rascunho, sem depender de intervenção física.
3. **Mapeamento:** separei problema, objetivo e resultado esperado (um PDF com plano semanal até a entrega do case).
4. **Prompt:** estruturei o pedido em 5 blocos: papel, contexto, tarefa, formato de saída, e tom e critérios.

### 4. Decisões
| Decisão | Por quê |
|---|---|
| Escolher o problema 1 (case de portfólio) | É planejamento e priorização, onde a IA funciona bem como apoio. Os problemas 2 e 3 dependem de dados de campo que a IA não tem |
| Pedir acompanhamento toda sexta, com corte de escopo do MVP em caso de atraso | Um cronograma estático não se ajusta quando a semana sai do plano |
| Pedir feedback direto, sem resposta mastigada | O objetivo é aprender a pensar como designer, não receber o case pronto |
| Avaliar as entregas pelo olhar de quem contrata | O case existe para ser mostrado em entrevistas |

### 5. Resultado
Prompt estruturado em 5 blocos:

| Bloco | Conteúdo |
|-------|----------|
| **Papel** | Mentor sênior de produto digital (UI/UX) acompanhando uma designer júnior |
| **Contexto** | Tema "Jovens e o mercado de trabalho"; pesquisa qualitativa e desk research prontos até o Mapa de Empatia; prazo de 4 semanas; 3h/dia, de segunda a sexta |
| **Tarefa** | Montar e manter um cronograma semana a semana até o case finalizado e apresentado |
| **Formato de saída** | (1) PDF estilizado para impressão, com checklists por semana, blocos diários de 3h e um entregável concreto por semana; (2) acompanhamento toda sexta, com ajuste de cronograma e corte de escopo do MVP em caso de atraso |
| **Tom e critérios** | Feedback direto; avaliação pelo olhar de quem recruta (raciocínio crítico, definição do problema, validação rápida); case com início, meio e fim; fechamento semanal com resultado e aprendizado |

<details>
<summary>Ver prompt completo</summary>

```text
Papel:
Atue como um mentor de produto digital (UI/UX) sênior, experiente, paciente,
estratégico e alinhado ao mercado. Seu objetivo é me mentorar como designer
júnior, mantendo meu ritmo de execução diário (3h/dia, de segunda a sexta),
focando em pequenas vitórias semanais até o case finalizado e a apresentação
em 4 semanas.

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

### 6. Aprendizados
- **O que funcionou:** separar problema, objetivo e entregável antes de abrir a IA. O prompt saiu muito mais preciso.
- **O que eu faria diferente:** registrar a resposta da IA junto com o prompt, para mostrar o resultado e não só o pedido.
- **O que levo para os próximos projetos:** nem todo problema é "de IA". Os problemas 2 e 3 precisam de dados coletados no mundo real, não de geração de texto. E pedir acompanhamento contínuo transforma a IA de gerador de resposta única em ferramenta de gestão do projeto.

### 7. Próximos passos
- [ ] Anexar o cronograma gerado pela IA como resultado do prompt
- [ ] Avaliar os problemas 2 e 3 como produto com coleta de dados colaborativa, e não só com IA

---

← [Voltar para todos os projetos](../README.md) · [Portfólio](https://www.alexsandramoura.com.br) · [LinkedIn](https://www.linkedin.com/in/alexsandramoura)
