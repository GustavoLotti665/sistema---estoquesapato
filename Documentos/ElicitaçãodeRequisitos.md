# 📋 Artefato 2: Documento de Elicitação de Requisitos (Perguntas e Respostas)

Este documento mostra o que foi conversado com o pessoal da loja para entender o que o sistema realmente precisa fazer.

---

### 🔍 1. O Problema
* **Pergunta:** O que mais atrapalha na hora de enviar o produto para o cliente?
* **Resposta:** O cliente compra uma cor ou tamanho no site e, quando vamos ver, o fornecedor não tem essa grade pronta. Isso atrasa a entrega e gera cancelamentos.

---

### 🔄 2. O Motivo do Erro
* **Pergunta:** Por que o site fica desatualizado com o que o fornecedor tem?
* **Resposta:** Porque eles mandam planilhas de estoque só uma vez por semana. Nesse meio tempo, o site continua vendendo coisas que já acabaram na fábrica.

---

### 💾 3. O que o Sistema precisa Salvar
* **Pergunta:** O que não pode faltar no banco de dados para resolver isso?
* **Resposta:** Precisamos cadastrar os sapatos detalhando bem o modelo, a marca, a cor exata e o tamanho (do 34 ao 44). Também ajuda marcar o prazo de entrega de cada marca.

---

### 🚨 4. Como o Sistema deve Avisar o Erro
* **Pergunta:** O que o programa deve fazer quando notar que o produto está em falta no fornecedor?
* **Resposta:** Ele tem que mostrar um alerta vermelho bem chamativo na tela de pedidos, avisando o lojista do risco antes de começar a embalar.

---

### 👥 5. Quem vai Usar
* **Pergunta:** Quem vai mexer no sistema no dia a dia?
* **Resposta:** * 🛒 **Comprador:** Para atualizar o estoque que os fornecedores mandam.
  * 📦 **Pessoal do Estoque:** Para ver quais pedidos estão com o tamanho garantido e já podem ser despachados.

---

### 🎨 6. Visual das Telas
* **Pergunta:** Como o sistema deve ser visualmente?
* **Resposta:** Muito simples e direto. Quem trabalha no estoque precisa bater o olho na tela e entender o status do pedido em segundos, sem menus confusos.
