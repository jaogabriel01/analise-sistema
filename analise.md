# Análise do Sistema Real

## Parte 1 - Análise do Sistema
1. **Qual é o objetivo do sistema?** Funcionar como um cardápio digital e sistema de delivery (Ponto de Venda Online), permitindo que clientes visualizem produtos e façam pedidos à distância.
2. **Quais funcionalidades ele oferece?** Navegação por categorias, personalização de produtos (ex: escolha de sabores e bordas para pizzas), adição de itens ao carrinho, cálculo de taxas de entrega e finalização do pedido (frequentemente integrando com WhatsApp ou painel próprio).
3. **Como o usuário interage com o sistema?** Através de uma interface gráfica web (responsiva para mobile), clicando em categorias, selecionando opções via formulários (botões de rádio/checkboxes) e visualizando um resumo interativo do carrinho.
4. **Como os produtos estão organizados?** Estão divididos em categorias claras (ex: Pizzas Tradicionais, Pizzas Especiais, Lanches, Bebidas) para facilitar a navegação.

## Parte 2 - Análise de Arquitetura
* **Tipo de Arquitetura:** Cliente-Servidor. O navegador do usuário (Client) faz requisições para o servidor onde o sistema está hospedado.
* **Divisão em Camadas:** É possível inferir uma divisão clara entre Frontend (Interface de Usuário) e Backend (Regras de Negócio e Banco de Dados). 
* **Separação de Responsabilidades:** Sim, diferente de um script único, o sistema consome dados dinamicamente (provavelmente via API), separando o que é exibição do que é processamento de dados.

## Parte 3 - Análise de Design
* **Coesão:** Alta. Componentes visuais (como o carrinho) têm funções específicas e bem delimitadas.
* **Acoplamento:** Baixo (inferido). Sendo um sistema moderno, o frontend interage com o backend via requisições, não dependendo de código misturado (HTML com regras de banco de dados).

## Parte 4 - Padrões de Projeto
1. **O sistema aparenta utilizar padrões?** Sim, sistemas complexos em produção costumam utilizar padrões para manter a manutenibilidade.
2. **Onde poderiam existir:**
   * **MVC:** Na estrutura geral do sistema, separando o Banco de Dados (Model), a Interface (View) e o Roteamento/Cálculos (Controller).
   * **Singleton:** No gerenciamento do "Carrinho de Compras" da sessão do usuário, garantindo que os itens adicionados em diferentes telas vão para o mesmo pedido.
   * **Factory:** Na criação de itens complexos, como uma "Pizza" (que precisa receber parâmetros como tamanho, múltiplos sabores, tipo de borda).

## Parte 10 - Reflexão Crítica
1. **É possível modelar um sistema sem ver o código?** Sim, através da engenharia reversa comportamental. Observando as entradas do usuário e as saídas do sistema, deduzimos as entidades e regras de negócio.
2. **Qual a importância da modelagem?** Ela permite visualizar a estrutura, facilitando a manutenção, evolução e compreensão do sistema por novos desenvolvedores antes de tocar no código.
3. **Diferença entre sistema real e didático:** O sistema real foca em escalabilidade, modularidade e tratamento de exceções, enquanto o didático (visto anteriormente) focava apenas em fazer funcionar, negligenciando padrões e segurança.