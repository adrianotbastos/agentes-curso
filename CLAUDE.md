# CLAUDE.md: memória do projeto Meu Radar

## O que é este projeto
Um time de agentes que pesquisa a internet todo dia sobre **mercado financeiro e economia no Brasil e no mundo, com um bloco sobre IA no setor financeiro**, e entrega um briefing diário. A definição completa do radar está em `RADAR.md`. Ela é a fonte da verdade: em caso de dúvida, siga `RADAR.md`.

## Para quem é
Um profissional do mercado financeiro que usa o briefing para:
- elaborar análises sucintas (quantitativas e qualitativas) do contexto econômico e do impacto em produtos de investimento;
- acompanhar como a IA está mudando o setor financeiro e se preparar para implantar soluções de IA no trabalho.

## Resumo do radar
- **Assunto:** mercado, economia (Brasil e mundo) e IA no setor financeiro, mais um resumo curto de IA em outras áreas
- **Fontes principais:** Banco Central do Brasil, Valor Econômico, Reuters. Apoio para IA: MIT Technology Review
- **Primeira linha:** fato mais importante do dia + impacto nos investimentos + urgência para hoje (ou "sem urgências")
- **Quantidade:** 7 notícias
- **Tom:** explicativo (fato, porquê, o que muda)

## Fica de fora
Cripto especulativa; política partidária sem efeito em juros, fiscal ou câmbio; notícia de empresa isolada sem efeito no mercado; previsões sem dado.

## O radar nunca
- dá opinião como se fosse fato;
- traz fofoca;
- cita rede social sem fonte;
- fala da vida pessoal de pessoas;
- usa notícia velha como se fosse nova;
- inventa números;
- apresenta recomendação de investimento como se fosse dele (sempre atribui a quem recomendou).

## Regras técnicas
1. **Toda afirmação tem link.** Todo fato e todo número no briefing têm link para a fonte original. Sem link, não entra.
2. **Data conferida.** Só entram notícias das últimas 24 a 48 horas. Sempre mostre a data da publicação.
3. **Números não são inventados nem arredondados por conta própria.** Copie o número como está na fonte. Se houver divergência entre fontes, mostre as duas.
4. **Separar fato de opinião.** Opinião ou projeção de analista vem marcada como tal e com o nome de quem disse ("segundo [instituição]...").
5. **Sem dados pessoais.** Nunca registre nem use dados pessoais do usuário (nome de clientes, empresa, salário, endereço), mesmo que apareçam por acidente em uma conversa.
6. **Cabe em uma página.** Se passar, corte as notícias menos relevantes, nunca a primeira linha.
7. **Formato de saída:** um arquivo Markdown por dia em `diario/AAAA-MM-DD.md` e a página `index.html`. Anotações brutas em `fontes/`, conferência em `verificacao/`.
8. **Ordem do time:** pesquisador → verificador → redator → guarda → comunicador. Só publica com PODE PUBLICAR do guarda. O comunicador grava o post de LinkedIn em `posts/AAAA-MM-DD.txt` e nunca publica: o autor revisa e posta.
9. **Checklist antes de entregar:** rode os itens da seção "Observáveis" do `RADAR.md`. Se algum falhar, corrija antes de entregar.
10. **Idioma:** português do Brasil.
