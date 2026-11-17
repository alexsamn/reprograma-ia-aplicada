## IA na Rotina — Automação Inteligente

Uma automação sem código que lê os e-mails de candidatura a vagas e monta sozinha uma planilha de acompanhamento, usando IA para extrair empresa, cargo e data.

```
FICHA DO PROJETO ──────────────────────

Semana ...... 03
Módulo ...... IA na Rotina: Automação Inteligente
Tipo ........ Individual
Meu papel ... Desenho e montagem do fluxo de ponta a ponta
Ferramentas . Make · Gmail · Google Gemini · Google Sheets
Status ...... Concluído
```

### 1. Problema
Numa busca de vagas, os e-mails de confirmação e retorno de candidatura se misturam com o resto da caixa de entrada. Saber onde me candidatei, para qual cargo e quando exigia copiar tudo à mão para uma planilha.

### 2. Objetivo
Automatizar o registro das candidaturas sem escrever código.

> Se cada e-mail de candidatura virar uma linha na planilha automaticamente, então consigo acompanhar quantas candidaturas faço por semana, para quais empresas e há quanto tempo estou sem retorno, sem trabalho manual.

### 3. Processo
1. **Gatilho:** no Gmail, os e-mails de candidatura recebem a tag *Candidatura*.
2. **Leitura:** o Make observa os e-mails com essa tag (*Watch emails*).
3. **Extração com IA:** o Google Gemini lê o texto do e-mail e extrai **empresa**, **cargo** e **data** (*Extract structured data*).
4. **Registro:** o Google Sheets grava cada candidatura como uma nova linha (*Add a row*).

### 4. Decisões
| Decisão | Por quê |
|---|---|
| Colocar IA no meio do fluxo, e não só copiar campos | Cada empresa e cada plataforma de vagas manda o e-mail num formato diferente. Remetente e assunto nem sempre dizem a empresa ou o cargo; o Gemini acha essas informações no texto livre |
| Filtrar pela tag do Gmail | A automação só lê os e-mails certos, sem processar a caixa inteira |
| Usar Make, sem código | Resolver o problema de verdade é mais importante que a tecnologia |

### 5. Resultado
⚙️ [Cenário da automação no Make (público)](https://us2.make.com/public/shared-scenario/xYeUr6R0E3J/integration-gmail-google-sheets)

![Fluxo da automação no Make: Gmail, Google Gemini AI e Google Sheets](./fluxo-make.png)

| Empresa | Cargo | Data |
|---------|-------|------|
| *extraída pelo Gemini* | *extraído pelo Gemini* | *extraída pelo Gemini* |

Uma planilha de candidaturas que se atualiza sozinha.

### 6. Aprendizados
- **O que funcionou:** usar a IA para **extrair dados**, não só para gerar texto. Ela transforma texto livre em colunas organizadas.
- **O que eu faria diferente:** incluir uma coluna de status (enviada, em processo, recusada) para a planilha medir o funil, não só registrar.
- **O que levo para os próximos projetos:** pensar sempre em gatilho → processamento → saída antes de escolher a ferramenta.

### 7. Próximos passos
- [ ] Adicionar status e data de retorno para acompanhar o funil de candidaturas
- [ ] Ligar à triagem de vagas desenhada na [S7](../S7-matriz-esforco-impacto/)

---

← [Voltar para todos os projetos](../README.md) · [Portfólio](https://www.alexsandramoura.com.br) · [LinkedIn](https://www.linkedin.com/in/alexsandramoura)
