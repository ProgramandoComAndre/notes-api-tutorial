# Funcionalidades


## Utilizador
1- Criar conta de utilizador
2- Login
3- Confirmar email(opcional mas devia de ter)
4- Mudar password(opcional mas pode ter)

## Notas

1- Criar uma nota e associar ao utilizador autenticado
2- Apagar uma nota
3- Conseguir as notas do utilizador
4- Atualizar a nota


1- Criar conta de utilizador

POST /users/register (name,email, password, confirmpassword)

Se o email for inválido -> retorna 400 { message: 'Email invalido'}
Se a password for invalido -> retorna 400 { message: 'Password invalida'}
Se a password não for a mesma do campo confirmpassword-> retorna 400 { message: 'Password não coincide com a confirmação'}
Se a conta de utilizador existir(se o email já coincidir com algum)-> retorna 400 { message: 'Utilizador já existente'}
Se a conta não existir -> chamar serviço de criar a conta -> aceder à base de dados -> registar utilizador
No final: retorna 201(Created) { id: 'ajdsoaladsoadsjasdoasd', name: 'teste', email: 'teste@test.com', password: 'qualquer coisa'}
