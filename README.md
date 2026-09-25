# Hora Santa — primeira sexta-feira

Folhetos e organização da Hora Santa mensal do grupo do Sagrado Coração de Jesus da
**Paróquia Santo Antonio de Uberaba — Curitiba, PR**, preparados a partir do livro
[*No Coração de Jesus*](https://magoja-br.github.io/no-coracao-de-jesus/).

**Site:** https://magoja-br.github.io/hora_santa/

## O que tem aqui

| Pasta / arquivo | Conteúdo |
|---|---|
| `index.html` | página inicial: próximas datas e todos os folhetos |
| `recursos.md` → `recursos.html` | funções da equipe, normas, checklist mensal, links do livro |
| `AAAA-MM-DD/` | um mês: `folheto` (fiéis) e `organizacao` (equipe), em `.md`, `.html` e `.pdf` A5 |
| `ferramentas/gerar_folheto.py` | gera HTML + PDF a partir dos `.md` |
| `ferramentas/folheto.css` | aparência (tela, celular e impressão A5) |
| `ferramentas/modelo/` | modelo de folheto e de organização para copiar |

## Como fazer o folheto de um novo mês

1. Copie `ferramentas/modelo/*.md` para uma pasta nova com a data, ex. `2026-11-06/`.
2. Edite o tema, o Evangelho em 4 momentos, a intenção do Papa, as preces e as datas.
3. Gere o site e os PDFs (precisa de Python com `markdown` e do Edge ou Chrome instalado):

   ```bash
   python ferramentas/gerar_folheto.py 2026-11-06
   ```

4. Publique:

   ```bash
   git add -A && git commit -m "Hora Santa de novembro" && git push
   ```

No Claude, basta pedir "prepare a próxima Hora Santa" (skill `hora-santa-primeira-sexta`).

## Convenções do texto

```
## 18h30 · Exposição     título com selo de horário
! texto                   rubrica (instrução em vermelho)
A. / L. / M. / P.         Animador, Leitor, Ministro, Presidente
T. / R.                   resposta de todos (negrito)
> [!Oração] Título        oração em caixa
> [!Nota] Título          caixa de aviso
- [ ] item                caixa de seleção
```
