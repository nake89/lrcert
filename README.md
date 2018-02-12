# lrcert
CLI tool to list non-self-signed certificates (for certain user by username or domain or for all users) in cPanel.
### Usage
```
Usage: lrcert [OPTION] [INPUT]
Example: lrcert [cPanel username]

Options:
  -d [domain]      Displays all certificates of the owner of the domain.
  -a, --all        Lists all certificates of all cPanel users
  -v, --version    Displays version.
  -h, --help       This help page.

```

### Prerequisites
**jq** is needed for json parsing. cPanel api gives out the result in json, which is why it is needed. You can install it simply by typying the below in to the terminal:
```
yum install jq
```

### Installing
```
mkdir ~/bin
cd ~/bin
echo export PATH=\$PATH:$PWD >> ~/.bashrc
source ~/.bashrc
cd ~
git clone https://github.com/nake89/lrcert
mv lrcert/ .lrcert
cd .lrcert
chmod u+x lrcert
ln -s ~/.lrcert/lrcert ~/bin/lrcert
```
