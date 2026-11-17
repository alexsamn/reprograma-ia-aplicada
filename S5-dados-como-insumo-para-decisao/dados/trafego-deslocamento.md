# Tráfego de Deslocamento — Semana 14 a 18/09/2026 (dados fictícios)

**Destino:** Clínica — Rua Vergueiro, 1500, Paraíso, São Paulo/SP  
**Origem:** endereço cadastral de cada paciente, agrupado por zona  
**Deslocamentos:** 86 (um por atendimento agendado)  
**Condição de trânsito:** segunda e sexta INTENSO · terça, quarta e quinta normal

## 1. Parâmetros do modelo

| Parâmetro | Valor |
|-----------|-------|
| Velocidade base | Carro 26 km/h · App 25 · Metrô/Trem 24 · Ônibus 16 · A pé 4,5 |
| Congestionamento de fundo | +45% em dia intenso · +15% em dia normal |
| Adicional de rush (07h–09h e 16h–17h) | +26% em dia intenso · +20% em dia normal |
| Sensibilidade ao trânsito | Carro 1,00 · App 0,95 · Ônibus 0,90 · Metrô/Trem 0,12 · A pé 0 |
| Espera de embarque | Ônibus e Metrô 6–14 min · App 3–8 min |
| Folga de recepção | 10 min antes do horário da consulta |

O modal e a distância de cada paciente são sorteados uma única vez e permanecem fixos na semana; o que varia dia a dia é o fator de congestionamento.

## 2. Resumo por dia

| Dia | Trânsito | Deslocamentos | Tempo médio | Mediana | Máximo | Atraso médio vs. via livre |
|-----|----------|---------------|-------------|---------|--------|----------------------------|
| 14/09 (seg) | **INTENSO** | 26 | 49 min | 47 min | 86 min | +20 min |
| 15/09 (ter) | Normal | 4 | 33 min | 24 min | 71 min | +7 min |
| 16/09 (qua) | Normal | 26 | 40 min | 34 min | 120 min | +10 min |
| 17/09 (qui) | Normal | 14 | 38 min | 40 min | 78 min | +9 min |
| 18/09 (sex) | **INTENSO** | 16 | 52 min | 44 min | 122 min | +21 min |
| **Semana** | | **86** | **45 min** | **40 min** | **122 min** | **+15 min** |

## 3. Tempo médio por zona × dia (minutos)

| Zona | Pacientes | 14/09 (seg) | 15/09 (ter) | 16/09 (qua) | 17/09 (qui) | 18/09 (sex) |
|------|-----------|---|---|---|---|---|
| Centro | 13 | 37 | 14 | 22 | — | 20 |
| Zona Sul | 23 | 51 | — | 31 | 29 | 45 |
| Zona Oeste | 29 | 51 | 24 | 35 | 27 | 47 |
| Zona Norte | 3 | 58 | — | — | — | 44 |
| Zona Leste | 15 | 40 | 71 | 69 | 57 | 71 |
| Grande SP | 3 | 60 | — | 101 | — | 122 |

Células com "—" são zona/dia sem nenhum paciente agendado. **Atenção ao ler esta matriz:** várias células têm 1 a 3 observações, então o efeito do dia intenso não aparece limpo em todas as zonas — Zona Leste na segunda (40 min) fica abaixo da terça (71 min) porque os poucos pacientes agendados naquele dia usam metrô, que é praticamente imune ao congestionamento. O contraste seg/sex só é estatisticamente legível no agregado da seção 2.

## 4. Distribuição de modal por zona

| Zona | Carro próprio | App/Táxi | Ônibus | Metrô/Trem | Distância média |
|------|---|---|---|---|---|
| Centro | 5 | 4 | 4 | 0 | 5.5 km |
| Zona Sul | 9 | 1 | 8 | 5 | 8.9 km |
| Zona Oeste | 11 | 7 | 6 | 5 | 9.7 km |
| Zona Norte | 0 | 1 | 0 | 2 | 14.8 km |
| Zona Leste | 4 | 4 | 4 | 3 | 17.0 km |
| Grande SP | 1 | 0 | 2 | 0 | 19.3 km |

## 5. Deslocamentos detalhados

| Dia | Trânsito | Consulta | Sair às | ID | Paciente | Zona | Bairro | Km | Modal | Tempo |
|-----|----------|----------|---------|----|----------|------|--------|----|-------|-------|
| 14/09 (seg) | INTENSO | 08:00 | 07:08 | P006 | Roberto Kimura Sato | Centro | Liberdade | 5.1 | Ônibus | 42 min |
| 14/09 (seg) | INTENSO | 08:00 | 07:12 | P011 | Juliana Moraes Estevam | Centro | Santa Ifigênia | 7.3 | App/Táxi | 38 min |
| 14/09 (seg) | INTENSO | 08:00 | 06:47 | P026 | Rafael Monteiro Dias | Zona Norte | Santana | 18.0 | Metrô/Trem | 63 min |
| 14/09 (seg) | INTENSO | 08:00 | 07:07 | P039 | Priscila Nogueira Cunha | Zona Oeste | Sumaré | 9.9 | App/Táxi | 43 min |
| 14/09 (seg) | INTENSO | 08:00 | 06:51 | P040 | Leonardo Assis Villela | Zona Sul | Moema | 8.4 | Ônibus | 59 min |
| 14/09 (seg) | INTENSO | 09:00 | 08:07 | P075 | Elisa Fontoura Barros | Zona Oeste | Jardim América | 9.8 | App/Táxi | 43 min |
| 14/09 (seg) | INTENSO | 09:00 | 07:58 | P064 | Everton Lisboa Caldeira | Zona Oeste | Pompeia | 11.5 | App/Táxi | 52 min |
| 14/09 (seg) | INTENSO | 09:00 | 08:16 | P046 | Rodrigo Bastos Camargo | Zona Oeste | Pinheiros | 7.9 | Metrô/Trem | 34 min |
| 14/09 (seg) | INTENSO | 09:00 | 07:27 | P038 | Otávio Lemos Bandeira | Zona Oeste | Alto da Lapa | 12.4 | Ônibus | 83 min |
| 14/09 (seg) | INTENSO | 09:00 | 08:01 | P069 | Sabrina Vilela Antunes | Zona Oeste | Jardim América | 12.2 | Carro próprio | 49 min |
| 14/09 (seg) | INTENSO | 09:00 | 08:15 | P019 | Rosana Teixeira Amaral | Zona Sul | Saúde | 8.9 | Carro próprio | 35 min |
| 14/09 (seg) | INTENSO | 10:00 | 09:10 | P031 | Tatiane Moura Falcão | Zona Leste | Tatuapé | 10.3 | App/Táxi | 40 min |
| 14/09 (seg) | INTENSO | 10:00 | 08:56 | P050 | Nelson Aquino Batista | Zona Norte | Santana | 16.0 | Metrô/Trem | 54 min |
| 14/09 (seg) | INTENSO | 10:00 | 09:03 | P048 | Fábio Junqueira Rebelo | Zona Oeste | Vila Madalena | 13.0 | Metrô/Trem | 47 min |
| 14/09 (seg) | INTENSO | 10:00 | 08:29 | P020 | Felipe Cardoso Menezes | Zona Oeste | Cerqueira César | 12.6 | Ônibus | 81 min |
| 14/09 (seg) | INTENSO | 10:00 | 09:26 | P049 | Renata Coutinho Vasques | Zona Oeste | Vila Madalena | 7.3 | Carro próprio | 24 min |
| 14/09 (seg) | INTENSO | 10:00 | 08:24 | P029 | Débora Castro Ribeiro | Zona Sul | Campo Belo | 14.5 | Ônibus | 86 min |
| 14/09 (seg) | INTENSO | 10:00 | 08:55 | P009 | Patrícia Ferreira Gomes | Zona Sul | Ipiranga | 8.6 | Ônibus | 55 min |
| 14/09 (seg) | INTENSO | 12:00 | 10:50 | P018 | Paulo Henrique Braga | Grande SP | Vila Augusta | 17.7 | Carro próprio | 60 min |
| 14/09 (seg) | INTENSO | 12:00 | 11:21 | P009 | Patrícia Ferreira Gomes | Zona Sul | Ipiranga | 8.6 | Carro próprio | 29 min |
| 14/09 (seg) | INTENSO | 12:00 | 11:25 | P033 | Simone Aparecida Rocha | Zona Sul | Jardim Míriam | 6.2 | App/Táxi | 25 min |
| 14/09 (seg) | INTENSO | 14:00 | 13:31 | P055 | Bianca Trindade Rosa | Centro | Higienópolis | 4.0 | App/Táxi | 19 min |
| 14/09 (seg) | INTENSO | 14:00 | 13:03 | P030 | Eduardo Pacheco Lins | Centro | Consolação | 6.1 | Ônibus | 47 min |
| 14/09 (seg) | INTENSO | 14:00 | 12:41 | P034 | Henrique Portela Vidal | Zona Sul | Vila Clementino | 11.5 | Ônibus | 69 min |
| 14/09 (seg) | INTENSO | 15:00 | 14:12 | P056 | Jorge Amaral Bittar | Centro | Vila Buarque | 4.9 | Ônibus | 38 min |
| 14/09 (seg) | INTENSO | 15:00 | 13:57 | P041 | Adriana Melo Quadros | Zona Sul | Vila Clementino | 8.5 | Ônibus | 53 min |
| 15/09 (ter) | Normal | 10:00 | 09:36 | P035 | Isabela Freitas Marinho | Centro | Centro | 5.2 | Carro próprio | 14 min |
| 15/09 (ter) | Normal | 10:00 | 08:39 | P078 | Sidney Rabelo Pontes | Zona Leste | Tatuapé | 15.5 | Ônibus | 71 min |
| 15/09 (ter) | Normal | 10:00 | 09:22 | P049 | Renata Coutinho Vasques | Zona Oeste | Vila Madalena | 7.3 | App/Táxi | 28 min |
| 15/09 (ter) | Normal | 10:00 | 09:30 | P065 | Milena Rocha Sandoval | Zona Oeste | Vila Madalena | 8.0 | Carro próprio | 20 min |
| 16/09 (qua) | Normal | 08:00 | 05:50 | P028 | Wagner Souza Peixoto | Zona Leste | São Miguel Paulista | 22.8 | Ônibus | 120 min |
| 16/09 (qua) | Normal | 08:00 | 07:12 | P036 | Alexandre Duarte Peçanha | Zona Oeste | Lapa | 12.5 | Carro próprio | 38 min |
| 16/09 (qua) | Normal | 08:00 | 06:59 | P044 | Márcio Toledo Ferraz | Zona Sul | Santo Amaro | 9.1 | Ônibus | 51 min |
| 16/09 (qua) | Normal | 09:00 | 08:29 | P057 | Letícia Ramos Valadares | Centro | Santa Cecília | 6.5 | Carro próprio | 21 min |
| 16/09 (qua) | Normal | 09:00 | 08:08 | P032 | Bruno Carvalho Ostrowski | Zona Leste | Tatuapé | 13.9 | Carro próprio | 42 min |
| 16/09 (qua) | Normal | 09:00 | 08:14 | P003 | Fernanda Lopes Machado | Zona Oeste | Perdizes | 10.7 | Metrô/Trem | 36 min |
| 16/09 (qua) | Normal | 09:00 | 08:19 | P073 | Heloísa Marques Teles | Zona Oeste | Perdizes | 7.9 | App/Táxi | 31 min |
| 16/09 (qua) | Normal | 09:00 | 08:20 | P004 | João Pedro Vasconcelos | Zona Oeste | Pompeia | 6.2 | Metrô/Trem | 30 min |
| 16/09 (qua) | Normal | 09:00 | 08:18 | P040 | Leonardo Assis Villela | Zona Sul | Moema | 8.4 | Metrô/Trem | 32 min |
| 16/09 (qua) | Normal | 09:00 | 08:37 | P012 | Ricardo Almeida Fontes | Zona Sul | Jardim Umuarama | 4.2 | Carro próprio | 13 min |
| 16/09 (qua) | Normal | 10:00 | 09:25 | P059 | Vera Lúcia Fagundes | Centro | Bela Vista | 6.3 | App/Táxi | 25 min |
| 16/09 (qua) | Normal | 10:00 | 09:28 | P059 | Vera Lúcia Fagundes | Centro | Bela Vista | 6.3 | App/Táxi | 22 min |
| 16/09 (qua) | Normal | 10:00 | 09:22 | P070 | Marcelo Tanaka Ishida | Centro | Liberdade | 4.2 | Ônibus | 28 min |
| 16/09 (qua) | Normal | 10:00 | 08:04 | P043 | Elaine Cristina Sobral | Zona Leste | Vila Prudente | 21.1 | Ônibus | 106 min |
| 16/09 (qua) | Normal | 10:00 | 08:53 | P064 | Everton Lisboa Caldeira | Zona Oeste | Pompeia | 11.5 | Ônibus | 57 min |
| 16/09 (qua) | Normal | 10:00 | 09:06 | P073 | Heloísa Marques Teles | Zona Oeste | Perdizes | 7.9 | Ônibus | 44 min |
| 16/09 (qua) | Normal | 10:00 | 09:12 | P042 | Vinícius Rangel Prates | Zona Sul | Vila Mariana | 14.5 | Carro próprio | 38 min |
| 16/09 (qua) | Normal | 11:00 | 10:13 | P061 | Amanda Peixoto Furtado | Zona Oeste | Perdizes | 12.6 | App/Táxi | 37 min |
| 16/09 (qua) | Normal | 11:00 | 10:24 | P058 | Anderson Muniz Trajano | Zona Sul | Brooklin | 4.3 | Ônibus | 26 min |
| 16/09 (qua) | Normal | 12:00 | 11:37 | P056 | Jorge Amaral Bittar | Centro | Vila Buarque | 4.9 | Carro próprio | 13 min |
| 16/09 (qua) | Normal | 12:00 | 11:12 | P007 | Luciana Bezerra Pinto | Zona Leste | Vila Industrial | 15.0 | Carro próprio | 38 min |
| 16/09 (qua) | Normal | 12:00 | 11:30 | P013 | Camila Rocha Bittencourt | Zona Oeste | Vila Madalena | 7.9 | Carro próprio | 20 min |
| 16/09 (qua) | Normal | 13:00 | 12:32 | P062 | Cláudio Menezes Arruda | Zona Oeste | Cerqueira César | 6.6 | Carro próprio | 18 min |
| 16/09 (qua) | Normal | 14:00 | 12:09 | P010 | Antônio Carlos Siqueira | Grande SP | Vila Assunção | 22.5 | Ônibus | 101 min |
| 16/09 (qua) | Normal | 14:00 | 13:10 | P067 | Jéssica Alvarenga Pontes | Zona Leste | Belenzinho | 13.6 | App/Táxi | 40 min |
| 16/09 (qua) | Normal | 15:00 | 14:26 | P044 | Márcio Toledo Ferraz | Zona Sul | Santo Amaro | 9.1 | Carro próprio | 24 min |
| 17/09 (qui) | Normal | 07:00 | 06:22 | P066 | Osvaldo Pinheiro Rocha | Zona Sul | Vila Mariana | 5.8 | Metrô/Trem | 28 min |
| 17/09 (qui) | Normal | 08:00 | 06:32 | P028 | Wagner Souza Peixoto | Zona Leste | São Miguel Paulista | 22.8 | App/Táxi | 78 min |
| 17/09 (qui) | Normal | 09:00 | 08:09 | P036 | Alexandre Duarte Peçanha | Zona Oeste | Lapa | 12.5 | Metrô/Trem | 41 min |
| 17/09 (qui) | Normal | 09:00 | 08:35 | P017 | Beatriz Sampaio Correia | Zona Sul | Vila Mariana | 4.9 | Carro próprio | 15 min |
| 17/09 (qui) | Normal | 09:00 | 08:06 | P024 | Thiago Barbosa Leal | Zona Sul | Paraíso | 14.0 | Carro próprio | 44 min |
| 17/09 (qui) | Normal | 10:00 | 09:03 | P052 | Alan Ferraz Modesto | Zona Leste | Anália Franco | 16.0 | App/Táxi | 47 min |
| 17/09 (qui) | Normal | 10:00 | 09:33 | P004 | João Pedro Vasconcelos | Zona Oeste | Pompeia | 6.2 | Carro próprio | 17 min |
| 17/09 (qui) | Normal | 10:00 | 09:27 | P015 | Vanessa Lima Cordeiro | Zona Oeste | Perdizes | 8.6 | Carro próprio | 23 min |
| 17/09 (qui) | Normal | 10:00 | 09:12 | P024 | Thiago Barbosa Leal | Zona Sul | Paraíso | 14.0 | Carro próprio | 38 min |
| 17/09 (qui) | Normal | 11:00 | 10:05 | P052 | Alan Ferraz Modesto | Zona Leste | Anália Franco | 16.0 | Carro próprio | 45 min |
| 17/09 (qui) | Normal | 11:00 | 09:49 | P014 | Sérgio Nunes Barreto | Zona Leste | Brás | 19.3 | Metrô/Trem | 61 min |
| 17/09 (qui) | Normal | 11:00 | 10:33 | P033 | Simone Aparecida Rocha | Zona Sul | Jardim Míriam | 6.2 | Carro próprio | 17 min |
| 17/09 (qui) | Normal | 11:00 | 10:19 | P019 | Rosana Teixeira Amaral | Zona Sul | Saúde | 8.9 | Metrô/Trem | 31 min |
| 17/09 (qui) | Normal | 12:00 | 10:56 | P054 | Douglas Serrano Pimenta | Zona Leste | Tatuapé | 20.4 | Carro próprio | 54 min |
| 18/09 (sex) | INTENSO | 08:00 | 06:57 | P077 | Nádia Cristina Bonfim | Zona Leste | Vila Gomes Cardim | 15.3 | Metrô/Trem | 53 min |
| 18/09 (sex) | INTENSO | 08:00 | 07:07 | P022 | Gustavo Nascimento Reis | Zona Oeste | Lapa | 10.8 | Carro próprio | 43 min |
| 18/09 (sex) | INTENSO | 08:00 | 06:44 | P075 | Elisa Fontoura Barros | Zona Oeste | Jardim América | 9.8 | Ônibus | 66 min |
| 18/09 (sex) | INTENSO | 08:00 | 07:19 | P023 | Sandra Regina Oliveira | Zona Sul | Jardim Prudência | 6.6 | Metrô/Trem | 31 min |
| 18/09 (sex) | INTENSO | 08:00 | 07:07 | P002 | Carlos Eduardo Ramalho | Zona Sul | Vila Emir | 11.0 | Metrô/Trem | 43 min |
| 18/09 (sex) | INTENSO | 09:00 | 06:48 | P018 | Paulo Henrique Braga | Grande SP | Vila Augusta | 17.7 | Ônibus | 122 min |
| 18/09 (sex) | INTENSO | 09:00 | 08:07 | P005 | Mariana Tavares Duarte | Zona Oeste | Pinheiros | 10.9 | Carro próprio | 43 min |
| 18/09 (sex) | INTENSO | 09:00 | 08:12 | P071 | Regina Célia Nunes | Zona Oeste | Vila Romana | 8.4 | App/Táxi | 38 min |
| 18/09 (sex) | INTENSO | 09:00 | 07:48 | P063 | Talita Gonçalves Serra | Zona Sul | Chácara Santo Antônio | 8.8 | Ônibus | 62 min |
| 18/09 (sex) | INTENSO | 10:00 | 09:28 | P016 | Diego Fontanella Cruz | Centro | Centro | 6.1 | Carro próprio | 22 min |
| 18/09 (sex) | INTENSO | 10:00 | 08:05 | P051 | Karina Duarte Sarmento | Zona Leste | Vila Gomes Cardim | 17.5 | Ônibus | 105 min |
| 18/09 (sex) | INTENSO | 10:00 | 08:56 | P013 | Camila Rocha Bittencourt | Zona Oeste | Vila Madalena | 7.9 | Ônibus | 54 min |
| 18/09 (sex) | INTENSO | 13:00 | 12:32 | P006 | Roberto Kimura Sato | Centro | Liberdade | 5.1 | Carro próprio | 18 min |
| 18/09 (sex) | INTENSO | 13:00 | 12:06 | P021 | Aline Prado Guimarães | Zona Norte | Santana | 10.3 | App/Táxi | 44 min |
| 18/09 (sex) | INTENSO | 13:00 | 12:11 | P027 | Larissa Antunes Coelho | Zona Oeste | Pinheiros | 11.3 | Carro próprio | 39 min |
| 18/09 (sex) | INTENSO | 14:00 | 12:56 | P078 | Sidney Rabelo Pontes | Zona Leste | Tatuapé | 15.5 | Metrô/Trem | 54 min |

## 6. Saídas críticas (antes das 06h00)

| Dia | Consulta | Sair às | Paciente | Zona | Modal | Tempo |
|-----|----------|---------|----------|------|-------|-------|
| 16/09 (qua) | 08:00 | 05:50 | Wagner Souza Peixoto | Zona Leste | Ônibus | 120 min |

1 paciente(s) precisariam sair antes das 06h para chegar no horário — candidatos naturais a falta ou remarcação.

## 7. Leitura dos números

- **Segunda e sexta custam 28% mais tempo de deslocamento** que os dias normais: 50 min contra 39 min de média.
- **A matriz por zona é ruidosa** em zonas com poucos pacientes (Norte, Grande SP, Leste). Para análise por zona, a base precisa de mais volume.
- O efeito não é uniforme: quem usa **metrô/trem quase não sente** o dia intenso (sensibilidade 0,12), enquanto **ônibus e carro absorvem o congestionamento inteiro**. A zona pesa menos que o modal.
- **Zona Leste e Grande SP** são as origens mais caras em tempo, e concentram justamente os deslocamentos de ônibus mais longos.
- O choque relevante é que os **picos de atendimento caem em segunda e sexta, que são também os dias de trânsito intenso**. A clínica está concentrando volume exatamente quando o paciente tem mais dificuldade de chegar — terça, o dia mais fácil de deslocamento, é o dia ocioso da agenda.