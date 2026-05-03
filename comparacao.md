# Comparação: Sistema Real vs. Sistema Didático

| Critério | Sistema Real (Tropykaly) | Sistema Didático (Pastelaria do Zé original) |
| :--- | :--- | :--- |
| **Arquitetura** | Cliente-Servidor (MVC ou API Rest) | Monolítica (Script Inline / Spaghetti) |
| **Coesão** | Alta (Módulos separam responsabilidades) | Baixa (Funções fazem múltiplas tarefas) |
| **Acoplamento** | Baixo (Comunicação via requisições/interfaces) | Alto (Regras de negócio atreladas ao DOM) |
| **Organização** | Estruturada em camadas lógicas e UI separada | Desorganizada (Variáveis globais, tudo no mesmo arquivo) |
| **Flexibilidade** | Alta (Fácil adicionar novas categorias/produtos) | Baixa (Preços hardcoded, difícil escalar) |

**Explicação das principais diferenças:**
O sistema real é projetado para escalabilidade. A separação em camadas permite que o frontend seja atualizado sem quebrar a lógica de precificação no backend. O sistema didático sofria de forte acoplamento, onde qualquer mudança na tela poderia quebrar o cálculo do valor final.