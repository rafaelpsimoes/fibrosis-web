# Fibrosis Staging Tool — Google Sites

Aplicação estática em HTML e JavaScript, com 10 classificadores originais e funções LDA exportadas. Os valores são processados localmente no navegador. A interface apresenta FIB-4 calculado pela fórmula convencional `AGE * AST / (PL * sqrt(ALT))`.

## Publicação
1. Crie um repositório público no GitHub.
2. Envie `index.html`, `app.js` e `models.json` à raiz da branch `main`.
3. Em **Settings → Pages**, escolha **Deploy from a branch**, `main`, `/ (root)`.
4. Aguarde a URL do GitHub Pages e abra-a para verificar o formulário e uma predição.
5. No Google Sites, selecione **Inserir → Incorporar → Por URL** e informe a URL do GitHub Pages. Ajuste a altura da incorporação e publique.

## Cálculo e inferência
O FIB-4 é calculado pela fórmula convencional `AGE * AST / (PL * sqrt(ALT))` tanto para exibição quanto para **todos os atributos de entrada** dos classificadores (`FIB4`, `FIB42`, `FIB4sqrt`) e para as funções discriminantes LDA que dependem deles. Os coeficientes LDA, os limiares e as estruturas das dez árvores exportadas permanecem inalterados; os modelos não são retreinados. Portanto, as predições podem diferir da versão que utilizava o FIB-4 invertido na inferência. Recomenda-se conferir a concordância com os resultados de referência antes da publicação.

A ferramenta é destinada a apoio à pesquisa, não a diagnóstico autônomo.

## Arquivos
- `index.html`: interface responsiva.
- `app.js`: lógica de inferência, cálculo FIB-4 convencional para exibição e regras.
- `models.json`: parâmetros das árvores e transformações LDA.

Não publique dados de pacientes ou credenciais no repositório.
