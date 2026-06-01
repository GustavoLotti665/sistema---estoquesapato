# 📄 Artefato 6: Documentação de Requisitos

Este documento lista as funções que o sistema deve ter (Requisitos Funcionais) e as tecnologias e regras visuais utilizadas (Requisitos Não Funcionais).

---

### ⚙️ 1. Requisitos Funcionais (RF)

| Código | O que o sistema deve fazer | Prioridade |
| :--- | :--- | :--- |
| **RF01** | **Cadastrar** os calçados detalhando marca, modelo, cor e numeração (grade do 34 ao 44). | Alta |
| **RF02** | **Importar** os dados de estoque e os prazos enviados pelos fornecedores. | Alta |
| **RF03** | **Bloquear** o pedido automaticamente se a numeração comprada não tiver no fabricante. | Alta |
| **RF04** | **Mostrar** um Alerta Vermelho na tela do administrador para pedidos com risco de atraso. | Alta |
| **RF05** | **Atualizar** o status para "Pronto para Embalar" assim que a grade for aprovada. | Média |

---

### 🛠️ 2. Requisitos Não Funcionais (RNF)

| Código | Como o sistema será construído | Tipo |
| :--- | :--- | :--- |
| **RNF01** | **Construir** o backend utilizando C# e ASP.NET Core. | Tecnologia |
| **RNF02** | **Salvar** as informações em um banco de dados SQL Server. | Banco de Dados |
| **RNF03** | **Criar** uma interface limpa (Clean UI) para o operador ver os alertas em até 3 segundos. | Usabilidade |
| **RNF04** | **Rodar** o sistema direto no navegador web de computadores ou tablets do estoque. | Portabilidade |
