📌 Caso de Uso 02 – Cancelar Pedido

Nome:



Cancelar pedido



Atores:



Usuário comprador



Usuário vendedor



Sistema de pagamento



Sistema administrativo



Descrição:



Permite cancelamento de pedido antes ou após pagamento, respeitando regras de status.



Pré-condições:



Pedido deve existir.



Pedido não deve estar finalizado como “Entregue”.



Pós-condições:



Pedido marcado como “Cancelado”.



Se houver pagamento, estorno iniciado.



🔄 Fluxo Principal (Cancelamento antes do pagamento)



O usuário acessa seus pedidos.



O usuário seleciona pedido pendente.



O usuário solicita cancelamento.



O sistema solicita confirmação.



O usuário confirma.



O sistema altera status para “Cancelado”.



Caso de uso encerrado.



🔁 Fluxos Alternativos

A1 – Cancelamento pelo vendedor antes da entrega



Vendedor recebe notificação do pedido.



Vendedor solicita cancelamento.



Sistema notifica comprador.



Sistema verifica status:



Se pagamento não confirmado → cancela imediatamente.



Se pagamento confirmado → inicia processo de estorno.



Pedido recebe status “Cancelado”.



A2 – Cancelamento após início da entrega



Usuário ou vendedor solicita cancelamento.



Sistema verifica status.



Se entrega já iniciada:



Sistema bloqueia cancelamento automático.



Encaminha para análise administrativa.



Administração decide:



Aprovar → estorno.



Negar → pedido continua.



🔺 Exceções



Tentativa de cancelamento de pedido já entregue.



Falha na comunicação com sistema de pagamento para estorno.



📏 Regras de Negócio



RN01 – Pedido entregue não pode ser cancelado automaticamente.



RN02 – Estorno deve ocorrer integralmente em caso de cancelamento pós-pagamento.



RN03 – Cancelamento deve registrar histórico para auditoria.



# **PROMPT NO CHATGPT:**



usuário faz o pedido escolhendo produtos que podem estar ligados à diferentes usuários, após confirmação do pedido, é confirmada a entrega sendo ela feita diretamente pelo aplicativo, escolhendo assim os locais que estão ligados aos usuários donos dos pedidos para que assim seja escolhida a melhor rota e logo após é criado uma confirmação de pagamento e após confirmado o pagamento a entrega é iniciada e é feita a entrega. acima é o fluxo principal de um aplicativo de uma rede social ligada à venda e compra de roupas, o usuário é único e ele já é configurado tanto como vendedor quanto comprador, a escolha é do usuário, eu preciso montar algumas coisas: o fluxo principal remodelado para que seja enumerado o fluxo alternativo para casos de: - cancelamento manual do pedido antes do pagamento - cancelamento do usuário que recebeu um pedido porém precisou cancelar à qualquer momento e por último preciso saber o caso de uso completo do fluxo principal



1\. Identificar stakeholders 2. Listar problemas principais 3. Definir requisitos funcionais 4. Definir requisitos não funcionais



pode me mostrar dois casos de usos detalhados?

