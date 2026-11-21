# Meu_Site

Regras gerais de trabalho vêm do `CLAUDE.md` global do usuário.

## Produto e stack
- Site de atividade do Módulo 9 do Conecta Jovem (`README.md`): página inicial e um resumidor de textos com IA. Não há `PRODUCT.md` nem `docs/`.
- Stack: HTML com JavaScript no navegador (`index.html`, `ia.html`); funções na nuvem em `api/*.js` (módulos ES, `export default { fetch }`, hospedadas na Vercel); scripts Python de estudo só com biblioteca padrão (`ia.py`, `ia_json.py`, `agente.py`, `rag.py`, `playground.py`). Modelo de IA via API da Cloudflare.
- Sem dependências: `package.json` só declara `"type": "module"`.
- Variáveis de ambiente (nomes, sem valores): `AI_GATEWAY_API_KEY` (chave da IA), `NOME_DA_TURMA` (opcional, usada em `api/ola.js`). Os scripts Python pedem a chave no terminal se ela não existir.

## Comandos canônicos
- Instalar, lint, formatar, tipos, build: não se aplica: não há configurados.
- Desenvolver: não há comando definido; as páginas chamam `/api/*`, então só funcionam completas na Vercel.
- Scripts Python: `python3 <arquivo>.py` (ex.: `python3 ia.py`).
- Testes: não há testes automatizados.
- Verificação: não há comando. Confira à mão: a página afetada no navegador e, para scripts Python, uma execução real, sem inventar o resultado.

## Mapa de documentação
- Descrição: `README.md`. Não há outros documentos.

## Convenções do projeto
- Nomes e textos do código em português (como já está nos arquivos), com comentários curtos explicando cada passo.
- `api/ia.js` limita o texto a 2000 caracteres e isola o texto do usuário entre `<texto>` e `</texto>`; mantenha as duas proteções.
