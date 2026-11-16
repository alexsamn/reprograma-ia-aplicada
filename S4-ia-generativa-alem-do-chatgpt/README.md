# S4 · IA Generativa Aplicada — Além do ChatGPT

**Aluna:** Alexsandra Moura
**Tipo:** individual
**Projeto:** Agente de Transição de Carreira e Produtividade

## Arquivos da entrega

| Arquivo | O que é |
|---------|---------|
| [`S4-prompt-inicial.docx`](./S4-prompt-inicial.docx) | Primeira versão das instruções do agente |
| [`S4-agente-transicao-carreira.pdf`](./S4-agente-transicao-carreira.pdf) | Instruções finais do agente, revisadas |
| [`S4-dossie-transicao-carreira.docx`](./S4-dossie-transicao-carreira.docx) | Dossiê gerado com o agente: currículo, perfil e plano de 24 semanas |
| [`S4-checkpoint-transicao-carreira.pptx`](./S4-checkpoint-transicao-carreira.pptx) | Apresentação de checkpoint para a turma (7 slides, com roteiro de fala nas notas) |

## Problema

Estou migrando de **Desenvolvimento de Produto Têxtil** para **Product Design (UI/UX)**, desempregada e com rotina fixa de aulas à noite. Os cursos de UX ensinam ferramenta, e cronogramas genéricos de estudo cobram conteúdo consumido, não raciocínio de produto. Eu precisava de um apoio que organizasse candidaturas, portfólio, entrevistas e agenda, e que cobrasse entrega real.

## Solução: um agente de IA com regras próprias

Em vez de usar o chat genérico a cada conversa, construí um **agente com instruções fixas** que funciona como assessor de recolocação e mentor de rotina.

### 1. Prompt inicial

A primeira versão definia:

- **Papel:** assessor de recolocação e mentor de rotina, conectando as habilidades de moda com UI/UX
- **Contexto:** desempregada, sem portfólio publicado, 2 hackathons com MVP a melhorar, aulas seg–sex 19h–22h, Design Circuit em andamento, avaliando faculdade EAD para poder aplicar a estágio
- **5 pilares:** vagas de estágio e júnior · hackathons · simulação de entrevistas · currículo/LinkedIn · agenda da semana
- **Restrições:** nada entre 18h e 22h nos dias úteis; hackathons só online ou no fim de semana; não inventar vagas, links ou prazos
- **Formato de saída:** resumo executivo + tabela de ações + bloco de agenda

E terminava com uma instrução importante: **"antes de definir todas as regras do agente, me questione"**. Assim a IA levantou as lacunas antes de fechar as regras.

### 2. Instruções finais (depois do questionamento)

| O que entrou na versão final | Por quê |
|------------------------------|---------|
| **Prioridade entre trilhas:** candidatura têxtil contínua; candidatura UX pausada até o 1º case estar publicado | Aplicar a vaga de design sem portfólio publicado é candidatura fraca |
| **Critérios de "pronto":** case só conta com link público no CV e no LinkedIn; candidatura só conta com CV atualizado; simulação de entrevista só conta com feedback registrado | Evita marcar como feito o que não gera resultado |
| **Métricas semanais (revisão às sextas):** mínimo de 5 candidaturas têxtil, retornos recebidos, % do case ativo no Double Diamond, 1 simulação de entrevista | Transforma o plano em algo mensurável |
| **Regra de status obrigatório:** perguntar a fase atual antes de montar qualquer plano | O agente não presume que nada mudou desde a última conversa |
| **Gatilho de reavaliação:** ao publicar o 1º case, liberar hackathons e candidaturas UX automaticamente | Destrava as próximas frentes sem eu precisar pedir |
| **Inventário do portfólio:** 4 ativos abertos (case "Jovens e o mercado de trabalho", case "Mapa de bicicletário", Hackathon Web3 "Rede Semente" com 1º lugar, Techstars Startup Weekend IA) | Dá contexto real para priorizar |
| **Anti-dispersão:** não abrir novas frentes enquanto houver ativo de portfólio não publicado | Risco de dispersão já identificado |
| **Estilo:** direto, técnico, baseado em evidência, sem bajulação | Feedback útil em vez de motivacional |

> **Ponto em aberto:** o teto de gastos com cursos e ferramentas (R$100) ficou sem confirmação na versão entregue. Por isso a instrução final ainda tem a marcação "AJUSTAR ESTE TETO".

### 3. Resultado: Dossiê de Transição de Carreira

Documento consolidado com:

1. **Perfil profissional e objetivo**, posicionando a experiência têxtil como base para produto digital
2. **Experiência profissional**, de Assistente de Estilo a Estilista de Moda Sênior na L'atelier, mais a produção de desfiles na SPFW
3. **Formação e certificações:** Design de Moda (Senac), ADS (FIAP), Design Circuit, Figma, IA no Processo de Design
4. **Plano estratégico de 24 semanas em 5 fases**, cada uma com fontes de estudo, entregas e aplicação prática:

| Fase | Semanas | Foco | Entregas |
|-----:|---------|------|----------|
| 1 | 1–4 | Fundação de negócio | Problem statement, business model canvas, análise de 3 concorrentes |
| 2 | 5–8 | Pesquisa que vira decisão | 5 entrevistas + JTBD, opportunity solution tree, memo PR/FAQ |
| 3 | 9–14 | Design que decide | MVP no Figma com fluxos completos, design decision log, apresentação SCQA |
| 4 | 15–18 | Influência e navegação | Stakeholder map, pitch de 2 min gravado, rascunho do case study |
| 5 | 19–24 | Lançamento e síntese | App publicado, case study completo, retrospectiva, métricas da 1ª semana |

### 4. Checkpoint para a turma

Apresentação de 7 slides: problema → solução → mapa das 5 fases → resultado → evolução → status atual. Na data da apresentação eu estava na **Fase 1**, fechando as 3 entregas de fundação de negócio.

## O que aprendi

- **Pedir para a IA me questionar antes de fechar as regras** gerou um agente muito mais preciso do que o prompt inicial.
- **Critérios de "pronto" e gatilhos** transformam um prompt em um sistema que se ajusta conforme a situação muda.
- **Mudança de mentalidade:** de "preciso aprender UX" para "preciso provar que já penso produto".
