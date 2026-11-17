<img width="1280" height="640" alt="capa" src="https://github.com/user-attachments/assets/13233e99-ed13-4f8f-a39f-4b6a10fe2775" />

Um glossário de Product Design para estudar por recuperação ativa, com interface de arquivo físico, banco de dados, área administrativa com login e deploy contínuo, construído com IA como par de programação.

```
FICHA DO PROJETO ──────────────────────

Semana ...... 12
Módulo ...... Vibe Coding
Tipo ........ Individual
Meu papel ... Produto, conteúdo, interface e desenvolvimento com IA
Ferramentas . Claude Code · Next.js · React · Tailwind · Supabase · Vercel
Status ...... Concluído
```

🔗 **[Acessar o site](https://arquivos-de-ux.vercel.app)** · **[Código no GitHub](https://github.com/alexsamn/arquivos-de-ux)**

### 1. Problema
Quem está entrando em Product Design precisa dominar muito vocabulário novo, e ler uma lista de definições não fixa nada. O jeito mais eficiente de estudar é tentar lembrar antes de conferir, e os glossários que existem são feitos para consulta, não para isso.

### 2. Objetivo
Tirar o glossário dos dados de exemplo e publicá-lo como produto de verdade: com banco de dados, área administrativa protegida por login e deploy contínuo.

> Se o glossário obrigar a tentar lembrar o termo antes de mostrar a definição, então o estudo deixa de ser leitura passiva e passa a mostrar o que eu já sei e o que preciso revisar.

### 3. Processo
A semana seguiu 4 fases, uma por aula, com o Claude Code como par de programação:

1. **Planejamento e interface:** plano faseado antes de qualquer código, revisado por um segundo modelo de IA no papel de consultor externo, e a interface funcionando localmente.
2. **Supabase e backend:** os termos saíram dos arquivos locais para uma tabela no banco.
3. **Melhoria contínua:** área `/admin` para criar, editar e apagar fichas sem mexer no código.
4. **Login e segurança:** Supabase Auth e Row Level Security. O glossário continua público, e só quem é admin escreve.

### 4. Decisões
| Decisão | Por quê |
|---|---|
| **Recuperação ativa como regra de interface:** a ficha só abre depois de escolher o termo, e os botões "Já sabia" e "Revisar depois" alimentam o progresso | A técnica de estudo virou comportamento da tela |
| **Interface de arquivo físico:** gaveteiro por letras, pastas e ficha que sobe | Dá um lugar na memória para cada termo, em vez de uma lista infinita |
| **Gavetas calculadas a partir dos dados** (letras vizinhas se juntam; nenhuma letra é dividida) | O gaveteiro se ajusta sozinho quando entram termos novos |
| **Proteção no banco, não na página** | Com RLS, qualquer pessoa lê, mas só a tabela `admins` escreve. Testei inserir um termo pela API sem login, e o banco recusou (HTTP 401). A página `/admin` sozinha não protege nada |
| **Manter o mesmo id dos termos na migração** | O progresso salvo no navegador usa esse id; trocar apagaria o que já tinha sido estudado |
| **Definições escritas do zero** a partir de nomes de termos de duas fontes (Silvestri e Google UX Design Certificate) | Evita copiar conteúdo e mantém um padrão de linguagem |
| **Acessibilidade:** contraste mínimo de 4,5:1, navegação por teclado e `prefers-reduced-motion` | Um glossário de UX precisa praticar o que ensina |

### 5. Resultado
- **164 termos** em 7 categorias: Pesquisa, Arquitetura da Informação, Interação, Prototipação, Estratégia, Times & Métodos e Design Visual
- **Busca instantânea** no nome, nos sinônimos (inglês, siglas, variações) e na definição
- **Filtros por categoria** e **progresso de estudo** (vistos e para revisar), com "Revisar N" virando filtro
- **Área administrativa** em `/admin`, protegida por login
- **Deploy automático** na Vercel a cada push

Detalhes técnicos, estrutura de pastas e como rodar o projeto estão no [README do repositório](https://github.com/alexsamn/arquivos-de-ux).

### 6. Aprendizados
- **O que funcionou:** planejar em fases antes de escrever código, e pedir para outro modelo de IA revisar o plano antes de executar.
- **O que eu faria diferente:** criar um único projeto no Supabase e na Vercel desde o início. O erro que mais demorou foi o site publicado abrir sem nenhum termo: havia dois projetos com o mesmo nome no Supabase e dois ligados ao repositório na Vercel, e as variáveis de ambiente estavam no projeto errado.
- **O que levo para os próximos projetos:** segurança fica no banco, não na tela. E a chave publicável pode ficar exposta (a Vercel nem aceita variáveis `NEXT_PUBLIC_` como segredo); quem barra a escrita é o RLS.

### 7. Próximos passos
- [ ] Integrar os 125 termos novos já escritos e juntar os sinônimos dos termos repetidos
- [ ] Corrigir o endereço de clone no README do repositório (`alexsamoura` → `alexsamn`)

---

← [Voltar para todos os projetos](../README.md) · [Portfólio](https://www.alexsandramoura.com.br) · [LinkedIn](https://www.linkedin.com/in/alexsandramoura)
