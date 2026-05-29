# 👤 Artefato 8: Diagrama de Casos de Uso (UML)

Este documento mapeia visualmente os atores do sistema e as ações que eles podem realizar, detalhando as interações e as validações automáticas de estoque.

---

### 🎭 1. Atores (Quem usa o sistema)

* 👨‍💻 **Administrador:** O funcionário que opera o painel para gerenciar produtos e despachar as vendas.
* 🤖 **Sistema do Fornecedor:** O sistema externo que fornece os dados da fábrica.

---

### ⚙️ 2. Casos de Uso (As ações)

* **Ações do Administrador:** Cadastrar Produto, Gerenciar Pedidos, Liberar Envio.
* **Ações do Sistema:** Importar Estoque, Validar Estoque do Pedido, Gerar Alerta de Falta.

---

### 🗺️ 3. Diagrama Visual (UML)

```mermaid
flowchart LR
    %% Estilo dos Atores
    classDef ator fill:transparent,stroke:none,color:#fff,font-size:14px,font-weight:bold;
    
    %% Estilo dos Casos de Uso
    classDef casoUso fill:#34495e,stroke:#2c3e50,stroke-width:2px,color:#fff,rx:20,ry:20;
    
    %% Atores
    Admin((👨‍💻 Administrador)):::ator
    Forn((🤖 Sistema<br>Fornecedor)):::ator

    %% Fronteira do Sistema
    subgraph Sistema [Fronteira do Sistema de Gestão]
        direction TB
        UC1([➕ Cadastrar Produto]):::casoUso
        UC2([📦 Gerenciar Pedidos]):::casoUso
        UC3([✅ Liberar Envio]):::casoUso
        UC4([🔄 Importar Estoque]):::casoUso
        UC5([🔍 Validar Estoque do Pedido]):::casoUso
        UC6([🚨 Gerar Alerta de Falta]):::casoUso
    end

    %% Ligações dos Atores com os Casos de Uso
    Admin --- UC1
    Admin --- UC2
    Admin --- UC3
    
    Forn --- UC4

    %% Relações de Include e Extend
    UC2 -. "<< include >>" .-> UC5
    UC5 -. "<< extend >>\n(Se faltar na fábrica)" .-> UC6
