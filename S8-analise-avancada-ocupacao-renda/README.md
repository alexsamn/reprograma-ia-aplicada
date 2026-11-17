<img width="1280" height="640" alt="capa" src="https://github.com/user-attachments/assets/2c0059e8-2636-4230-a817-216da14345c0" />

Uma análise em grupo de um dataset de pedidos de delivery: limpeza, cruzamento de ocupação com renda e recomendação estratégica para operação e marketing.

```
FICHA DO PROJETO ──────────────────────

Semana ...... 08
Módulo ...... Dados Avançado: De Bruto a Insight
Tipo ........ Em grupo (Alexsandra Moura, Karol de Castro e Rilza Boaventura)
Meu papel ... Integrante da equipe: diagnóstico, limpeza, análise e recomendação
Ferramentas . IA generativa · Excel / planilhas
Status ...... Concluído
```

### 1. Problema
Uma plataforma de delivery quer saber onde concentrar campanhas e operação. A pergunta do nosso grupo (tema 1, o mais avançado da turma): **o efeito da ocupação sobre o comportamento de pedido muda conforme a faixa de renda?** Para responder, é preciso cruzar duas variáveis, não só uma.

### 2. Objetivo
Entregar uma análise completa: dado preparado, padrão encontrado, visualização e recomendação estratégica para duas personas, apresentada em 5 minutos.

> Se entendermos como ocupação e renda se combinam, então as campanhas podem mirar o segmento certo, em vez de tratar todo cliente igual.

### 3. Processo
1. **Base:** dataset compartilhado da turma, com 388 linhas e 13 colunas (idade, gênero, estado civil, ocupação, renda, escolaridade, tamanho da família, tipo de cliente, localização, `Output` Yes/No e feedback). A renda está em rúpias, e os CEPs são de Bangalore, na Índia.
2. **Diagnóstico de qualidade** com IA.
3. **Limpeza** com prompts.
4. **Padrões:** taxa de `Output = Yes` por ocupação e faixa de renda.
5. **Visualização e recomendação** para as personas de operação (A) e de mercado (B).

| Problema | O que encontramos | Como resolvemos |
|----------|-------------------|-----------------|
| **Duplicatas** | 103 linhas duplicadas exatas (388 → 285) | Remoção com prompt, pedindo à IA que informasse o total removido |
| **Coluna fantasma** | Uma coluna idêntica a `Output`, criada por uma vírgula sobrando no fim do cabeçalho | Coluna removida |
| **Formato inconsistente** | `Monthly Income`, `Family size`, `latitude` e `Pin code`. A latitude virou data no Excel (ex.: `9766-12-01` no lugar de `12.9766`) | Padronização |
| **Erro de digitação** | `Self Employeed` | Correção |
| **Formatos misturados** | `Ph.D`; faixas de renda com e sem moeda (`Below Rs.10000` × `10001 to 25000`) | Padronização |
| **Tipo errado** | CEP salvo como número inteiro | Conversão para texto |

### 4. Decisões
| Decisão | Por quê |
|---|---|
| Remover as duplicatas antes de qualquer conta | 103 linhas são 27% da base e distorceriam todas as taxas |
| Mostrar o tamanho de cada grupo (n) no gráfico | Uma taxa de 100% com 1 pessoa não vale o mesmo que 86% com 122 |
| Tratar grupos com menos de 10 pessoas como leitura frágil | Cruzar duas variáveis multiplica os grupos e encolhe cada um |
| Recomendar a ação para empregados de renda baixa **como teste** | A faixa tem só 6 pessoas; não sustenta uma conclusão sozinha |

### 5. Resultado
![Taxa de Output = Yes por ocupação e faixa de renda](./grafico-ocupacao-renda.png)

*Gráfico refeito a partir do dataset sem duplicatas, com o tamanho de cada grupo (n) indicado.*

| Ocupação | Padrão | Solidez |
|----------|--------|---------|
| **Estudantes** | Taxa alta em qualquer faixa: 86% sem renda (105 de 122) e 80% a 100% nas faixas com renda | ✅ Sólido para "sem renda" (n=122). As faixas com renda têm de 1 a 13 pessoas |
| **Empregados** | Sobe de 33% (abaixo de Rs 10.000) para 76% (Rs 10.001–25.000) e fica entre 62% e 63% nas faixas mais altas | ⚠️ O patamar de 62% a 76% é sólido (n de 21 a 38). O "salto" a partir de 33% vem de **só 6 pessoas** |
| **Autônomos** | Estável entre 55% e 70% acima de Rs 10.000 | ✅ Moderado (n de 10 a 17) |
| **Donas de casa** | 78% (7 de 9), todas sem renda própria | ⚠️ Grupo pequeno |

**Leitura:** a ocupação pesa mais que a renda. Estudantes pedem muito mesmo sem renda própria.

**Recomendação estratégica:**
- **Estudantes:** apostar em frequência, não em poder de compra. Combos de baixo custo, entrega rápida, indicação (member-get-member) e programa de pontos.
- **Empregados com renda de Rs 10.001–25.000:** a faixa de maior resposta. Ofertas de conveniência para a rotina.
- **Empregados abaixo de Rs 10.000:** cupom de primeira compra e isenção de taxa de entrega, como teste.

| Persona | O que o achado significa |
|---------|--------------------------|
| **A · Operação e logística** | Estudantes geram volume constante, independentemente da renda. Vale cruzar ocupação com região para dimensionar a frota onde eles se concentram |
| **B · Mercado e produto** | Segmentar por ocupação antes de segmentar por renda: combos e fidelidade para estudantes, ofertas de entrada para empregados de renda baixa |

### 6. Aprendizados
- **O que funcionou:** limpar antes de analisar. 80% do trabalho foi arrumar a base.
- **O que eu faria diferente:** conferir o gráfico gerado com IA contra os números da tabela antes de apresentar, e documentar o que `Output` mede antes de interpretar a coluna.
- **O que levo para os próximos projetos:** todo gráfico precisa mostrar o n. Explicações como "mesada" ou "rotina digital" são hipóteses, porque a base não tem esses dados.

### 7. Próximos passos
- [ ] Repetir a análise com uma amostra maior de empregados de renda baixa
- [ ] Cruzar ocupação com região para a recomendação de frota

---

← [Voltar para todos os projetos](../README.md) · [Portfólio](https://www.alexsandramoura.com.br) · [LinkedIn](https://www.linkedin.com/in/alexsandramoura)
