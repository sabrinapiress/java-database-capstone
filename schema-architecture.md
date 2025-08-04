## Seção 1: Resumo da arquitetura

Este aplicativo Spring Boot utiliza controladores tanto MVC quanto REST. Templates Thymeleaf são usados para os painéis de Admin e Médico, enquanto APIs REST atendem todos os outros módulos. O aplicativo interage com dois bancos de dados—MySQL (para dados de paciente, médico, consultas e admin) e MongoDB (para prescrições). Todos os controladores encaminham as solicitações por meio de uma camada de serviço comum, que por sua vez delega para os repositórios apropriados. MySQL utiliza entidades JPA, enquanto MongoDB utiliza modelos de documentos.


## Seção 2: Fluxo de dados e controle numerado

1. O usuário acessa os painéis de Admin ou de Consulta.
2. A ação é roteada para o controlador Thymeleaf ou REST apropriado.
3. O controlador chama a camada de serviço correspondente.
4. A camada de serviço processa a lógica de negócios necessária.
5. A camada de serviço interage com os repositórios JPA (MySQL) ou modelos de documentos (MongoDB).
6. Os dados são recuperados ou atualizados nos bancos de dados conforme necessário.
7. A resposta é enviada de volta ao usuário via template Thymeleaf ou como resposta REST.
