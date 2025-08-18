---
id: Linux Dependencies
aliases: []
tags:
  - linux
---

1. Dunst - Notification daemon
   - Install: `sudo apt install dunst`
   - Configuration: `~/.config/dunst/dunstrc`

2. Flameshot - Screenshot tool
   - Install: `sudo apt install flameshot`
   - Configuration: `~/.config/flameshot/flameshot.ini`

3. Polybar - Status bar
   - Install: `sudo apt install polybar`
   - Configuration: `~/.config/polybar/config`

4. Picom - Compositor
   - Install: `build from source`
   - Configuration: `~/.config/picom/picom.conf`

5. Rofi - Application launcher
   - Install: `sudo apt install rofi`
   - Configuration: `~/.config/rofi/config.rasi`

6. Kitty - Terminal emulator
   - Install: `sudo apt install kitty`
   - Configuration: `~/.config/kitty/kitty.conf`

7. Neovim - Text editor
   - Install: `build from source for latest version or use package manager`
   - Configuration: `~/.config/nvim/init.vim`

8. zsh - Shell
   - Install: `sudo apt install zsh`
   - Configuration: `~/.zshrc`

9. fsearch - File search utility
   - Install: `sudo apt install fsearch`

10. ranger - File manager
    - Install: `sudo apt install ranger`
    - Configuration: `~/.config/ranger/rc.conf`

11. git - Version control system
    - Install: `sudo apt install git`
    - Configuration: `~/.gitconfig`

12. vlc - Media player
    - Install: `sudo apt install vlc`

13. mpd - Music Player Daemon
    - Install: `sudo apt install mpd`
    - Configuration: `~/.config/mpd/mpd.conf`

14. mpc - Music Player Client
    - Install: `sudo apt install mpc`

15. plattenalbum - Music player
    - Install: Install from source or use flathub

16. fzf - File fuzzy finder
    - Install: `sudo apt install fzf`
    - Setup:

    ```sh
    # Set up fzf key bindings and fuzzy completion in ~/.zshrc
    source <(fzf --zsh)
    ```

17. wikiman - manpage fuzzy finder
    - Install: Install '.deb' file from github page

18. bat - preview syntax highlighting
    - Install: `sudo apt install bat`

19. tealdeer - manpage summary
    - Install: `sudo apt install tealdeer`
