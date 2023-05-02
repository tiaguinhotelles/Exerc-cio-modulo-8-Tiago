#language: pt

Funcionalidade: Tela de cadastro - Checkout
Como cliente da EBAC-SHOP
Quero fazer concluir meu cadastro   
Para finalizar minha compra

Contexto: 
Dado que eu realize o cadastro no checkout

Cenario: Cadastro com sucesso 
Quando eu preencher os campos obrigatorios
E clicar em finalizar compra
Entao o sistema deve exibir a mensagem de "compra conluida com sucesso"

Cenario: campos obrigatorios incompletos   
Quando preencher os campos obrigatorios
E um <campo obrgatorio> estiver em branco
Entao o sistema deve exibir uma <mensagem>

| Campo obrigatorio  | Mensagem                                             |
| Nome Completo      | "Por gentileza preencher o campo Nome Obrigatorio"   |
| Data de nascimento | "Por gentileza preencher o campo Data de nascimento" |
| Endereço           | "Por gentileza preencher o campo Endereço"           |
| CPF                | "Por gentileza preencher o campo CPF"                |
| CEP                | "Por gentileza preencher o campo CEP"                |

Cenario: campo e-mail com formato invalido 
Quando preencher o campo email no formato diferente de "teste@teste.com"
E clicar em finalizar compra
Entao o sistem deve exibir uma mensagem "Formato de e-mail incorreto , por gentileza verifique novamente o campo"
