# Proposta de Arquitetura e Aplicação de Padrões

## Proposta de Arquitetura (Parte 8)
Proponho uma arquitetura baseada em **Camadas (MVC)** aliada a uma comunicação via API:
* **View (Frontend):** Responsável apenas por renderizar o cardápio e capturar as interações do usuário. Pode ser construída com React ou Vue.js.
* **Controller (Backend/API):** Intermedia as chamadas, processando regras como "se pedir meia pizza, cobrar pelo sabor mais caro".
* **Model (Banco de Dados):** Gerencia as persistências de dados (Produtos, Categorias, Pedidos, Clientes).

## Aplicação de Padrões (Parte 9)
* **Padrão Factory:** Seria aplicado no Backend para instanciar objetos variados. Ao invés de usar `new Pizza()` ou `new Lanche()` espalhados pelo código, uma `ItemFactory.criar(tipo, detalhes)` centraliza a criação, garantindo que uma pizza de 2 sabores receba o cálculo correto de preço antes de ir pro carrinho.
* **Padrão Singleton:** Seria aplicado no Frontend (estado da aplicação) para gerenciar o `PedidoManager`. Garante que haja apenas uma instância ativa do pedido do cliente durante toda a navegação, evitando que o estado seja perdido ao trocar de página no cardápio.