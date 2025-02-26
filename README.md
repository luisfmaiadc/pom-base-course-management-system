<h1 align="center">pom-base-course-management-system</h1>

<p align="center" style="margin-bottom: 20;">
    <img src="https://img.shields.io/badge/Apache%20Maven-C71A36?style=for-the-badge&logo=Apache%20Maven&logoColor=white" alt="Apache Maven" />
</p>

<p align="center">Este projeto serve como o repositório central de dependências para o <b>Sistema de Gerenciamento de Cursos</b>, um sistema baseado em arquitetura de microsserviços desenvolvido com <b>Java 21</b> e <b>Spring Boot 3.4.2</b> como framework.</p>

<h2>📌 Visão Geral do Projeto</h2>
<p align="justify">O Sistema de Gerenciamento de Cursos é composto por múltiplos microsserviços que operam de forma independente, cada um com seu próprio banco de dados PostgreSQL, e que se comunicam via API Gateway. A autenticação das requisições é feita por meio de tokens JWT, garantindo controle de acesso com base em roles de usuário.</p>

<h2>🚀 Tecnologias Utilizadas</h2>

- <b>Java 21 + Spring Boot 3.4.2</b>
- <b>Spring Cloud</b> (para Service Discovery e API Gateway)
- <b>PostgreSQL</b> (SGBD utilizado por todos os microsserviços)
- <b>Flyway</b> (para versionamento e gerenciamento de migrations)
- <b>Autenticação JWT</b> (com controle de acesso por roles)
- <b>Eureka Service Discovery</b> (para facilitar a comunicação entre serviços)

<h2>🏗️ Estrutura do Sistema</h2>

<h3>🔹 pom-base-course-management-system</h3>
<p>Gerencia as dependências compartilhadas entre os microsserviços, garantindo consistência e padronização nas versões das bibliotecas utilizadas.</p>

<h3>🔹 sboot-cms-teacher-ms</h3>
<p>Responsável pelo gerenciamento de instrutores, permitindo cadastro, atualização, inativação e validação de registro.</p>

<h3>🔹 sboot-cms-student-ms</h3>
<p>Gerencia as operações relacionadas aos alunos, como cadastro, atualização, matrícula em cursos e inativação de matrícula.</p>

<h3>🔹 sboot-cms-course-ms</h3>
<p>Administra o ciclo de vida dos cursos, incluindo cadastro, atualização, validação e inativação.</p>

<h3>🔹 sboot-cms-service-discovery</h3>
<p>Implementação de um servidor Eureka para descoberta de serviços, permitindo que os microsserviços se localizem dinamicamente.</p>

<h3>🔹 sboot-cms-api-gateway</h3>
<p>Centraliza as requisições para os microsserviços, além de realizar autenticação via JWT, protegendo endpoints e validando permissões de acesso.</p>

<h2>🎯 Objetivo do pom-base-course-management-system</h2>
<p>Este módulo foi criado para simplificar a manutenção das dependências em todos os microsserviços do sistema. Ele funciona como um POM pai, garantindo que cada serviço utilize versões consistentes das bibliotecas necessárias.</p>

<h2>📜 Exemplo de Uso</h2>
<p>Nos microsserviços, basta configurar a herança no pom.xml:</p>

```xml
<parent>
    <groupId>com.portfolio.luisfmdc</groupId>
    <artifactId>pom-base-course-management-system</artifactId>
    <version>1.0.0-SNAPSHOT</version>
</parent>
```

<p>A quesito informativo é dessa forma que todos os microsserviços herdam automaticamente as dependências e versões definidas no <code>pom-base-course-management-system</code>.</p>

<h2>🤝 Colaboradores</h2>
<p style="margin-bottom: 20;">Este projeto marca o meu retorno ao desenvolvimento de portfólio após um período focado em adquirir conhecimento sobre arquitetura de microsserviços. Durante esse tempo, me aprofundei no uso do <code>pom.xml</code> e na herança entre módulos, além de explorar conceitos avançados para estruturar sistemas distribuídos. O resultado é um projeto bastante completo, que consolida boa parte do que aprendi. No futuro, pretendo refiná-lo ainda mais, incorporando melhorias e novas práticas para torná-lo ainda mais robusto e eficiente.</p>
<table>
  <tr>
    <td align="center">
      <a href="https://github.com/luisfmaiadc">
        <img src="https://github.com/user-attachments/assets/b38280aa-a62a-4c33-bc98-8cae0e67fd75" width="100px;" alt="Luis Felipe Maia da Costa Profile Picture"/><br>
        <sub>
          <b>Luis Felipe Maia da Costa</b>
        </sub>
      </a>
    </td>
  </tr>
</table>