#	fedora 28 packet tracer repository


### Installation

step 1 :

'''sh
$ sudo dnf install zlib-devel ncurses-devel gtk2 glibc glibc-devel  \\
 libpng12 libstdc++ libX11-devel libXrender libXrandr libusb \\ 
 libXtst nss qt qtwebkit qt5-qtmultimedia qt5-qtwebkit
'''

step 2 :

'''sh
$ git clone https://github.com/0xbj/packettracer_fedora28.git
$ cd packettracer_fedora28
$ cp -rf .lib64 ~
$ cd openssl_x86_64 && sudo rpm -i openssl-lib-compat-1.0.0i-1.fc28.x86_64.rpm && cd ,,
'''

step 3 :

'''sh
$ tar -xzf PacketTracer71_*_linux.tar.gz && cd PacketTracer71
$ chmod +x install
$ sudo ./install
'''

step 4 :

'''sh
$ sudo chmod +x /opt/pt/set_ptenv.sh
$ sudo /opt/pt/set_ptenv.sh
$ sudo chmod +x /opt/pt/set_qtenv.sh
$ sudo /opt/pt/set_qtenv.sh
'''

step 5 :
'''sh
$ sudo sed -i "s|lib|lib:$HOME/.lib64|g" /opt/pt/packettracer
'''