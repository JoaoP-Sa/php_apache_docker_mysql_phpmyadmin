# Resumo
Neste diretório encontram-se algumas configurações básicas para que
seja possível rodar um projeto com PHP + Apache + MySQL + PHPMyAdmin em um
ambiente docker, para executar o docker e fazer o ambiente rodar basta rodar
o comando:

    docker compose up -d

# Arquivos
Ao desenvolver algum projeto em php é importante que os arquivos estejam
dentro do diretório www, pois é através dele que o servidor irá servir
a aplicação.

Nota: Caso queira é possível mudar o diretório dos arquivos do projeto, basta
apenas que o desenvolvedor altere a linha 7 do arquivo docker-compose.yaml
e indique qual será o diretório de trabalho (exemplo: se quiser que o
diretório de trabalho seja a pasta raíz basta alterar a linha 7 para 
" - .:/var/www/html/ "), e após a modificação é necessário rodar o comando
"docker-compose down" para derrubar os containeres e em seguida o comando
"docker-compose up -d --build" para se certificar de que todas as alterações
sejam feitas no container do php-apache.
