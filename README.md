# Alura Challenge DevOps
Só com a ajuda do ChatGPT consegui sequer abrir este repositório kkkk.

## Como rodar o processo
- Garantir que há um schema chamado 'vollmed_api' no MySQL Workbench e garantir que o arquivo /src/main/resources/application.properties está configurado com o usuário e a senha correta para o acesso do MySQL server
- Usar o comando ```mvn spring-boot:run``` no terminal
- Cheguei até aqui e o app parece estar rodando, mas ainda preciso descobrir como fazer testes no Hopscotch
- O app está rodando na porta ```8080```.
- O aplicativo é protegido com um token JWT, que aparentemente é gerado com usuário e senha (seguir o curso <a href="https://cursos.alura.com.br/course/spring-boot-aplique-boas-praticas-proteja-api-rest">Spring Boot 3: aplique boas práticas e proteja uma API Rest</a>)

### Problemas com o Maven
Eu tive problemas iniciais com o Maven que basicamente me desmotivaram a continuar o curso de acordo com o cronograma (que foi em Abril/23). Tive que recorrer ao ChatGPT para entender como era feita a instalação do Maven, que parece ser um gerenciador de pacotes para o Java. A instalação não é tão simples, pois dependia da criação de uma variável de sistema ```%MAVEN_HOME%```, que não estava sendo automaticamente liberada para o meu usuário no windows.

## 📝 Licença

Projeto desenvolvido por [Alura](https://www.alura.com.br) e utilizado nos cursos de Spring Boot.

Instrutor: [Rodrigo Ferreira](https://cursos.alura.com.br/user/rodrigo-ferreira) 

---
