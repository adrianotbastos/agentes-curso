---
name: radar
description: Roda o radar do dia com o time de agentes, na ordem pesquisador, verificador, redator, guarda (e o agente do dono, se existir), e depois grava o dia no repositório com um commit. Use quando alguém pedir para rodar o radar ou quando a rotina das 7h disparar.
---

# Radar do dia

Você coordena o time do radar. Você não pesquisa, não escreve e não confere no lugar dos agentes: aciona cada um, confere o que ele entregou e só então passa para a próxima etapa.

Siga as etapas nesta ordem, uma por vez, sem pular nenhuma. Antes de começar, leia `CLAUDE.md` e `RADAR.md` e descubra a data de hoje (AAAA-MM-DD). Ela vale para todos os arquivos desta rodada.

Para acionar um agente, use a ferramenta Agent com `subagent_type` igual ao nome dele (por exemplo, `pesquisador`) e diga no pedido a data de hoje.

## 1. Pesquisador
Acione o `pesquisador`. Depois confira que `fontes/AAAA-MM-DD.md` existe e tem pelo menos três itens.
- Se tiver menos de três, ou se não houver nada novo, anote isso e siga mesmo assim.

## 2. Verificador
Acione o `verificador`. Depois confira que `verificacao/AAAA-MM-DD.md` existe e tem a tabela e a contagem no fim. Guarde a contagem de CONFERE.

## 3. Redator
Acione o `redator`. Depois confira que `diario/AAAA-MM-DD.md` existe e que `index.html` foi gerado com a data de hoje.
- Se o redator avisar que falta `modelo-index.html`, anote e siga: o guarda vai barrar.

## 4. Agentes do dono
Liste `.claude/agents/`. Todo agente além de `pesquisador`, `verificador`, `redator` e `guarda` é um agente do dono.
- Para cada um, acione-o e inclua o que ele devolver no fim de `diario/AAAA-MM-DD.md`, numa seção com o nome dele (`## Nome do agente`).
- **Exceção, o `comunicador`:** ele escreve o rascunho privado do post de LinkedIn e só trabalha depois do PODE PUBLICAR do guarda. Não o acione nesta etapa e não coloque o post no briefing. Ele roda na etapa 5.

## 5. Guarda
Acione o `guarda` e leia o relatório até a última linha.
- **NÃO PUBLIQUE:** pare aqui. Mostre o relatório inteiro, não faça commit e não acione o `comunicador`.
- **PODE PUBLICAR:** se o `comunicador` existir, acione-o agora e confira que `posts/AAAA-MM-DD.txt` foi gravado. Esse arquivo fica só no computador (`posts/` está no `.gitignore`) e nunca entra no briefing. Depois siga para a etapa 6.

## 6. Gravar no repositório
Só com PODE PUBLICAR:
1. `git add -A`
2. `git commit -m "radar de AAAA-MM-DD"`
3. Se houver remoto (`git remote` não vazio), `git push`.

Se o push falhar, diga o motivo exato que o git deu e pare. Não tente contornar: sem forçar o envio, sem trocar de remoto, sem mexer em credenciais. Se pedir login, avise o dono para fazer o login no navegador.

## 7. Relato final
Mostre, em poucas linhas:
- a primeira linha do briefing de hoje;
- quantos itens conferiram (CONFERE de quantos no total);
- quantos agentes rodaram e quais;
- se o commit e o push deram certo;
- se o post de LinkedIn foi gravado em `posts/AAAA-MM-DD.txt`.

## Nunca
- Enviar nada a ninguém além do commit e do push: nada de e-mail, mensagem ou publicação em rede social.
- Usar, pedir ou gravar chave ou senha.
- Pular uma etapa ou mudar a ordem.
- Fazer commit sem PODE PUBLICAR do guarda.
