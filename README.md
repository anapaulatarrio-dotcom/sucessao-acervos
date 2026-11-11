# Sucessão de Acervos TJPA

Aplicação estática (GitHub Pages) para localizar o responsável atual pelo acervo de um
desembargador do TJPA a partir do relator e do ano da última decisão.

## Arquivos
- `index.html` — aplicação completa (motor de sucessão, consulta, ficha, composição, pendências, edição).
- `dados.js` — fonte de dados: órgãos, tipos de evento, magistrados, acervos e eventos (uma linha por portaria).
- `gerar_dados.py` — script que gerou o `dados.js` inicial a partir da planilha; não é necessário para o funcionamento.
- `eventos_para_validacao.xlsx` — mesma base em Excel, com as pendências marcadas em amarelo.

## Publicação
1. Crie um repositório e envie `index.html` e `dados.js` para a raiz (ou para `/docs`).
2. Em Settings → Pages, aponte para a branch e pasta escolhidas.

## Atualização dos dados
Na aba **Edição** da aplicação, inclua ou corrija eventos e clique em **Baixar dados.js**.
Substitua o arquivo no repositório. Nenhuma alteração em código é necessária.

## Modelo de dados
Cada **acervo** nasce num provimento originário e muda de responsável ou de órgão por eventos:
ORIG, ASSUME (remanescente), CONV/CESSA (convocação), LEVA (art. 114, I), DEIXA (art. 114, II),
APOS, FALEC, SAIDA, REDIST (sorteio entre membros), VAGA (vaga transferida), EQUAL e PARCIAL (alertas).
