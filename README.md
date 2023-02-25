# ComoAdicionarSSH_Wind
Mini tutorial em português, como criar e add chave no wind para o github.

*******************************


--- T U T O R I A L —


1 -  Instale o Git no seu computador.
	1 - Configure o Git no seu computador.

2 - Abra o terminal.
	2.0 Vá para pasta .ssh ela está dentro seu usário, abra o terminal lá.
	2.1 - Cole isso ssh-keygen -t ed25519 -C "your_email@example.com"
	
	2.2 - Essa mensagem informa para você um nome para sua chave. Caso não faça isso, uma aleatória é gerada.
	Enter a file in which to save the key (/c/Users/YOU/.ssh/id_ALGORITHM):[Press enter]
	
	2.3 Outra mensagem irá surgir pedindo que você informe uma frase de segurança. Caso não informe, ficará em branco, observação, ficar sem essa frase
	de segurança não é um problema, aperte enter, para deixar em branco.
		
		Enter passphrase (empty for no passphrase): [Type a passphrase]
		Enter same passphrase again: [Type passphrase again]

3 - Agora vamos adicionar sua chave criada ao sistema.

	3.1 - add isso. eval "$(ssh-agent -s)
	
	3.2 - Caso tenha alterado o nome da chave mude id_ed25519 para o nome criado. ssh-add ~/.ssh/id_ed25519


4 - Vá no disco local C, dentro de usuários, acessando a pasta com o nome do usuário root. Vá nas configurações da tela e solicite ver arquivos ocultos. Irá surgir
uma pasta .ssh entre nela e clique com o botão direito dentro dela, botão esquerdo git bash aqui. escreva "cat "nome do arquivo".pub " assim você irá ter acesso
ao conteúdo do arquivo, copie.

Vá até o github. Acesse a configuração, clique em SSH, clique em new SSH key, dê um nome a sua chave e cole no local indicado. 


NOTA: 
git config --global user.name
git config --global user.email

git config --list

*******************************

