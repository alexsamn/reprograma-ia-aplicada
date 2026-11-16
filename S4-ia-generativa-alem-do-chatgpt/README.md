# S4 · IA Generativa Aplicada — Além do ChatGPT

**Aluna:** Alexsandra Moura
**Tipo:** individual
**Projeto:** Agente de Transição de Carreira

> Os arquivos originais desta entrega (instruções do agente, documento gerado e apresentação) não estão no repositório porque têm informações pessoais. Este README descreve o método e a estrutura do projeto.

## Problema

Quem muda de área, no meu caso de Desenvolvimento de Produto Têxtil para Product Design (UI/UX), costuma estudar com cursos que ensinam ferramenta e com cronogramas genéricos que cobram conteúdo consumido, não raciocínio de produto. Faltava um apoio que organizasse estudo, portfólio e preparação para o mercado e que **cobrasse entrega real**.

## Solução: um agente de IA com regras próprias

Em vez de começar do zero a cada conversa no chat, construí um **agente com instruções fixas** que funciona como mentor de transição de carreira.

### 1. Prompt inicial

A primeira versão definia:

- **Papel:** mentor de transição que conecta a experiência anterior em produto físico com UI/UX
- **Pilares de atuação:** prospecção de vagas, hackathons, simulação de entrevistas, currículo/LinkedIn e organização da semana
- **Restrições:** respeitar os horários já comprometidos; não inventar vagas, links ou prazos
- **Formato de saída:** resumo executivo + tabela de ações + bloco de agenda

E terminava com uma instrução importante: **"antes de definir todas as regras do agente, me questione"**. Assim a IA levantou as lacunas antes de fechar as regras.

### 2. Instruções finais (depois do questionamento)

| O que entrou na versão final | Por quê |
|------------------------------|---------|
| **Prioridade entre frentes de trabalho**, com regra fixa do que vem primeiro | Evita dividir o esforço igualmente entre tudo |
| **Critérios de "pronto":** um case só conta como concluído quando está publicado com link; uma simulação de entrevista só conta com feedback registrado | Evita marcar como feito o que não gera resultado |
| **Métricas semanais** revisadas toda sexta | Transforma o plano em algo mensurável |
| **Regra de status obrigatório:** perguntar a fase atual antes de montar qualquer plano | O agente não presume que nada mudou desde a última conversa |
| **Gatilho de reavaliação:** quando o 1º case for publicado, o agente libera novas frentes sozinho | Destrava a etapa seguinte sem eu precisar pedir |
| **Anti-dispersão:** não abrir novas frentes enquanto houver trabalho de portfólio não publicado | Foco em terminar antes de começar |
| **Estilo:** direto, técnico, baseado em evidência, sem bajulação | Feedback útil em vez de motivacional |

### 3. Resultado: plano estratégico de 24 semanas

O agente consolidou currículo, perfil e um **plano de estudo em 5 fases**. Nenhuma fase fecha com "estudei sobre X": cada uma exige uma entrega concreta.

| Fase | Semanas | Foco | Entregas |
|-----:|---------|------|----------|
| 1 | 1–4 | Fundação de negócio | Problem statement, business model canvas, análise de 3 concorrentes |
| 2 | 5–8 | Pesquisa que vira decisão | 5 entrevistas + JTBD, opportunity solution tree, memo PR/FAQ |
| 3 | 9–14 | Design que decide | MVP no Figma com fluxos completos, design decision log, apresentação SCQA |
| 4 | 15–18 | Influência e navegação | Stakeholder map, pitch de 2 min gravado, rascunho do case study |
| 5 | 19–24 | Lançamento e síntese | App publicado, case study completo, retrospectiva, métricas da 1ª semana |

Referências usadas no plano: *Inspired* (Marty Cagan), *Continuous Discovery Habits* (Teresa Torres), Jobs to Be Done, Pirâmide de Minto (SCQA), *The Lean Startup*, *Influence* (Cialdini), *Obviously Awesome* (April Dunford) e a Lenny's Newsletter.

### 4. Checkpoint para a turma

Apresentação de 7 slides: problema → solução → mapa das 5 fases → resultado → evolução → status. Na data da apresentação eu estava na **Fase 1**.

## O que aprendi

- **Pedir para a IA me questionar antes de fechar as regras** gerou um agente muito mais preciso do que o prompt inicial.
- **Critérios de "pronto" e gatilhos** transformam um prompt em um sistema que se ajusta conforme a situação muda.
- **Mudança de mentalidade:** de "preciso aprender UX" para "preciso provar que já penso produto".
