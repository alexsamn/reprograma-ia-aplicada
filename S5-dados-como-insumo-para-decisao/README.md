# S5 · Dados como Insumo para Decisão

**Aluna:** Alexsandra Moura
**Tipo:** individual

Duas análises com o mesmo princípio: **separar o que o número mostra do que alguém está concluindo**, e só então decidir.

| Parte | Pergunta de decisão | Entregável |
|-------|---------------------|------------|
| 1 | A campanha de vacinação de idosos fracassou? | Leitura crítica, prompt de agente de IA, 2 gráficos, DIKW |
| 2 | Qual o melhor dia da semana para marcar uma consulta? | Bases de dados fictícias + apresentação com recomendação |

---

## Parte 1 · Desafio 01: A campanha de vacinação que "fracassou"

### O caso

Campanha de vacinação contra gripe para idosos (60+): **11.160 vacinados** de **18.000 cadastrados no SUS**, cobertura oficial de **62%** contra uma meta de **90%**. O secretário de saúde defende a campanha recalculando a cobertura sobre uma estimativa de **14.500 idosos ativos** (77%). A oposição aponta 6.840 idosos sem vacina, 2 óbitos por gripe e uma UBS que ficou 5 dias sem vacina.

### O que os dados dizem

Organizei os números por quem os apresenta:

| Fonte | Dados |
|-------|-------|
| **Campanha** | 18.000 idosos cadastrados · 11.160 vacinados · cobertura de 62% · meta de 90% · R$ 285.000 · 45 dias · 6 UBS + 2 pontos volantes |
| **Secretário** | Base de 14.500 "idosos ativos" (77%) · 1.200 vacinações em domicílio · campanha anterior com 58% · R$ 25,54 por dose, contra uma referência nacional de R$ 32 |
| **Oposição** | 6.840 não vacinados · 2 óbitos por gripe · UBS Esperança 5 dias sem vacina · pontos volantes abertos só 3 dias cada · cidade vizinha com 83% · pesquisa com 200 não vacinados: 35% não sabiam da campanha, 28% acharam o posto longe, 20% tinham medo de efeito colateral, 17% não achavam necessário |
| **Nenhum lado usou** | 60% dos idosos se informam pelo WhatsApp, e a campanha não usou o canal · os 2 idosos que morreram frequentavam a UBS, mas o protocolo não prevê vacinar na consulta de rotina · a falta de vacina foi causada por geladeira quebrada sem equipamento de backup · a cidade vizinha usou agentes comunitários de saúde (ACS) porta a porta; o município cortou 30% do programa de ACS no ano anterior |

### O que os dados não dizem

- **De onde vem o número de 14.500 idosos ativos.** É uma estimativa sem método declarado, e é ela que faz a cobertura subir de 62% para 77%.
- **Se a cidade vizinha é comparável.** Não há dados de infraestrutura nem do tamanho da população-alvo.
- **Quanto a falta de vacina pesou.** Não se sabe quantos idosos dependiam da UBS Esperança, então não dá para medir o efeito dos 5 dias no resultado.

### Perguntas que precisam de mais dados

1. Qual foi o método e a origem dos dados que chegaram aos 14.500 idosos ativos?
2. A cidade vizinha tem características estruturais comparáveis às do município?

### Prompt do agente de IA

Agente de apoio à decisão em **saúde pública municipal**, com regras explícitas para não substituir o julgamento humano:

- **Análise:** listar fatos observáveis; identificar lacunas, problemas de qualidade e vieses; testar explicações alternativas sem afirmar causa sem evidência; comparar pelo menos duas opções de decisão
- **Esclarecimento:** antes de concluir, listar as perguntas que só um humano com acesso aos dados originais pode responder
- **Recomendação:** SIM, NÃO ou AINDA NÃO, com nível de confiança de 0 a 100% e o que faria a recomendação mudar
- **Restrições:** não inventar números, fontes ou fatos (escrever "dado não disponível"); a **decisão final é do Conselho Municipal de Saúde**, pelo impacto sobre a saúde de idosos
- **Formato:** tabela de fatos · inferências e opiniões separadas · lacunas e vieses · perguntas · comparação de opções · recomendação · gatilhos de mudança

### Gráficos

**Gráfico 1: como a cobertura se compara à meta, ao histórico e à cidade vizinha, dependendo da base usada?**

![Cobertura vacinal por base de cálculo](./desafio01-grafico-cobertura.png)

- **O que mostra:** a escolha do denominador muda a cobertura em 15 pontos percentuais (de 62% para 77%). Mesmo na leitura mais favorável, a campanha fica abaixo da meta (90%) e da cidade vizinha (83%).
- **O que não prova:** qual denominador é o correto, nem que a diferença para a cidade vizinha vem do modelo de campanha. O corte de ACS é uma explicação alternativa.

**Gráfico 2: independentemente da taxa, quantas pessoas ficaram sem vacina?**

![Idosos não vacinados por base de cálculo](./desafio01-grafico-nao-vacinados.png)

- **O que mostra:** mesmo na base do secretário (14.500), **3.340 idosos** ficaram sem proteção.
- **O que não prova:** que essas pessoas correm o mesmo risco, nem quantas delas se encaixam nos motivos da pesquisa (comunicação, distância, medo).

### DIKW: de dado a decisão

| Nível | Exemplo |
|-------|---------|
| **Dado** | 11.160 |
| **Informação** | 11.160 vacinados de 18.000 cadastrados |
| **Conhecimento** | Os idosos que morreram já frequentavam a UBS, mas o protocolo não previa vacinar durante a consulta: a falha foi de **oportunidade perdida**, não de acesso |
| **Sabedoria** | Em vez de discutir se a campanha foi sucesso ou fracasso, o Conselho pode **mudar o protocolo para vacinar em qualquer consulta de rotina** |

---

## Parte 2 · Qual o melhor dia para marcar uma consulta?

Simulação com dados 100% fictícios de uma clínica em São Paulo, na semana de 14 a 18/09/2026, cruzando a **ocupação da agenda** com o **tempo de deslocamento** dos pacientes.

📊 [Apresentação completa (PDF)](./apresentacao-melhor-dia-consulta.pdf)

### Bases de dados

| Arquivo | Conteúdo |
|---------|----------|
| [`dados/pacientes.md`](./dados/pacientes.md) | 78 pacientes, 100 registros por especialidade |
| [`dados/corpo-clinico.md`](./dados/corpo-clinico.md) | 32 profissionais em 27 especialidades, dimensionados pela regra 1 médico : 15 pacientes |
| [`dados/agenda-semanal.md`](./dados/agenda-semanal.md) | 86 atendimentos de 1h, ocupação por dia e por hora, médicos ociosos |
| [`dados/trafego-deslocamento.md`](./dados/trafego-deslocamento.md) | Tempo de cada paciente até a clínica, por modal, zona e condição de trânsito |

O corpo clínico passou por uma revisão: a primeira versão tinha **96 profissionais**. Com a regra 1:15 aplicada à base real de pacientes, o quadro caiu para **32**.

### Resultado

![Atendimentos por dia](./grafico-atendimentos-por-dia.png)

![Tempo de deslocamento por dia](./grafico-deslocamento-por-dia.png)

| Dia | Atendimentos | Deslocamento médio | Trânsito | Recomendação |
|-----|-------------:|-------------------:|----------|--------------|
| **Terça** | 4 | 33 min | normal | 1º, melhor escolha |
| Quinta | 14 | 38 min | normal | 2º, boa alternativa |
| Quarta | 26 | 40 min | normal | 3º, aceitável |
| Segunda e sexta | 26 e 16 | 49 e 52 min | intenso | evitar |

**Ressalva da recomendação:** na terça só 20 dos 32 profissionais atendem, e 12 especialidades ficam de fora (entre elas Dermatologia, Ginecologia, Oftalmologia e Psiquiatria). Para consulta com especialista, **quinta é a escolha mais segura**.

### Limitações da análise

- **Os dados são simulados.** A condição de trânsito de cada dia (intenso ou normal) foi definida como parâmetro do modelo, e a distância de cada paciente foi sorteada sem relação com o endereço cadastrado. A diferença entre segunda/sexta e os outros dias vem dessa premissa; ela não foi observada.
- **A amostra da terça é pequena.** A média de 33 min vem de apenas 4 deslocamentos. Entre terça, quarta e quinta, que têm o mesmo fator de trânsito no modelo, a diferença depende de quais pacientes foram sorteados para cada dia.
- **A agenda não chega a lotar em nenhum dia.** A ocupação fica entre 4% e 19%, então "dia cheio" aqui quer dizer mais volume relativo, não falta de horário. O achado mais forte da base é outro: **o quadro está superdimensionado**. Os 32 profissionais comportariam cerca de 480 pacientes, e a base tem 78.

## O que aprendi

- **O denominador muda a história.** A mesma campanha tem 62% ou 77% de cobertura dependendo da base, e as duas leituras ainda deixam milhares de pessoas sem vacina.
- **Taxa e número absoluto contam histórias diferentes**, então os dois precisam aparecer juntos.
- **A melhor decisão às vezes não responde à pergunta original.** "Sucesso ou fracasso?" vale menos do que "o que mudar no protocolo?".
- **Um prompt de IA para decisão precisa de freios:** proibição de inventar dados, separação entre fato e inferência, e decisão final humana.
