🔹 Fluxo Principal (Enumerado)

Fluxo Principal – Compra com múltiplos vendedores

O usuário acessa o aplicativo.

O usuário navega pelos produtos disponíveis.

O usuário adiciona ao carrinho produtos que podem pertencer a diferentes usuários (vendedores).

O usuário revisa o carrinho.

O usuário confirma o pedido.

O sistema agrupa os produtos por vendedor.

O sistema identifica os endereços vinculados a cada vendedor.

O sistema calcula a melhor rota de entrega considerando todos os pontos de coleta.

O sistema apresenta o resumo final (valor total + frete).

O usuário confirma o pagamento.

O sistema processa o pagamento.

O sistema confirma o pagamento.

O sistema notifica todos os vendedores envolvidos.

O sistema agenda a coleta dos produtos.

A entrega é iniciada.

O pedido é entregue ao comprador.

O sistema finaliza o pedido como concluído.

🔹 Fluxos Alternativos
📌 A1 – Cancelamento manual antes do pagamento

Ponto de desvio: Antes do passo 10 do fluxo principal.

O usuário acessa o resumo do pedido.

O usuário seleciona a opção "Cancelar pedido".

O sistema solicita confirmação do cancelamento.

O usuário confirma.

O sistema cancela o pedido.

O pedido recebe status cancelado (antes do pagamento).

O fluxo é encerrado.

📌 A2 – Cancelamento por vendedor

Esse cenário pode acontecer após a confirmação do pedido, mas antes ou depois do pagamento.

A2.1 – Cancelamento antes do pagamento

O vendedor recebe notificação de novo pedido.

O vendedor escolhe cancelar o pedido.

O sistema notifica o comprador.

O pedido é cancelado.

O fluxo é encerrado.

A2.2 – Cancelamento após pagamento confirmado

Ponto de desvio: Após o passo 12 do fluxo principal.

O vendedor solicita cancelamento.

O sistema verifica status da entrega.

Se a entrega ainda não foi iniciada:

O sistema aprova cancelamento.

O sistema inicia processo de estorno.

O comprador é notificado.

Pedido recebe status cancelado com reembolso.

Se a entrega já foi iniciada:

O sistema bloqueia cancelamento automático.

Encaminha para análise administrativa.

Fluxo encerrado.

🔹 Caso de Uso Completo – Fluxo Principal
Nome:

Realizar compra com múltiplos vendedores

Ator principal:

Usuário (comprador)

Atores secundários:

Usuários vendedores

Sistema de pagamento

Sistema de logística

Pré-condições:

Usuário autenticado.

Produtos cadastrados.

Vendedores com endereço válido.

Meio de pagamento válido.

Pós-condições (sucesso):

Pagamento confirmado.

Entrega realizada.

Pedido finalizado.

Pós-condições (falha):

Pedido cancelado.

Pagamento não processado.

Estorno realizado (se aplicável).


1️⃣ Identificação dos Stakeholders
🔹 Primários

Usuário comprador/vendedor (entidade única que assume ambos os papéis)

Equipe administrativa da plataforma

Entregadores / sistema de logística

🔹 Secundários

Sistema de pagamento (ex: Stripe, PayPal, Mercado Pago)

Serviço de mapas/roteirização (ex: Google Maps)

Órgãos reguladores (LGPD no Brasil) — exigências legais de dados

2️⃣ Principais Problemas que o Sistema Resolve

Centralização de venda social de roupas

Usuários querem vender e comprar no mesmo ambiente.

Compra de múltiplos vendedores em um único pedido

Complexidade de agrupar produtos e calcular rota otimizada.

Coordenação logística

Coleta em múltiplos pontos com entrega única.

Garantia de pagamento seguro

Confirmação antes da entrega.

Reembolso em caso de cancelamento.

Gestão de cancelamentos

Cancelamento antes do pagamento.

Cancelamento por vendedor.

Cancelamento com reembolso.

Confiança entre usuários

Notificações, status do pedido, rastreio.

3️⃣ Requisitos Funcionais (RF)
🔹 Gestão de Usuário

RF01 – O sistema deve permitir cadastro e autenticação de usuários.

RF02 – O usuário deve poder atuar como comprador e vendedor.

RF03 – O usuário deve cadastrar endereço.

RF04 – O usuário deve cadastrar produtos para venda.

🔹 Catálogo e Carrinho

RF05 – O sistema deve permitir visualizar produtos.

RF06 – O usuário deve adicionar produtos ao carrinho.

RF07 – O carrinho deve permitir produtos de múltiplos vendedores.

🔹 Pedido

RF08 – O sistema deve permitir confirmação de pedido.

RF09 – O sistema deve agrupar produtos por vendedor.

RF10 – O sistema deve calcular valor total e frete.

RF11 – O sistema deve calcular rota otimizada para coleta.

🔹 Pagamento

RF12 – O sistema deve processar pagamento.

RF13 – O sistema deve confirmar pagamento antes de iniciar entrega.

RF14 – O sistema deve permitir estorno em caso de cancelamento após pagamento.

🔹 Entrega

RF15 – O sistema deve notificar vendedores após pagamento confirmado.

RF16 – O sistema deve iniciar processo logístico.

RF17 – O sistema deve atualizar status da entrega.

RF18 – O sistema deve finalizar pedido após entrega concluída.

🔹 Cancelamento

RF19 – O comprador deve poder cancelar antes do pagamento.

RF20 – O vendedor deve poder solicitar cancelamento.

RF21 – O sistema deve avaliar status antes de aprovar cancelamento pós-pagamento.

4️⃣ Requisitos Não Funcionais (RNF)
🔹 Segurança

RNF01 – O sistema deve proteger dados conforme LGPD.

RNF02 – Pagamentos devem ser criptografados.

RNF03 – Autenticação deve ser segura.

🔹 Desempenho

RNF04 – O cálculo de rota deve ocorrer em tempo aceitável (< 5 segundos).

RNF05 – O sistema deve suportar múltiplos pedidos simultâneos.

🔹 Disponibilidade

RNF06 – Sistema disponível 24/7.

RNF07 – Backup automático de dados.

🔹 Escalabilidade

RNF08 – Arquitetura deve permitir crescimento do número de usuários.

RNF09 – O sistema deve suportar múltiplos vendedores em um mesmo pedido sem degradação significativa.

🔹 Usabilidade

RNF10 – Interface intuitiva.

RNF11 – Status do pedido deve ser claramente exibido.

🔹 Confiabilidade

RNF12 – O sistema não deve iniciar entrega sem confirmação de pagamento.

RNF13 – O sistema deve garantir consistência transacional (pedido + pagamento).



REFERÊNCIA - Chatgpt
PROMPT:
usuário faz o pedido escolhendo produtos que podem estar ligados à diferentes usuários, após confirmação do pedido, é confirmada a entrega sendo ela feita diretamente pelo aplicativo, escolhendo assim os locais que estão ligados aos usuários donos dos pedidos para que assim seja escolhida a melhor rota e logo após é criado uma confirmação de pagamento e após confirmado o pagamento a entrega é iniciada e é feita a entrega. acima é o fluxo principal de um aplicativo de uma rede social ligada à venda e compra de roupas, o usuário é único e ele já é configurado tanto como vendedor quanto comprador, a escolha é do usuário, eu preciso montar algumas coisas: o fluxo principal remodelado para que seja enumerado o fluxo alternativo para casos de: - cancelamento manual do pedido antes do pagamento - cancelamento do usuário que recebeu um pedido porém precisou cancelar à qualquer momento e por último preciso saber o caso de uso completo do fluxo principal
preciso também:
Identificar stakeholders 2. Listar problemas principais 3. Definir requisitos funcionais 4. Definir requisitos não funcionais