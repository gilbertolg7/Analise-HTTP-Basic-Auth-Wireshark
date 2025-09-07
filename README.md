# Análise de Trafego de Rede com Wireshark
## Challenge - Http Basic Auth
__Cenário:__  Foi encaminhado um log para a Central de monitoramento de segurança relatando atividades de um possivel ataque</br>
A central deve retirar o máximo de informações do arquivo .pcap</br>
Para isso deve-se utilizar uma VM disponivel com o arquivo </br>
Wireshark é a ferramenta utilziada para a analise detalhada</br>
![](/images/inicial.png)

## Perguntas a serem respondidas.
![](/images/HTTP%20pacotes.png)
__How many HTTP GET requests are in pcap?__  5 pacotes de requests</br>
Foi utilizado a vizualizaçao das estatisticas com a filtro de HTTP e contadores de pacotes </br>
![](/images/Server.png)
__What is the server operating system?__  FreeBSD Apache IP 1.1.1.5</br>
__What is the name and version of the web server software?__ Apache/2.2.15</br>
__What is the version of OpenSSL running on the server?__ OpenSSL/0.9.8n</br>
Foi utilizado uma response do servidor para obter os dados do mesmo</br>
![](/images/user-agent.png)
__What is the client's user-agent information?__  Lynx/2.8.7rel.1 libwww-FM/2.14 SSL-MM/1.4.1 OpenSSL/0.9.8n</br>
Foi utilizado um request do cliente para obter os dados do mesmo</br>
![](/images/200.png)
__What is the username used for Basic Authentication?__ webadmin </br>
__What is the user password used for Basic Authentication?__ W3b4Dm1n</br>
Foi utilizado um request do cliente com sucesso em seguida, isso indica que os dados foram autentifcados corretamente e o acesso foi concedido</br>

## Resultado da analise.
__Total de Requisições:__ 5 requisições HTTP GET.
__Informações do Servidor:__ Sistema operacional FreeBSD Apache IP 1.1.1.5, Web Server Apache/2.2.15, OpenSSL/0.9.8n.
__Informações do Cliente__: O cliente usou o User-Agent Lynx/2.8.7rel.1, indicando que se trata de um navegador de texto.
__Credenciais de Autenticação:__ A autenticação Basic Auth revelou o usuário webadmin e a senha W3b4Dm1n.

## Recomendações.
Utilização de Sites ou Servers HTTPS para gerar mais segurança a empresa
Investigação profunda para buscar mais usuários em comum, alem do user-agent indicar um navagador de texto não comum para fazer a requisição.
Basic Auth representa um risco nos dias autais, portanto deve-se tomar cuidado na utilização e se utilizado na empresa a mudança é crucial.

 


