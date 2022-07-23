# Como Restaurar a barra de tarefas/painel do Linux XFCE

### Todos os comandos abaixo devem ser executados com o atalho Alt F2 e um por vez.

xfce4-panel --quit 

pkill xfconfd 

rm -rf ~/.config/xfce4/panel 

rm -rf ~/.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-panel.xml 

xfce4-panel