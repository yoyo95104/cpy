# Cpy
a simple clipboard manager for wayland written in rust
## Installation
### Prerequisites
  - wl-clipboard
  - rofi (if you use wofi change every entry in src/main.rs , disclamer: images wont render in wofi)
  - rust language
### Building the Project
```bash
  git clone https://github.com/yooyo95104/cpy.git]
  cd cpy
  cargo install --path .
```
then add a system file like this
```bash
  mkdir -p ~/.config/systemd/user
  nano ~/.config/systemd/user/cpy.service
```
then paste this 
```
[Unit]
Description=cpy Clipboard Daemon
After=graphical-session.target

[Service]
ExecStart=%h/.cargo/bin/cpy daemon
Restart=always

[Install]
WantedBy=graphical-session.target
```

# Tips and Tricks
  you can have the popup menu to select which item you want to copy like this
  ```bash
    cpy pick
  ```
  you can add it to your WM with the exec command
