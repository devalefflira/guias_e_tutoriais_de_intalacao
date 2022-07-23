# Como Instalar o VirtualBox no Linux/Ubuntu 20.04 - via terminal >◼️

- 1° Acesse o link abaixo ou vá direto para o passo 2 se a sua versão do Ubuntu for a 20.04

  [**](https://www.virtualbox.org/wiki/Linux_Downloads)https://www.virtualbox.org/wiki/Linux_Downloads**  ↗️

- 2° Ubuntu 20.04. Se você estiver na mesma versão que o tutorial, segue o link direto:

  [**](https://download.virtualbox.org/virtualbox/6.1.34/virtualbox-6.1_6.1.34-150636.1~Ubuntu~eoan_amd64.deb)https://download.virtualbox.org/virtualbox/6.1.34/virtualbox-6.1_6.1.34-150636.1~Ubuntu~eoan_amd64.deb**  ↗️

- 3° Aguarde o download finalizar

  ☕ Beba um café, uma água…rsrsrsrs 🙂👍

- 4° Abra o terminal

  (Ctrl Alt T) - Vá até a pasta onde está localizado o download do pacote do virtualbox. Por padrão é na pasta Downloads.

  ```bash
  cd Downloads
  ```

  Depois liste os arquivos:

  ```bash
  ls
  ```

- 5º Após localizar o arquivo baixado, execute o seguinte comando no terminal:

  ```bash
  sudo dpkg -i virtualbox-6.1_6.1.34-150636.1_Ubuntu_eoan_amd64.deb
  ```

  Aguarde a finalização da instalação.

  Pronto. O VirtualBox está instalado. Vamos conferir!