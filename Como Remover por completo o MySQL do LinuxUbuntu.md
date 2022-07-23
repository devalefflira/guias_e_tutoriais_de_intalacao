# Como Remover por completo o MySQL do Linux/Ubuntu

- Verificar se o programa está instalado:

  ```bash
  dpkg -l mysql-server
  ```

- Remover o mysql-server:

  ```bash
  sudo apt-get remove --purge mysql-server
  ```

- Remover o PHPMYADMIN - gerenciador gráfico de banco de dados:

  ```bash
  sudo apt-get remove --purge phpmyadmin
  ```

- Parar o serviço do MySQL:

  ```bash
  sudo /etc/init.d/mysql stop
  ```

- Remover o pacote common do MySQL

  ```bash
  sudo apt-get remove --purge mysql-common
  ```

- Apagar a pasta mysql

  ```bash
  sudo rm -rf /var/lib/mysql
  ```

- Executar os seguintes comandos - **um comando por vez:**

  ```bash
  sudo apt-get autoremove --purge
  ```

  ```bash
  sudo apt-get autoclean
  ```

  ```bash
  sudo apt-get clean
  ```

- Realizar nova verificação de instalação do MySQL

  ```bash
  dpkg -l mysql-server
  ```

  ```bash
  mysql --version
  ```

  Pronto. Agora você removeu por completo o MySQL do seu Linux/Ubuntu.