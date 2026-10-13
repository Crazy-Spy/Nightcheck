<div align="center">
  <img src="pin.png" alt="Nightcheck Logo" width="96" height="96">
  <h1>Nightcheck</h1>
  <p><strong>Onde a Cris vai passar a noite?</strong></p>
  <p>Aplicação web simples, rápida e moderna para consulta de escala de plantão e pernoite.</p>

  <p>
    <a href="https://crazy-spy.github.io/Nightcheck/"><strong>Acessar Demonstração Online »</strong></a>
  </p>
</div>

---

## 📌 Sobre o Projeto

O **Nightcheck** foi criado para resolver uma dúvida recorrente no dia a dia: saber com antecedência se a Cris **dorme em casa** ou **no plantão**, além de indicar os horários previstos de chegada e saída para cada data.

A aplicação foi desenvolvida em **HTML5, CSS3 e JavaScript puro (Vanilla JS)**, sem dependências externas pesadas, com foco em simplicidade, velocidade e uma experiência de usuário (UX) agradável no celular e no computador.

---

## ✨ Funcionalidades

- 🏠 **Status Claro e Direto**:
  - **Em Casa**: Indica que ela passa a noite em casa e *Chega em casa às 17h* (vindo do plantão).
  - **Plantão (Dorme Fora)**: Indica a noite de plantão e que ela *Está em casa até as 19h30.*
- 📅 **Previsão para 7 Dias**:
  - Mini-calendário interativo com os próximos dias.
  - Exibe dia da semana, data, status (`Em casa` ou `Plantão`) e horários (`Chega às 17h` / `Sai às 19h30`).
  - Toque/clique em qualquer cartão da previsão para ver os detalhes daquele dia imediatamente no card principal.
- 🧭 **Navegação Intuitiva por Datas**:
  - Botões rápidos: `◀ Ontem`, `Hoje` e `Amanhã ▶`.
  - Saltos rápidos de semana: `⏪ -7 dias` e `+7 dias ⏩`.
  - Seletor de data (`<input type="date">`) integrado e sincronizado em tempo real.
- 🌓 **Modo Escuro / Claro (Dark Mode)**:
  - Alternância com um toque (botão ☀️ / 🌙 no cabeçalho).
  - Detecção automática da preferência do sistema operacional (`prefers-color-scheme`).
  - Preferência salva automaticamente no navegador (`localStorage`).
- 📱 **PWA (Progressive Web App)**:
  - Suporte a instalação na tela inicial do smartphone (Android / iOS) via `manifest.json`.
  - Abre em tela cheia (modo *standalone*), funcionando como um aplicativo nativo.
- ♿ **Acessibilidade e Usabilidade**:
  - Elementos de toque com área confortável para dedos em telas mobile (mínimo de 44px–48px).
  - Textos com alto contraste e navegação navegável por teclado (`Enter` / `Espaço`).

---

## ⚙️ Regra de Negócio

A lógica do plantão segue um ciclo alternado de **dia sim / dia não**, calibrado a partir da data-base:

* **Data de Referência**: `01/09/2024` (Dormiu em casa)
* **Cálculo**:
  * Dias pares de diferença em relação à data-base $\rightarrow$ **Dorme em Casa** (`Chega em casa às 17h`).
  * Dias ímpares de diferença em relação à data-base $\rightarrow$ **Plantão** (`Está em casa até as 19h30.`).
* O cálculo é feito com datas normalizadas ao meio-dia (`12:00:00`), evitando inconsistências de fuso horário UTC ou horário de verão.

---

## 📁 Estrutura de Arquivos

```text
Nightcheck/
├── index.html      # Estrutura semântica e lógica JavaScript da aplicação
├── 404.html        # Redirecionamento automático para links e favoritos antigos
├── styles.css      # Estilos modernos, variáveis CSS, temas claro/escuro e responsividade
├── manifest.json   # Configuração de PWA (Web App Manifest) para instalação no celular
├── pin.png         # Ícone oficial da aplicação (512x512)
└── README.md       # Documentação do projeto
```

---

## 🚀 Como Executar Localmente

Como o projeto é 100% estático (não requer compiladores nem Node.js), basta abrir o arquivo no seu navegador favorito:

1. Clone o repositório:
   ```bash
   git clone https://github.com/Crazy-Spy/Nightcheck.git
   ```
2. Acesse a pasta do projeto:
   ```bash
   cd Nightcheck
   ```
3. Abra o arquivo `index.html`:
   - No Windows: duplo clique no arquivo ou execute `start index.html`
   - Ou utilize extensões como o *Live Server* do VS Code.

---

## 📱 Como Instalar no Celular

### No Google Chrome / Android:
1. Abra o site no Chrome do celular.
2. Toque no menu de três pontos no canto superior direito.
3. Selecione **"Adicionar à tela inicial"** ou **"Instalar aplicativo"**.

### No Safari / iOS (iPhone):
1. Abra o site no Safari.
2. Toque no botão de **Compartilhar** (ícone do quadrado com a seta para cima).
3. Role para baixo e selecione **"Adicionar à Tela de Início"**.

---

## 📄 Licença

Distribuído sob direitos reservados &copy; Cris.

