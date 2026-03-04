📌 Caso de Uso 01 – Realizar Pedido com Múltiplos Vendedores

Nome:



Realizar pedido



Atores:



Ator Principal: Usuário (comprador)



Atores Secundários:



Usuários vendedores



Sistema de pagamento



Sistema de logística



Descrição:



Permite que um usuário selecione produtos de diferentes vendedores, confirme o pedido, realize o pagamento e inicie o processo de entrega.



Pré-condições:



Usuário autenticado.



Produtos cadastrados por vendedores.



Endereços cadastrados (comprador e vendedores).



Meio de pagamento válido.



Pós-condições (sucesso):



Pagamento confirmado.



Pedido registrado no sistema.



Processo de entrega iniciado.



Pós-condições (falha):



Pedido cancelado.



Pagamento não processado.



🔄 Fluxo Principal



O usuário acessa o catálogo.



O usuário seleciona produtos.



O usuário adiciona produtos ao carrinho (podendo ser de múltiplos vendedores).



O usuário revisa o carrinho.



O usuário confirma o pedido.



O sistema agrupa produtos por vendedor.



O sistema calcula valor total e frete.



O sistema calcula rota de coleta.



O sistema apresenta resumo final.



O usuário confirma pagamento.



O sistema processa pagamento.



O sistema confirma pagamento.



O sistema notifica vendedores.



O sistema inicia processo logístico.



Pedido recebe status “Em entrega”.



🔁 Fluxos Alternativos

A1 – Cancelamento antes do pagamento



O usuário cancela antes da confirmação de pagamento.



O sistema altera status para “Cancelado”.



Caso de uso encerrado.



A2 – Falha no pagamento



O sistema não autoriza pagamento.



O sistema informa erro.



Usuário pode tentar novamente ou cancelar.



🔺 Exceções



Produto indisponível antes da confirmação.



Endereço inválido.



Serviço de pagamento indisponível.



📏 Regras de Negócio



RN01 – O pedido só pode iniciar entrega após confirmação de pagamento.



RN02 – Produtos pertencem a um único vendedor.



RN03 – Pedido pode conter produtos de múltiplos vendedores.



# **PROMPT NO CHATGPT:**



usuário faz o pedido escolhendo produtos que podem estar ligados à diferentes usuários, após confirmação do pedido, é confirmada a entrega sendo ela feita diretamente pelo aplicativo, escolhendo assim os locais que estão ligados aos usuários donos dos pedidos para que assim seja escolhida a melhor rota e logo após é criado uma confirmação de pagamento e após confirmado o pagamento a entrega é iniciada e é feita a entrega. acima é o fluxo principal de um aplicativo de uma rede social ligada à venda e compra de roupas, o usuário é único e ele já é configurado tanto como vendedor quanto comprador, a escolha é do usuário, eu preciso montar algumas coisas: o fluxo principal remodelado para que seja enumerado o fluxo alternativo para casos de: - cancelamento manual do pedido antes do pagamento - cancelamento do usuário que recebeu um pedido porém precisou cancelar à qualquer momento e por último preciso saber o caso de uso completo do fluxo principal



1\. Identificar stakeholders 2. Listar problemas principais 3. Definir requisitos funcionais 4. Definir requisitos não funcionais



pode me mostrar dois casos de usos detalhados?

