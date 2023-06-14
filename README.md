# Alura Challenge DevOps
Só com a ajuda do ChatGPT consegui sequer abrir este repositório kkkk.

## Como rodar o processo
- Garantir que o <a href="https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html">Java Development Kit JDK versão 17</a> está instalado no computador, assim como o <a href="https://maven.apache.org/download.cgi">maven</a>. <a href="#problemas-com-o-maven">Veja a nota abaixo caso tenha algum problema com o Maven</a>.
- Garantir que há um schema chamado 'vollmed_api' no MySQL Workbench e garantir que o arquivo /src/main/resources/application.properties está configurado com o usuário e a senha correta para o acesso do MySQL server
- Inserir diretamente no banco de dados o usuário para conseguir um token para acessar as funcionalidades do app. Eu fiz diretamente no MySQL Workbench com o código:
```
INSERT INTO usuarios (id, login, senha) VALUES (1, 'ana.souza@voll.med', '$2a$10$Y50UaMFOxteibQEYLrwuHeehHYfcoafCopUazP12.rqB41bsolF5.');
```
- Usar o comando ```mvn spring-boot:run``` no terminal
- O app está rodando na porta ```8080```.

### Problemas com o Maven
Eu tive problemas iniciais com o Maven que basicamente me desmotivaram a continuar o curso de acordo com o cronograma (que foi em Abril/23). Tive que recorrer ao ChatGPT para entender como era feita a instalação do Maven, que parece ser um gerenciador de pacotes para o Java. A instalação não é tão simples, pois dependia da criação de uma variável de sistema ```%MAVEN_HOME%```, que não estava sendo automaticamente liberada para o meu usuário no windows.

### Seeders
O app não vem com um usuário cadastrado, então não é possível acessar nenhuma rota da API. No curso de boas práticas, o instrutor cria uma entrada na tabela usuário com hardcode. Para facilitar minha vida e o teste da API quando em produção, quero gerar um Seeder, que segundo o ChatGPT, parece ser apenas mais uma versão das migrations com o flyway. Como o Spring Security usa por padrão um algoritmo de encriptação BCrypt, o seeder tem que usar uma senha que siga o mesmo padrão.
❌ Adicionar um seeder simplesmente não foi possível para a tabela de usuários, sendo necessário adicionar o usuário diretamente no banco de dados.

### Nota sobre o acesso
- O aplicativo é protegido com um token JWT, que aparentemente é gerado com usuário e senha (seguir o curso <a href="https://cursos.alura.com.br/course/spring-boot-aplique-boas-praticas-proteja-api-rest">Spring Boot 3: aplique boas práticas e proteja uma API Rest</a>)

## 📝 Licença

Projeto desenvolvido por [Alura](https://www.alura.com.br) e utilizado nos cursos de Spring Boot.

Instrutor: [Rodrigo Ferreira](https://cursos.alura.com.br/user/rodrigo-ferreira) 

Forked from: [Este Repositório](https://github.com/alura-cursos/2771-spring-boot)

---
