# Espate-BodhiBuilder

EspateOS用にカスタマイズされたBodhiBuilderです。  
日本語化やvesamenu.c32が見つからないバグなどが修正されています。  
アイコンを参照するディレクトリもEspateOS用に変更されています。  

# インストール方法

EspateOS向けのものですが、他のUbuntu系ディストリビューションでも使用できるように、あえてファイル配置などは変更していません。  
BodhiBuilderとの完全な互換性を保ち、ファイル構造などは一切変更していません。　

```bash
sudo apt install git --yes
cd ~/
git clone https://github.com/Hayao0819/espate-bodhibuilder.git
chmod 755 -R espate-bodhibuilder
dpkg -b espate-bodhibuilder
rm -r espate-bodhibuilder
sudo apt purge git --yes
sudo apt install gdebi-core --yes
sudo gdebi espate-bodhibuilder.deb
sudo apt purge gdebi-core --yes
sudo apt --purge --yes autoremove
sudo apt clean
sudo bodhibuilder-gtk
```