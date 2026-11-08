# Desenvolvimento

MVP estático em HTML, CSS e JavaScript, sem dependências externas ou credenciais. Requer Python 3 para servir os arquivos; Node.js permite verificar a sintaxe de JavaScript.

Use o checkout existente em `/workspace/ZEUS-STORE`. Cada tarefa na nuvem já é isolada; não crie um Git worktree sem solicitação explícita.

## Iniciar

```bash
cd /workspace/ZEUS-STORE
node --check app.js
python3 -m http.server 3000 --bind 0.0.0.0
```

O servidor precisa ser reiniciado em novas sessões. Não há etapa de build. Para hospedagem estática, publique index.html, style.css, app.js e assets/.

## Funcionalidades

- Oito roupas de exemplo com ilustrações SVG locais, preços em BRL e categorias.
- Busca por nome/cor, filtro de categoria e ordenação de preço.
- Detalhes, seleção de tamanho e carrinho com limite de 10 unidades por item/tamanho.
- Carrinho persistido no localStorage (`zeus-cart`), alteração de quantidade e remoção.
- Frete demonstrativo de R$ 19,90, gratuito a partir de R$ 299.
- Checkout demonstrativo com validação de nome, e-mail e formato de CEP.
- Confirmação de pedido fictício; nenhum pagamento, envio, e-mail ou armazenamento dos dados do formulário.

## Validação

Verificação de sintaxe e testes automatizados no Chromium/Playwright passaram em 2026-11-08: catálogo, busca, filtros, tamanhos, persistência após recarregar, quantidade, frete grátis, checkout, busca vazia e ausência de rolagem horizontal em tela de 390 px. Nenhum erro de execução no navegador foi observado.

Para conferir manualmente: selecione uma peça, escolha um tamanho, adicione à sacola, recarregue, ajuste as quantidades e conclua com dados fictícios. Verifique também a remoção e os resultados vazios da busca.

## Limites

Catálogo e estoque são exemplos. Não há backend, autenticação, cálculo real de frete, pagamentos ou pedidos duráveis. Preços e totais no navegador não são adequados para transações reais.

As instruções de instalação/inicialização foram preparadas, mas a plataforma não confirmou a gravação no rascunho do ambiente durante esta sessão. Este arquivo preserva os comandos para reutilização; a publicação do ambiente não foi realizada.
