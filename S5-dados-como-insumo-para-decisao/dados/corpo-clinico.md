# Banco de Dados da Clínica — Corpo Clínico (v2, dados fictícios)

**Total de profissionais:** 32 (era 96)
**Janela de funcionamento:** 07h–18h, todas as agendas dentro desse intervalo
**Base de pacientes:** 78 pacientes únicos / 100 registros paciente-especialidade

## Regra de dimensionamento aplicada (1 médico : 15 pacientes)

| Bloco | Cálculo | Resultado |
|-------|---------|-----------|
| Clínica Geral (porta de entrada — todo paciente tem um clínico) | ceil(78 pacientes ÷ 15) | 6 médicos |
| Cada especialidade (demanda própria) | ceil(pacientes da especialidade ÷ 15) | 1 médico cada × 26 |
| **Total** | | **32** |

Nenhuma especialidade do banco de pacientes passa de 8 pacientes, então todas ficam com 1 profissional sem estourar o teto de 15.

---

## Corpo clínico

| ID | Especialidade | Nome do Médico | Agenda Disponível | Pacientes na base |
|----|---------------|----------------|-------------------|-------------------|
| M001 | Clínica Geral | Dr. Adalberto Ximenes Faria | Seg a Sex, 07h–13h | 78 (painel) |
| M002 | Clínica Geral | Dra. Renata Poli Carneiro | Seg a Sex, 12h–18h | 78 (painel) |
| M003 | Clínica Geral | Dr. Emerson Vilaça Prado | Seg a Sex, 07h–13h | 78 (painel) |
| M004 | Clínica Geral | Dra. Lívia Sampaio Grillo | Seg a Sex, 12h–18h | 78 (painel) |
| M005 | Clínica Geral | Dr. Gilmar Toledo Pessoa | Seg, Qua e Sex, 08h–14h | 78 (painel) |
| M006 | Clínica Geral | Dra. Sônia Braga Malaquias | Ter, Qui e Sáb, 07h–13h | 78 (painel) |
| M007 | Alergologia | Dra. Sueli Kawano Prates | Ter e Qui, 08h–12h | 2 |
| M008 | Angiologia | Dr. Gilberto Assunção Sarti | Qua e Sex, 07h–12h | 3 |
| M009 | Cardiologia | Dr. Túlio Bessa Cavalcante | Seg a Qui, 07h–13h | 8 |
| M010 | Dermatologia | Dra. Andreia Kuroda Belmonte | Seg e Qua, 09h–15h | 6 |
| M011 | Endocrinologia | Dr. Sílvio Ramalho Botelho | Seg a Qua, 08h–13h | 6 |
| M012 | Fisioterapia | Dr. Lucas Terêncio Mesquita | Seg a Sex, 07h–13h | 3 |
| M013 | Fonoaudiologia | Dra. Marília Esteves Vasques | Qua e Sex, 08h–14h | 2 |
| M014 | Gastroenterologia | Dr. Reinaldo Bustamante Cruz | Seg e Qui, 08h–13h | 4 |
| M015 | Geriatria | Dr. Osmar Fontes Cavallini | Seg a Qua, 08h–13h | 3 |
| M016 | Ginecologia | Dra. Heloísa Prado Vitorino | Seg, Qua e Sex, 08h–14h | 6 |
| M017 | Hematologia | Dra. Cláudia Rezende Portilho | Ter e Qui, 08h–14h | 1 |
| M018 | Infectologia | Dr. Gabriel Assis Monteiro | Seg, Qua e Sex, 12h–17h | 1 |
| M019 | Mastologia | Dra. Eliane Nascimento Vergara | Ter e Qui, 08h–13h | 2 |
| M020 | Nefrologia | Dr. Ari Bezerra Colombo | Seg e Qua, 07h–12h | 3 |
| M021 | Neurologia | Dr. Maurício Xavier Tostes | Seg a Qua, 12h–17h | 4 |
| M022 | Nutrição | Dra. Ingrid Sá Nepomuceno | Seg a Sex, 08h–13h | 5 |
| M023 | Oftalmologia | Dr. Ademar Vilela Fiúza | Seg, Qua e Sex, 08h–14h | 4 |
| M024 | Oncologia | Dr. Cláudio Berger Mascarenhas | Seg a Qua, 08h–14h | 2 |
| M025 | Ortopedia | Dr. Jefferson Malta Carvalhaes | Seg a Sex, 07h–12h | 7 |
| M026 | Otorrinolaringologia | Dr. Wanderley Chaves Bonatti | Seg e Qua, 09h–14h | 3 |
| M027 | Pediatria | Dra. Milena Faro Bandeira | Seg a Sex, 08h–12h | 3 |
| M028 | Pneumologia | Dr. Célio Marques Andrade | Seg a Qua, 07h–13h | 3 |
| M029 | Psicologia | Dra. Marina Duque Rosales | Seg a Sex, 09h–15h | 4 |
| M030 | Psiquiatria | Dr. Estevão Miranda Aloise | Seg e Qua, 12h–18h | 3 |
| M031 | Reumatologia | Dr. Hélio Sanchez Furtado | Seg e Qui, 08h–13h | 4 |
| M032 | Urologia | Dr. Onofre Batista Leal | Seg a Qua, 12h–17h | 5 |

---

## Notas

- Clínica Geral cobre 07h–18h de segunda a sexta com dois turnos sobrepostos (M001/M003 manhã, M002/M004 tarde), mais reforço em dias alternados e sábado de manhã.
- Especialidades com 1 profissional e agenda de 2 dias (Alergologia, Angiologia, Fonoaudiologia, Mastologia, Nefrologia) são os gargalos mais prováveis em simulação de fila.
- Nenhuma agenda ultrapassa 18h nem começa antes das 07h.
