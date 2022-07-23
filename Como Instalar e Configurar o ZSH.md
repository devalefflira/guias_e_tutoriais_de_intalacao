# Como Instalar e Configurar o ZSH

- Abra o terminal e atualize os pacotes:

  ```bash
  sudo apt update -y
  sudo apt upgrade -y
  ```

- Instalar os pacotes a seguir

  ```bash
  sudo apt install dkms make perl gcc build-essential git curl -y
  ```

- Instalar e configurar o ZSH

  ```bash
  sudo apt install zsh -y
  chsh -s /bin/zsh
  zsh
  ```

- Instalar Oh-my-zsh!

  ```bash
  sh -c "$(curl -fsSL <https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh>)"
  ```

- Instalar o Tema Spaceship Prompt

  ```bash
  git clone <https://github.com/spaceship-prompt/spaceship-prompt.git> "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
  ```

  ```bash
  ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
  ```

- Mudar o tema padrão do ZSH

  - No terminal coloque: nano ~/.zshrc
  - Vá até a linha ZSH_THEME
  - Altere para “spaceship”

  Ctrl Shift O para salvar

  Ctrl Shift X para sair

- Instalar ZSH Autosuggestions

  ```bash
  git clone <https://github.com/zsh-users/zsh-autosuggestions> ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
  ```

- Instalar o ZSH Syntax Highlighting

  ```bash
  git clone <https://github.com/zsh-users/zsh-syntax-highlighting.git> ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
  ```

- Acessar novamente o arquivo .zsh e Alterar os plugins (Autosuggestions e Highlighting)

  - Encontrar a linha plugins

  - Colocar o seguinte: zsh-autosuggestions zsh-syntax-highlighting

    Obs: depois do termo git

- Último passo:

  Reiniciar o PC