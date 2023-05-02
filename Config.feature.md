#language: pt

Funcionalidade: Configurar produto   
Como cliente da EBAC-SHOP
Quero configurar meu produto de acordo com meu tamanho, cor e quantidade
Para depois inserir no carrinho

Contexto:
Dado que sou cliente da EBAC-SHOP

Cenario: Inserir produto no carrinho com sucesso

Quando configuro o produto escolhido com o tamanho, cor 
E quantidade desejada 
Entao posso inserir no carrinho

Cenario: Inserir mais de 10 itens 

Quando seleciono a quantidade de um determinado produto
E a <quantidade>
Entao o sistema deve apresentar uma mensagem de alerta <mensagem> ""

| Quantidade | Mensagem                                |
| "1"        | " Adicionado ao carrinho com sucesso "  |
| "5"        | " Adicionado ao carrinho com sucesso "  |
| "11"       | " Venda limitada a 10 itens por pedido" |
| "12"       | " Venda limitada a 10 itens por pedido" |

Cenario: Não preencher campos obrigatorios

Quando seleciono o produto 
E nao seleciono o tamanho ou a cor 
Entao o sistema deve apresentar uma mensagem de alerta "Por gentileza selecione o tamnho e cor desejados"

Cenario: Limpar cor e tamanhos selecionados 

Quando Clicar no botão limpar 
Entao os campos selecionados irão ser desselecionados 
