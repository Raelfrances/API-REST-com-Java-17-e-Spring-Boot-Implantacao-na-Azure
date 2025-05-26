# API-REST-com-Java-17-e-Spring-Boot-Implantacao-na-Azure
Este projeto demonstra a construção e a implantação de uma API REST utilizando Java 17 (LTS), Spring Boot 3, Spring Data JPA e documentação com OpenAPI (Swagger). A aplicação está hospedada na Microsoft Azure, garantindo escalabilidade e desempenho.

---

🔹 Tecnologias utilizadas:

Java 17 🚀

Spring Boot 3 ⚙️

Spring Data JPA 🗄️

PostgreSQL/MySQL 🛢️

OpenAPI (Swagger) 📄

Azure App Service ☁️

Azure PostgreSQL (Banco de Dados)
---

🚀 Como executar o projeto?

1️⃣ Pré-requisitos
Java 17+ instalado

Maven ou Gradle configurado

Azure CLI instalado (Download)

2️⃣ Clonar o repositório
````
bash
git clone https://github.com/seu-usuario/minha-api.git
cd minha-api

````

---

3️⃣ Configurar banco de dados
````
🔹 Para PostgreSQL no Azure, adicione ao application.properties:

properties
spring.datasource.url=jdbc:postgresql://meubanco.postgres.database.azure.com:5432/meudb
spring.datasource.username=admin
spring.datasource.password=SenhaForte123
🌐 Implantação na Azure
````
---

Criar recursos no Azure App Service
````
bash
az group create --name MeuGrupoRecursos --location "East US"
az appservice plan create --name MeuPlano --resource-group MeuGrupoRecursos --sku B1 --is-linux
az webapp create --name MinhaAPI --resource-group MeuGrupoRecursos --plan MeuPlano --runtime "JAVA|17-java17"
Gerar .jar da API
bash
mvn clean package
Fazer o Deploy na Azure
bash
az webapp deploy --resource-group MeuGrupoRecursos --name MinhaAPI --src-path target/minha-api.jar
````
---

Testar a API na nuvem
````
Acesse:

https://minhaapi.azurewebsites.net
````
---
----

📚 Endpoints principais
````
Método	Endpoint	Descrição
GET	/api/clientes	Listar clientes
POST	/api/clientes	Criar novo cliente
GET	/api/clientes/{id}	Buscar cliente por ID
PUT	/api/clientes/{id}	Atualizar cliente
DELETE	/api/clientes/{id}	Excluir cliente
````

