<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=200&section=header&text=Taha%20Hamoudi&fontSize=56&fontColor=ffffff&fontAlignY=36&desc=Full%20Stack%20Developer%20%E2%80%A2%20Java%20%E2%80%A2%20Spring%20Boot%20%E2%80%A2%20Angular&descAlignY=58&descSize=18&animation=fadeIn" width="100%" alt="Taha Hamoudi banner"/>
</p>

<p align="center">
  <a href="https://hamouditaha.github.io">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=36BCF7&center=true&vCenter=true&width=600&lines=Full+Stack+Developer+%E2%80%94+Java+%2F+Spring+Boot+%2F+Angular;Microservices+%C2%B7+Kafka+%C2%B7+Docker+%C2%B7+Kubernetes;Event-driven+systems+with+SAGA+%26+Kafka;Learning+Generative+AI%3A+Spring+AI+%C2%B7+RAG+%C2%B7+LLMs" alt="Typing SVG"/>
  </a>
</p>

<p align="center">
  <a href="https://hamouditaha.github.io"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio"/></a>
  <a href="https://linkedin.com/in/tahahamoudi"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:tahahamoudi32@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <img src="https://img.shields.io/badge/Casablanca,_Morocco-2C5364?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location"/>
  <img src="https://img.shields.io/badge/Open_to_work-2EA44F?style=for-the-badge" alt="Open to work"/>
</p>

---

## 👨‍💻 About me

```java
public class TahaHamoudi {

    String role       = "Full Stack Developer";
    String location   = "Casablanca, Morocco 🇲🇦";
    String education  = "Master's in Software Engineering, Big Data & Cloud Computing — ENSET Mohammedia (2026)";
    int    experience = 3; // years building business web applications

    String[] backend  = {"Java 17", "Spring Boot 3", "Spring Cloud", "Spring Security", "Kafka"};
    String[] frontend = {"Angular", "TypeScript"};
    String[] devops   = {"Docker", "Kubernetes", "Jenkins", "GitHub Actions"};

    String currentFocus = "Migrating monoliths to microservices";
    String learning     = "Generative AI in Java: Spring AI, LangChain4j, RAG, pgvector";
    String[] languages  = {"Arabic", "French", "English"};
}
```

- 🔁 **Latest work:** migrated the **OptiManager** business application from a Laravel monolith to **Spring Boot microservices** (Gateway, Eureka, Config Server, Docker, CI/CD) with an **Angular** front-end, during my final-year internship at HouXplore.
- 🏗️ I enjoy **distributed systems**: event-driven communication, SAGA transactions, idempotency and distributed locking.
- 🤖 Next step: adding **LLM features** (RAG assistants, semantic search) to existing Java products.

---

## 🛠️ Tech stack

<table>
  <tr>
    <td align="center" width="150"><b>Back-end</b></td>
    <td><img src="https://skillicons.dev/icons?i=java,spring,python,kafka,maven&perline=10" alt="Back-end"/></td>
  </tr>
  <tr>
    <td align="center"><b>Front-end</b></td>
    <td><img src="https://skillicons.dev/icons?i=angular,ts,js,html,css,bootstrap&perline=10" alt="Front-end"/></td>
  </tr>
  <tr>
    <td align="center"><b>Databases</b></td>
    <td><img src="https://skillicons.dev/icons?i=postgres,mysql,mongodb,redis&perline=10" alt="Databases"/></td>
  </tr>
  <tr>
    <td align="center"><b>DevOps & Cloud</b></td>
    <td><img src="https://skillicons.dev/icons?i=docker,kubernetes,jenkins,githubactions,gitlab,linux&perline=10" alt="DevOps"/></td>
  </tr>
  <tr>
    <td align="center"><b>Tools</b></td>
    <td><img src="https://skillicons.dev/icons?i=git,github,idea,vscode,postman&perline=10" alt="Tools"/></td>
  </tr>
</table>

<p>
  <img src="https://img.shields.io/badge/JUnit_5-25A162?style=flat-square&logo=junit5&logoColor=white"/>
  <img src="https://img.shields.io/badge/Mockito-78A641?style=flat-square"/>
  <img src="https://img.shields.io/badge/Testcontainers-2E4D7B?style=flat-square"/>
  <img src="https://img.shields.io/badge/SonarQube-4E9BCD?style=flat-square&logo=sonarqube&logoColor=white"/>
  <img src="https://img.shields.io/badge/Keycloak-4D4D4D?style=flat-square&logo=keycloak&logoColor=white"/>
  <img src="https://img.shields.io/badge/OAuth2_%2F_JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring_AI-6DB33F?style=flat-square&logo=spring&logoColor=white"/>
  <img src="https://img.shields.io/badge/LangChain4j-1C3C3C?style=flat-square"/>
  <img src="https://img.shields.io/badge/RAG_%2F_pgvector-336791?style=flat-square&logo=postgresql&logoColor=white"/>
</p>

---

## 🚀 Featured projects

### 🏦 [Banks: Real-time Fraud Detection System](https://github.com/hamouditaha/banks)

Digital banking platform built as **Spring Boot microservices** that communicate over **Kafka**. Money transfers are coordinated by an **orchestration-based SAGA** with compensations. **Redis** serves as the system of record, with atomic Lua debits, idempotent steps and **Redisson** distributed locks.

```mermaid
flowchart LR
    C([Client]) --> GW[API Gateway<br/>:8080]
    GW --> ACC[account-service<br/>:8081]
    GW --> ORC[orchestrator-service<br/>:8083]
    GW --> NOT[notification-service<br/>:8084]
    ORC <-->|saga commands / replies| K{{Kafka}}
    ACC <--> K
    FR[fraud-detection-service<br/>:8082] <--> K
    K -->|outcome events| NOT
    ACC & ORC & FR & NOT --> R[(Redis)]
    EU[Eureka<br/>:8761] -.service discovery.- GW
```

`Spring Boot` `Spring Cloud Gateway` `Eureka` `Kafka` `Redis` `Redisson` `SAGA` `Docker Compose`

<table>
  <tr>
    <td width="50%" valign="top">
      <h4>👥 <a href="https://github.com/hamouditaha/gestion-RH">HR Management: QR attendance &amp; payroll</a></h4>
      Employees clock in with a <b>QR code</b>. The app tracks attendance, absences and late arrivals, <b>computes monthly salaries</b> and <b>e-mails payslips</b>. Scheduled jobs mark absences automatically.
      <br/><br/>
      <code>Spring Boot</code> <code>Angular 17</code> <code>MySQL</code> <code>ZXing</code> <code>Thymeleaf</code>
    </td>
    <td width="50%" valign="top">
      <h4>🛒 <a href="https://github.com/hamouditaha/e-commerce_Microservices">E-commerce Microservices</a></h4>
      Microservices e-commerce platform, <i>in progress</i>: Docker Compose infrastructure (PostgreSQL, MongoDB, Kafka, Zipkin) and a product service with Flyway migrations.
      <br/><br/>
      <code>Spring Cloud</code> <code>Kafka</code> <code>PostgreSQL</code> <code>Docker</code>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>🏨 <a href="https://github.com/hamouditaha/hotel-management">Hotel Management System</a></h4>
      Desktop app for hotel reception: rooms, customers, check-in and check-out, staff and pick-up service.
      <br/><br/>
      <code>Java Swing</code> <code>JDBC</code> <code>MySQL</code>
    </td>
    <td width="50%" valign="top">
      <h4>📦 <a href="https://github.com/hamouditaha/ProductManager">Product Manager</a></h4>
      Desktop product catalogue with CRUD operations and live statistics, built on the MVC pattern.
      <br/><br/>
      <code>JavaFX</code> <code>FXML</code> <code>Maven</code>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>🧩 <a href="https://github.com/hamouditaha/design-patterns-builder-singleton-prototype">Design Patterns in Java</a></h4>
      Builder, thread-safe Singleton and Prototype (deep clone) patterns applied to a banking domain.
      <br/><br/>
      <code>Java 17</code> <code>Maven</code> <code>Jackson</code>
    </td>
    <td width="50%" valign="top">
      <h4>🌐 <a href="https://hamouditaha.github.io">Portfolio</a></h4>
      My personal website: experience, projects and CV.
      <br/><br/>
      <code>HTML</code> <code>CSS</code> <code>GitHub Pages</code>
    </td>
  </tr>
</table>

---

## 📊 GitHub stats

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=hamouditaha&show_icons=true&include_all_commits=true&count_private=true&theme=tokyonight&hide_border=true&border_radius=10" alt="GitHub stats"/>
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=hamouditaha&layout=compact&langs_count=8&theme=tokyonight&hide_border=true&border_radius=10" alt="Top languages"/>
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=hamouditaha&theme=tokyonight&hide_border=true&border_radius=10" alt="GitHub streak"/>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/hamouditaha/hamouditaha/output/github-snake-dark.svg"/>
    <img src="https://raw.githubusercontent.com/hamouditaha/hamouditaha/output/github-snake.svg" alt="Contribution snake"/>
  </picture>
</p>

---

## 📜 Certifications

<p>
  <img src="https://img.shields.io/badge/Claude_Code_in_Action-Anthropic-D97757?style=for-the-badge&logo=anthropic&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python_Essentials-Cisco-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white"/>
</p>

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=hamouditaha&color=2C5364&style=flat-square&label=Profile+views" alt="Profile views"/>
</p>

<p align="center"><i>💬 Open to Full Stack Java / Spring Boot opportunities — feel free to reach out!</i></p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=100&section=footer" width="100%" alt="footer"/>
