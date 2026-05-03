# Problemas Identificados e Melhorias

## Problemas Identificados (Inferidos do comportamento Web)
* **Dependência de Plataformas Terceiras:** Muitos sistemas desse tipo dependem do WhatsApp para finalizar a transação, o que impede automação total do fluxo de pagamento.
* **Sincronização de Estado:** Se a internet do usuário oscilar, o sistema pode perder os dados do carrinho se não houver uso adequado de `localStorage` ou banco de dados em tempo real.
* **Possível Acoplamento de UI em modais:** Formulários muito extensos para personalização de pizza podem tornar a tela confusa no mobile.

## Melhorias Propostas
1. Implementar checkout e pagamento online nativo (via PIX/Cartão integrados), reduzindo a fricção de enviar mensagem para atendente.
2. Uso de PWA (Progressive Web App) para permitir funcionamento offline parcial e carregamento mais rápido do cardápio.
3. Cacheamento de imagens estáticas (fotos dos lanches) via CDN para melhorar a performance.