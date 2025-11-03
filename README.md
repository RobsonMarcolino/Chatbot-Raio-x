<!-- Título com o GIF alinhado ao centro -->
<!-- Título com o GIF alinhado ao centro -->

<div align="center">
<img src="[https://media3.giphy.com/media/v1.Y2lkPWVjZjA1ZTQ3ZHJ1eGZkaHRuM2cyZ3FrOW40eG92MWExNGNncDl3bDl6dWs3Z3BxNyZlcD12MV9zdGlja2Vyc19zZWFyY2gmY3Q9cw/4NCmkwMuPoJSBzyIt8/giphy.webp](https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExeTI3eTltZGVzM2VxOWYxMWIxb2ozazl3dG01dHI3N2RjdW44cjkwOCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/8lUe197VNH9i7e4UCZ/giphy.gif)" width="150" alt="Robô IA"/>

  <h1>
    <strong>Raio-X Score 5 (Direta MG)</strong>
  </h1>
  <p>
    Um chatbot inteligente para consulta de performance e análise de dados de estabelecimentos.
  </p>
</div>

<!-- Badges/Escudos de Tecnologias -->
<div align="center">
  <img src="[https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)" alt="HTML5"/>
  <img src="[https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)" alt="Tailwind CSS"/>
  <img src="[https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)" alt="JavaScript"/>
  <img src="[https://img.shields.io/badge/Google_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white](https://img.shields.io/badge/Google_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)" alt="Google Gemini"/>
  <img src="[https://img.shields.io/badge/Google_Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white](https://img.shields.io/badge/Google_Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)" alt="Google Sheets"/>
</div>

<br>

## 🎯 Sobre o Projeto

O **Raio-X Score 5** é uma aplicação web (PWA) de página única (SPA) desenhada para fornecer acesso rápido e inteligente aos dados de performance de vendas da Direta MG.

O utilizador (vendedor, supervisor) pode simplesmente digitar o **Código EG** de um estabelecimento e o chatbot retorna:
1.  Informações cadastrais (Rede, Nome Fantasia).
2.  Dados da Equipe responsável (Coordenador, Supervisor).
3.  Métricas de Performance e Execução (Share, Atendimento, COB HDW, etc.).
4.  Uma **análise de IA** (via Google Gemini) com Pontos Fortes e Pontos de Atenção.

Este projeto foi construído inteiramente em **HTML, CSS (Tailwind) e JavaScript puro**, sem a necessidade de frameworks complexos, e é totalmente responsivo (mobile-first).

---

## ✨ Funcionalidades Principais

-   **🤖 Interface de Chat Intuitiva:** Uma tela de boas-vindas amigável e uma tela de chat que imita um smartphone.
-   **📊 Consulta de Dados em Tempo Real:** Busca informações diretamente de uma planilha Google Sheets (publicada como CSV).
-   **🧠 Análise com IA (Gemini):** Fornece insights acionáveis (Pontos Fortes 🟢 e Pontos de Atenção 🔴) sobre a performance do estabelecimento.
-   **📱 Design Responsivo (Mobile-First):** Funciona perfeitamente em telemóveis, tablets e desktops.
-   **🔮 Visual Moderno:** Tema "Ambev Tech" (Dourado/Preto) com animações de fundo, partículas e efeitos de "glassmorphism".

---

## 🛠️ Como Funciona (Arquitetura)

O fluxo de dados é simples, mas eficaz, e contorna as limitações de segurança do navegador (CORS) sem um backend dedicado:

1.  **Frontend (index.html):** O utilizador digita o Código EG.
2.  **Proxy CORS:** A aplicação usa um proxy (ex: `api.allorigins.win`) para buscar a planilha Google Sheet (publicada como CSV). Isso é necessário porque o Google não permite a leitura direta do CSV via `fetch` do navegador.
3.  **Google Sheets (Base de Dados):** A planilha CSV é lida, e os dados do Código EG são encontrados.
4.  **Google Gemini API:** Os dados de performance são enviados para a API do Google Gemini.
5.  **Análise de IA:** A IA retorna a análise formatada em Pontos Fortes e Pontos de Atenção.
6.  **Frontend (index.html):** Os dados e a análise são exibidos para o utilizador.

---

## 🚀 Como Executar

Este projeto não requer instalação de pacotes ou builds.

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/RobsonMarcolino/Chatbot-Raio-x.git
    ```

2.  **Navegue até a pasta:**
    ```bash
    cd Chatbot-Raio-x
    ```

3.  **Abra o arquivo:**
    Simplesmente abra o ficheiro `index.html` no seu navegador de preferência (Chrome, Firefox, Edge, etc.).

> **Nota:** Para que a busca na planilha e a análise de IA funcionem, o projeto precisa ser hospedado (como no **GitHub Pages**, Vercel, Netlify) ou executado num servidor local (como a extensão "Live Server" do VS Code). Abrir o ficheiro diretamente do disco (`file:///...`) pode causar erros de segurança (CORS).
