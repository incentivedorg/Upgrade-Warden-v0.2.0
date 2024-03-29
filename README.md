# Upgrade-Warden-v0.2.0
Applies to those who have installed according to previous instructions

https://github.com/incentivedorg/Warden-protocol

```sudo systemctl stop wardend
sudo apt install unzip -y
cd $HOME
sudo rm -rf /usr/local/bin/wardend
wget https://github.com/warden-protocol/wardenprotocol/releases/download/v0.2.0/wardend_Linux_x86_64.zip
unzip wardend_Linux_x86_64.zip
rm -rf wardend_Linux_x86_64.zip
chmod +x wardend
sudo mv wardend /usr/local/bin/
wardend version
sudo systemctl daemon-reload
sudo systemctl enable wardend
sudo systemctl restart wardend && sudo journalctl -u wardend -f --no-hostname -o cat```
