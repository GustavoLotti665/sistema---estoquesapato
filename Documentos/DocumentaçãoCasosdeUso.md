# 📝 Artefato 10: Especificação de Caso de Uso

Este documento explica passo a passo como funciona a ação mais importante do nosso sistema: garantir que o sapato vendido realmente existe no estoque da fábrica.

---

### 🔍 Detalhamento: Validar Estoque do Pedido

| O que é | Como funciona na prática |
| :--- | :--- |
| **Quem executa** | O Sistema (de forma automática). |
| **Quem é avisado** | O Administrador da loja. |
| **Resumo** | O sistema pega o pedido que acabou de cair no site e cruza com a tabela do fornecedor para evitar furos de estoque. |
| **O que precisa acontecer antes** | 1. O cliente fechou e pagou a compra.<br>2. A tabela do fornecedor já está no nosso banco de dados. |
| **Como termina** | O pedido é liberado para envio **OU** fica travado esperando o lojista resolver. |

---

### 🟢 O Caminho Ideal (Quando tem estoque)

Aqui é o cenário perfeito, quando o fornecedor tem o sapato para entregar.

1. Cai um pedido novo no e-commerce.
2. O sistema verifica qual é o modelo, a cor e o tamanho exato.
3. Ele consulta a lista do fornecedor no banco de dados.
4. Ele confirma que o fornecedor tem aquela numeração disponível.
5. O sistema muda o status da venda para "Pronto para Embalar".
6. Fim do processo. Tudo certo.

---

### 🔴 O Tratamento de Erro (Quando falta na fábrica)

Aqui é quando a numeração esgotou na fábrica ou o fornecedor cortou o modelo de surpresa.

1. Cai um pedido novo no e-commerce.
2. O sistema verifica qual é o modelo, a cor e o tamanho exato.
3. Ele consulta a lista do fornecedor no banco de dados.
4. **O problema:** Ele descobre que o fornecedor zerou o estoque daquele tamanho.
5. O sistema trava a venda na hora para evitar a emissão de nota fiscal errada.
6. Ele acende um **Alerta Vermelho** no painel do administrador.
7. O processo automático para por aqui, aguardando o lojista tomar uma decisão (como ligar para o cliente para trocar a cor ou estornar).
