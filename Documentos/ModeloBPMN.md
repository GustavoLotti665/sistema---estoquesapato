# 🔄 Artefato 5: Modelo de Processo de Negócio (BPMN)

Este documento descreve o fluxo de trabalho atual da loja e como o novo sistema vai automatizar e corrigir o processo de venda e checagem de estoque.

---

### 📉 1. Processo Atual (As-Is) - Sem o Sistema

Hoje, o fluxo é manual, lento e passível de erros frequentes:

1. 🛒 **Cliente** acessa o e-commerce, escolhe o modelo/tamanho do calçado e finaliza a compra.
2. 🧾 **E-commerce** gera o pedido e envia para o painel de vendas.
3. 📦 **Funcionário do Estoque** recebe o pedido e vai até a prateleira buscar o produto.
4. ❌ **Se não houver a grade física:** O funcionário avisa o gerente, que precisa entrar em contato com o fornecedor.
5. 📅 **Gerente** consulta a última planilha semanal enviada pelo fabricante.
6. 💔 **Se o fornecedor também não tiver:** O gerente precisa ligar para o cliente para oferecer a troca por outra cor/modelo ou realizar o estorno do dinheiro.

---

### 📈 2. Processo Futuro (To-Be) - Com o Novo Sistema

Com o sistema em C#, o processo fica inteligente e previne o erro antes do envio:

1. 🛒 **Cliente** faz a compra de um calçado no site.
2. 🖥️ **Sistema** recebe o pedido e faz o cruzamento imediato com o banco de dados SQL Server (que já possui a disponibilidade atualizada dos fornecedores).
3. ⚡ **Validação Automática:**
   * 🟢 **Se o estoque estiver garantido:** O sistema libera o pedido automaticamente e o status muda para "Pronto para Embalar".
   * 🔴 **Se houver risco de falta na fábrica:** O sistema bloqueia o faturamento e gera um **Alerta Vermelho** na tela do administrador.
4. 📦 **Funcionário do Estoque** abre o painel limpo (desenhado no Figma), visualiza apenas os pedidos validados e faz a postagem rápida sem risco de erro.

---

### 🗺️ Elementos do Diagrama (Para desenhar no draw.io)

Para montar o seu gráfico no draw.io, utilize a seguinte estrutura:
* 🏢 **Pool/Lanes (Rias):** Divida o diagrama em 3 raias: `Cliente`, `E-commerce / Sistema` e `Fornecedor`.
* 🟢 **Evento de Início:** Pedido realizado pelo cliente.
* 🔶 **Gateway (Decisão):** Usar o losango de decisão para checar: *"Fornecedor possui a grade disponível?"*.
* 🔴 **Evento de Fim:** Pedido enviado com sucesso OU Pedido cancelado/estornado.
