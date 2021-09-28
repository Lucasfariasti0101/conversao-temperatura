Primeiro temos que criar o Dockerfile que vai conter todas as instruções para a
criação de uma imagem do container. Primeiro temos que informar qual é a imagem
que o Docker vai usar como base para a criação da nova, depois temos que definir um 
diretório de trabalho para o Docker, copiamos nesse caso os arquivos package para o diretório, rodamos o comando npm install que instala todas a dependências do projeto listadas no package, depois disso expomos a porta que o container irá executar no caso a 8080 que é a porta que o node usa como padrão, por último, mandamos o terminal rodar o comando "node server.js", que vai inicializar a aplicação.
	
	Depois da criação do Dockerfile devemos rodar o comando para criar a imagem,
neste caso o comando será esse: "docker image build -t  conversao-temperatura ."
depois iremos criar um container com o comando "docker container run -p 8080:8080 convercao-temperatura".
