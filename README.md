<h1 align="center">Twitter Clone</h1>

|  | Telas do Sistema |
|---------- | --------|
|Login | ![principal](https://user-images.githubusercontent.com/38691922/87491915-c1724a00-c61f-11ea-8870-0ba28fd0e3bc.png) |
|Home | ![home](https://user-images.githubusercontent.com/38691922/87491898-b3242e00-c61f-11ea-9627-39b28a1f3587.png)|
|Inscrever-se | ![inscrever-se](https://user-images.githubusercontent.com/38691922/87491733-4c067980-c61f-11ea-947a-19db5280b03f.png) |
|Seguir | ![seguir](https://user-images.githubusercontent.com/38691922/87492743-a1438a80-c621-11ea-9861-a9413e5b1d44.png) |

<h2> <img src="https://user-images.githubusercontent.com/38691922/77790815-3d7e5d00-7044-11ea-8ffe-e8d448946d4a.png" height="30" width="30">Projeto</h2>

Trata-se de uma aplicação que visa reproduzir algumas funcionalidades do Twitter como forma de estudo. 

<h2><img src="https://user-images.githubusercontent.com/38691922/77791007-98b04f80-7044-11ea-9602-4c78098960a0.png" height="40" width="40">Tecnologia</h2>

* PHP


<h2> <img src="https://user-images.githubusercontent.com/38691922/77794952-838aef00-704b-11ea-84ff-cb3c7a61a815.png" height="30" width="30">  Configuração</h2>

Para rodar o sistema será necessário executar o comando ``` php -S localhost:8080 ``` dentro da pasta public e, ainda, deve possuir o seguinte programa:

* Xampp or similar
<p>
  É preciso dar um <strong>start</strong> no Apache e no MySQL. 
</p>

<h2> <img src="https://user-images.githubusercontent.com/38691922/87493125-81f92d00-c622-11ea-951b-f61090181678.png" height="30" width="30">  Configuração do Banco de Dados</h2>

Para criação do banco de dados que essa aplicação utiliza, rode as seguintes queries:

```
  create database twitter_clone;

  use twitter_clone;

  create table usuarios(
    id int not null primary key AUTO_INCREMENT,
    nome varchar(100) not null,
    email varchar(150) not null,
    senha varchar(32) not null
  );

  create table tweets(
    id int not null PRIMARY KEY AUTO_INCREMENT,
    id_usuario int not null,
    tweet varchar(140) not null,
    data datetime default current_timestamp
  );

  create table usuarios_seguidores(
    id int not null primary key auto_increment,
    id_usuario int not null,
    id_usuario_seguindo int not null
  );
  
```

Ainda será necessário modificar o arquivo <strong>Connection.php</strong> dentro da pasta <strong>App</strong>, caso as suas configurações estejam diferentes das minhas. 
É nela que tem a configuração da conexão com o banco de dados, nome do banco, nome do user e a senha.

<h2><img src="https://user-images.githubusercontent.com/38691922/77791613-bcc06080-7045-11ea-864b-78684851af42.png" 
         height="30" width="30"> Como contribuir</h2>
         
* Faça um fork desse repositório;
* Cria uma branch com a sua feature: git checkout -b minha-feature;
* Faça commit das suas alterações: git commit -m 'feat: Minha nova feature';
* Faça push para a sua branch: git push origin minha-feature.

Depois que o merge da sua pull request for feito, você pode deletar a sua branch.


<h2> <img src="https://user-images.githubusercontent.com/38691922/77789846-93ea9c00-7042-11ea-9813-0c6bca84fd2d.png" height="30" width="30">   Licença</h2>

Esse projeto está sob a licença MIT.
