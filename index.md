<h2>Generació dels certificats:</h2>
<p>He decidit crear el certificat amb mkcert.</p>
<p>En el terminal base posem:</p>
<p>- sudo apt-get update</p>
<p>- sudo apt install wget libnss3-tools</p>
<p>- /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"</p>
<p>- sudo apt-get install git</p>
<p>- test -d ~/.linuxbrew && eval $(~/.linuxbrew/bin/brew shellenv)</p>
<p>- test -d /home/linuxbrew/.linuxbrew && eval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)</p>
<p>- test -r ~/.bash_profile && echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.bash_profile</p>
<p>- echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.profile</p>
<p>- brew install mkcert</p>
<p><img src="https://raw.githubusercontent.com/Areebaellahi/FOTOS/main/7.png" alt="Cat"></p>
<p>Després d'instal·lar el mkcert hem de crear la clau i el certificat.</p>
<p>En el terminal posem:</p>
<p>- mkcert example.com "*example.com" example.test inte 10.5.2.14</p>
<p>He creat la clau i el certificat amb el nom exemple.com, Ara vull canviar el nom de example.com per "clave.pem" i "certificat.pem":</p>
<p>- mv example.com+4-key.pem clau.pem</p>
<p>- mv example.com+4.pem certificat.pem</p>
<p><img src="https://raw.githubusercontent.com/Areebaellahi/FOTOS/main/claucerti.png" alt="Cat"></p>
<p>Una vegada creat els certificats, anem a firefox i posem la ip del inte i barra admin (https://10.5.2.14/admin)i fem login:</p>
<p>Anem a "System settings" > "TLS certificate"</p>
<p>Ara posem la clau i els certificats fent click a Browse</p>
<p><img src="https://raw.githubusercontent.com/Areebaellahi/FOTOS/main/browse.png" alt="Cat"></p>
Una cop posat la clau i el certificat anem a inte per reiniciar docker:




<p><img src="https://raw.githubusercontent.com/Areebaellahi/FOTOS/main/6.png" alt="Cat"></p>

