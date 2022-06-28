## Instalação e Configuração do Moodle

<p>Instalação de pacotes necessários</p>

    apt install -y graphviz aspell ghostscript clamav git

![moddle1](install moddle.JPG)

<p>Instalação do mariadb</p>

    apt install -y mariadb-server mariadb-client

![mariadb1](mariadb.JPG)

<p>Instalação do webserver Apache com o suporte php</p>

    apt install -y apache2 php libapache2-mod-php php-cli php-mysql php-mbstring php-xmlrpc php-zip

![webserver1](web1.JPG)

![webserver2](web2.JPG)

<p>Reiniciar o serviço apache</p>

``` systemctl restart apache2 ```

#### Criação de um diretório para baixar o moodle

![diretório moodle](dir-moodle.JPG)

#### Configurações

![conf moodle](conf-moodle.JPG)

#### Criando banco de dados e usuário no mariadb

![usuário-mariadb](usuario-mariadb.JPG)

>```rm /var/www/html/index.html ```
>
>```chmod 777 /var/www ```

![m1](m1.JPG)

![m2](m2.JPG)

![m3](m3.JPG)

![m4](m4.JPG)

![m5](m5.JPG)

![m6](m6.JPG)

``` chmod 777 /var/www ```

