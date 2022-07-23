# Como Instalar o LAMP - Apache, MySQL e PHP no Linux/Ubuntu

## APACHE

- Abrir o terminal e atualizar os pacotes através do comando:

  ```bash
  sudo apt update
  ```

- Instalar o Apache através do comando:

  ```bash
  sudo apt install apache2
  ```

- Habilitar o Firewall para rodar Aplicações Web com o seguinte comando:

  ```bash
  sudo ufw app list
  ```

  O Apache deve constar na lista que será apresentada a partir da inserção do comando acima.

- Comando para verificar a porta que o Apache está rodando:

  ```bash
  sudo ufw app info "Apache Full"
  ```

  Será apresentado a porta principal que o Apache está rodando.

- Para permitir/habilitar o Apache no firewall, execute o seguinte comando:

  ```bash
  sudo ufw allow in "Apache Full"
  ```

  As regras serão atualizadas.

- Agora abra o seu navegador/browser e digite na barra de endereço:

  **localhost**

## MYQSL

- Abra o terminal e execute o seguinte comando, para iniciar a instalação do MySQL

  ```bash
  sudo apt install mysql-server mysql-client
  ```

- Verificar o status do serviço do MySQL

  ```bash
  service mysql status
  ```

- Realizar a conexão com o MySQL

  ```bash
  sudo mysql -uroot -p
  ```

  A instalação padrão não precisa de senha. Apenas dar Enter quando for solicitado a senha/password

- Verificar se está conectado ao MySQL

  ```sql
  SHOW DATABASES;
  ```

- Alterar a senha de **root**

  ```sql
  ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'senha_root';
  ```

  **Observação:** No comando acima, onde tem ‘senha_root’ - coloque a senha desejada **entre aspas simples**.

  Dê **Enter**  - ocorrendo tudo bem a mensagem a ser apresetada na tela do terminal será:

  ```sql
  Query OK, 0 rows affected (0.00 sec)
  ```

- Saia do mysql usando **exit** e logue novamente, mas dessa vez sem o sudo, conforme abaixo:

  ```bash
  mysql -uroot -p
  ```

  Será solicitada a senha criada, digite-a. Pronto a Instalação do MySQL. Agora vamos instalar o MySQL Workbench.

- Para instalar o **MySQL Workbench** use o comando seguinte:

  Acesse o link:

  https://dev.mysql.com/downloads/workbench/

  Escolha o sistema operacional e a versão

  Baixe o pacote e instale

  ```bash
  sudo apt install mysql-workbench
  ```

  Agora abra o MySQL Workbench e clique em Local Instance 3306 e digite a senha criada. Pronto. Instalação completa.

## PHP

- Instalar o PHP, a biblioteca que vai conectar o PHP ao APACHE e a biblioteca que vai conectar o PHP ao MySQL,  através do seguinte comando:

  ```bash
  sudo apt install php libapache2-mod-php php-mysql
  ```

- Após a conclusão do processo acima é necessário reiniciar o servidor do Apache, com o comando:

  ```bash
  sudo systemctl restart apache2
  ```

  O procedimento é simples. Ocorrendo tudo certo não vai aparecer nada na tela, apenas o seu usuário para digitar um novo comando.

- Confira o status do Apache com o seguinte comando:

  ```bash
  sudo systemctl status apache2
  ```

  Será apresentada a tela com o status Ok (bolinha verde) . Para sair aperte a teca Q.

- Acesse a pasta root do Apache, através do comando:

  ```bash
  cd /var/www/html
  ls
  ```

- Dentro da pasta root do Apache - Crie um arquivo para teste, com o nano (ou o editor de sua preferência), com o seguinte comando:

  ```bash
  sudo nano teste.php
  ```

- Quando, no terminal, a tela do nano abrir para a edição do arquivo criado (teste.php), crie a tag de abertura e fechamento do PHP - use o exemplo abaixo:

  ```php
  <?php
  	echo "Hello World!";
  ?>
  ```

  Depois:

  - **Ctrl Shift O** - para salvar - depois **Enter**
  - **Ctrl Shift X** - para sair

  Observação: echo é uma função que vai imprimir algo na tela. O ;

- Para testar o arquivo criado, abra o navegador/browser e na barra de navegação digite:

  **localhost/teste.php**