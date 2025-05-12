# Summary
Keyboard setup for my linux devices with a Norwegian keyboard layout.

# Features
 - Make Ctrl+Alt behave as AltGr to access certain 3rd level characters such as `{`, `[`, `~`, etc

# Setup
1. Install [keyd](https://github.com/rvaiya/keyd)
2. Copy config 
```bash
sudo cp keyd/* /etc/keyd/default.conf
```
3. Apply config
```bash
sudo keyd reload
```