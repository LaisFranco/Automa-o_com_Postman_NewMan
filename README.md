<h1 align="center">🚀 Automação de Testes de API - Postman + Newman + GitHub Actions</h1>

<p align="center">
  <img src="https://img.shields.io/github/actions/workflow/status/LaisFranco/Automa-o_com_Postman_NewMan/main.yml?branch=main&style=for-the-badge" alt="CI Status"/>
  <img src="https://img.shields.io/badge/tests-Postman%20Collection-orange?style=for-the-badge&logo=postman" alt="Postman Tests"/>
  <img src="https://img.shields.io/badge/report-HTML-blue?style=for-the-badge" alt="HTML Report"/>
</p>

---

## 📌 Sobre o Projeto

Este projeto demonstra como automatizar testes de **API REST** utilizando:

- **Postman** → para criar as coleções de testes.  
- **Newman** → para rodar os testes em linha de comando.  
- **newman-reporter-htmlextra** → para gerar relatórios em HTML detalhados.  
- **GitHub Actions** → para integração contínua (CI/CD).  
- **GitHub Pages** → para publicação automática dos relatórios.

Cada vez que a pipeline é executada, um **novo relatório em HTML é gerado** e publicado, ficando disponível para visualização online ✅.

---

## ⚙️ Como funciona o Workflow

1. Faz checkout do repositório.  
2. Instala **Newman** e o **Reporter HTML Extra**.  
3. Executa a coleção `user.json` com as variáveis de ambiente (`postman.json` e `global.json`).  
4. Gera relatório HTML com **timestamp**.  
5. Publica automaticamente no **GitHub Pages**.  

---

## 🌐 Relatórios Online  

<p align="center">
  📊 <strong>Relatórios de Testes Automatizados</strong>  
</p>

<p align="center">
  👉 O último relatório gerado pode ser acessado pelo link abaixo:
</p>

<p align="center">
  <a href="https://laisfranco.github.io/AutomacaoPostmanNewman/" target="_blank">
    <img src="https://img.shields.io/badge/🔗%20Acesse%20o%20Relatório-1E90FF?style=for-the-badge&logo=githubpages&logoColor=white" alt="Relatório Online"/>
  </a>
</p>

---

## 🔹 Rodar no GitHub Actions (CI/CD)

Você também pode rodar os testes pelo **GitHub Actions**:

1. Vá até a aba **Actions** do repositório.  
2. Selecione o workflow **Run Postman Tests**.  
3. Clique em **Run workflow → Branch: main → Run workflow**.  

Durante a execução:  
- 📂 O pipeline cria a pasta `result/` (no CI/CD, não visível no repositório).  
- 📊 O relatório gerado é publicado automaticamente no **GitHub Pages**.


---
 ▶️ Como rodar localmente

Se quiser rodar os testes na sua máquina:

 1️⃣ Instale o Node.js
Baixe e instale a versão mais recente do **Node.js**:  
👉 [https://nodejs.org](https://nodejs.org)

```bash
# Instale o Newman e o Reporter
npm install -g newman
npm install -g newman-reporter-htmlextra

# Execute a coleção
newman run ./user.json -e ./postman.json -g ./global.json \
  --reporters cli,htmlextra \
  --reporter-htmlextra-export ./result/Report.html
```



----
## 👩‍💻 Autor(a)

Feito com ❤️ por [Laís Franco](https://github.com/LaisFranco) · QA  
🔎 Garantindo qualidade ponta a ponta, explorando bugs e transformando falhas em aprendizado.

