<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=130&color=0:1e293b,50:2b4c7e,100:2a7f86&section=header&animation=fadeIn" alt="header"/>

<!-- Name swaps between "Muhammad Adeen" and "MuhammadAdeen" -->
<h1 align="center">
  <a href="https://github.com/MuhammadAdeen">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=38&duration=1800&pause=2600&color=4C9BE8&center=true&vCenter=true&width=640&height=70&lines=Muhammad+Adeen;MuhammadAdeen" alt="Muhammad Adeen / MuhammadAdeen"/>
  </a>
</h1>

<p align="center">
  <a href="https://github.com/MuhammadAdeen">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=400&size=15&duration=2700&pause=1300&color=2DB8A5&center=true&vCenter=true&multiline=true&repeat=true&width=640&height=130&lines=%E2%96%B8+Full-Stack+%26+Mobile+Developer;%E2%96%B8+Building+cross-platform+apps+with+React+Native+%2B+Go;%E2%96%B8+Shipping+multi-model+AI+tools+for+the+browser;%E2%96%B8+Backend+APIs+with+Python+%26+FastAPI" alt="Typing animation"/>
  </a>
</p>

<p align="center">
  <a href="https://github.com/MuhammadAdeen"><img src="https://img.shields.io/badge/GitHub-2DB8A5?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/></a>
  <img src="https://komarev.com/ghpvc/?username=MuhammadAdeen&style=for-the-badge&color=8B7CF6&label=PROFILE+VIEWS" alt="Profile views"/>
</p>

<br/>

I build cross-platform mobile apps, AI-powered browser tools and the backend APIs behind them, somewhere between **mobile**, **AI tooling** and **backend engineering**.

> Most of my repositories are private to protect client and product code. Each project below is documented in full: what I built, the stack, my role, and the technical details. Code walkthroughs or read access are available on request.

<br/>

## Selected Work

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Vouch</h3>
      <p>B2B resource exchange app where businesses trade skills and services with an internal credit system. <b>Sole designer and developer.</b></p>
      <img src="https://img.shields.io/badge/React_Native-4C9BE8?style=flat-square" alt="React Native"/>
      <img src="https://img.shields.io/badge/Expo-4C9BE8?style=flat-square" alt="Expo"/>
      <img src="https://img.shields.io/badge/Go-4C9BE8?style=flat-square" alt="Go"/>
      <img src="https://img.shields.io/badge/Supabase-4C9BE8?style=flat-square" alt="Supabase"/>
    </td>
    <td width="33%" valign="top">
      <h3>Nexora AI</h3>
      <p>Chrome extension for contextual AI help in the browser. Chat with multiple LLMs, summarize pages, rewrite and translate selected text.</p>
      <img src="https://img.shields.io/badge/Manifest_V3-8B7CF6?style=flat-square" alt="Manifest V3"/>
      <img src="https://img.shields.io/badge/TypeScript-8B7CF6?style=flat-square" alt="TypeScript"/>
      <img src="https://img.shields.io/badge/LLM_APIs-8B7CF6?style=flat-square" alt="LLM APIs"/>
    </td>
    <td width="33%" valign="top">
      <h3>Turing · Devsinc</h3>
      <p>Backend engineering on the Turing platform: REST APIs, PostgreSQL management, automated tests and data workflows.</p>
      <img src="https://img.shields.io/badge/Python-2DB8A5?style=flat-square" alt="Python"/>
      <img src="https://img.shields.io/badge/FastAPI-2DB8A5?style=flat-square" alt="FastAPI"/>
      <img src="https://img.shields.io/badge/PostgreSQL-2DB8A5?style=flat-square" alt="PostgreSQL"/>
    </td>
  </tr>
</table>

<br/>

## Project Details

<details>
<summary><b>Vouch — B2B Business Alliance & Resource Exchange Network</b></summary>

<br/>

**What I built**

A full-stack cross-platform mobile app where businesses trade skills and services using an internal credit system called Vouch Credits. Businesses post what they need or offer, match with complementary businesses, negotiate through in-app messaging, and complete exchanges that build their Vouch Score, a reputation metric that grows with every verified trade.

**Technologies**

| Layer | Technology |
|---|---|
| Mobile | React Native · Expo · TypeScript |
| State | Zustand · AsyncStorage |
| Backend | Go · Fiber v2 |
| Database | Supabase (PostgreSQL) |
| Auth | Supabase Auth · JWT · Google OAuth · Apple OAuth |
| Realtime | Supabase Realtime |
| Storage | Supabase Storage |
| Deployment | Railway |
| Build | EAS Build (iOS + Android) |

**My role**

Sole designer and developer. I built the entire product from concept to implementation: database schema design, backend API, mobile UI, authentication flows and deployment configuration.

**Key features and technical details**

- **Vouch Credits**: atomic credit transfer through a PostgreSQL stored procedure (`transfer_vouch_credits`) that validates balances, updates both parties, logs transactions and marks the exchange complete in a single transaction, preventing race conditions and partial state
- **Vouch Score**: reputation engine that increments on every completed exchange and recalculates from average review ratings, giving businesses a visible trust signal
- **Post feed**: filterable by city, post type (need/offer) and status with server-side pagination; business metadata (name, avatar, Vouch Score) is joined at the database layer
- **Row Level Security**: every Supabase table is protected with RLS policies; businesses can only modify their own records and messages are scoped to exchange participants
- **Alliance Groups**: businesses join city- and category-based alliances for community discovery
- **Dual theme**: light mode (#355E3B green + #faf9f4 cream) and dark mode (#355E3B green + #0a0a0a black) with a system-level toggle
- **Cross-platform**: one codebase targeting iOS and Android through Expo EAS Build

</details>

<details>
<summary><b>Nexora AI — Multi-Model AI Browser Assistant</b></summary>

<br/>

**What I built**

A Chrome extension that brings contextual AI assistance directly into the browser. Users chat with multiple LLMs, switch models mid-conversation, summarize pages, rewrite selected text, translate content and get AI analysis of the current webpage, all without leaving their tab.

**Technologies**

| Layer | Technology |
|---|---|
| Extension | Chrome Extensions Manifest V3 |
| Language | JavaScript · TypeScript |
| AI | Multiple LLM APIs (model switching) |
| Browser APIs | Chrome Extensions API · Content Scripts · Background Service Workers |
| Page analysis | DOM parsing · contextual content extraction |

**My role**

I built the full extension: content scripts, background service worker, popup UI and all LLM API integrations. I designed the model-switching architecture and the webpage context extraction pipeline.

**Key features and technical details**

- **Multi-model support**: multiple LLM APIs behind a unified interface; users switch models without losing conversation context
- **Contextual page analysis**: content scripts parse the active tab's DOM and pass relevant page content to the model, enabling accurate in-page Q&A and summarization
- **Background service worker**: handles API calls and state management in the background, keeping the popup lightweight and responsive
- **Manifest V3 compliant**: built to Chrome's current extension security model with declarative net request rules and scoped permissions
- **Inline actions**: rewrite, translate and summarize triggered directly on selected text from the context menu

</details>

<details>
<summary><b>Turing — Backend Engineering at Devsinc (Oct 2024 – Jun 2025)</b></summary>

<br/>

**What I built**

At Devsinc I worked on Turing, a platform involving API development, database management and integration with external applications. The work covered building and maintaining REST APIs, managing PostgreSQL databases, writing automated tests and running data workflows in Google Colab.

**Technologies**

| Layer | Technology |
|---|---|
| Language | Python |
| APIs | FastAPI · REST |
| Database | PostgreSQL · SQL |
| Data workflows | Google Colab |
| Testing | Automated testing frameworks |
| Version control | Git |

**My role**

Backend engineer responsible for API development and database management. I wrote integration code connecting the platform with third-party applications, built automated test suites covering edge cases and failure scenarios, and used Google Colab for data processing and validation workflows.

**Key features and technical details**

- **REST API development**: designed and implemented endpoints following REST conventions with proper status codes, error handling and request validation
- **Database management**: wrote and optimized SQL queries, managed schema changes and maintained PostgreSQL databases across environments
- **Automated testing**: built test suites with mock code and edge-case coverage to validate API behavior under failure conditions and unexpected input
- **Third-party integrations**: developed integration layers connecting the platform with external services and applications
- **Data workflows**: used Google Colab notebooks for data extraction, transformation and validation

</details>

<br/>

## Stack

<p>
  <img src="https://skillicons.dev/icons?i=react,ts,js,go,py,fastapi,postgres,supabase,git,github&theme=dark" alt="Tech stack"/>
</p>

<sub><b>Also:</b> Expo · EAS Build · Zustand · Fiber v2 · Supabase Auth / Realtime / Storage · Chrome Extensions Manifest V3 · LLM APIs · Railway</sub>

<br/>

## Experience

- Backend Engineer · **Devsinc** (Oct 2024 – Jun 2025)
- Sole designer and developer · **Vouch**
- Creator · **Nexora AI**

<br/>

## Activity

<p align="center">
  <img height="150" src="https://github-readme-stats.vercel.app/api?username=MuhammadAdeen&show_icons=true&hide_border=true&theme=transparent&title_color=4C9BE8&text_color=8B949E&icon_color=2DB8A5&bg_color=00000000" alt="GitHub stats"/>
  <img height="150" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MuhammadAdeen&layout=compact&hide_border=true&theme=transparent&title_color=4C9BE8&text_color=8B949E&bg_color=00000000" alt="Top languages"/>
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=MuhammadAdeen&hide_border=true&background=00000000&stroke=4C9BE855&ring=4C9BE8&fire=E8A24C&currStreakNum=4C9BE8&sideNums=8B949E&currStreakLabel=2DB8A5&sideLabels=8B949E&dates=8B949E&refresh=2" alt="GitHub streak"/>
</p>

<!-- Animated snake: needs the workflow in .github/workflows/snake.yml -->
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/MuhammadAdeen/MuhammadAdeen/output/github-snake-dark.svg"/>
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/MuhammadAdeen/MuhammadAdeen/output/github-snake.svg"/>
    <img alt="Contribution snake" src="https://raw.githubusercontent.com/MuhammadAdeen/MuhammadAdeen/output/github-snake-dark.svg"/>
  </picture>
</p>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=110&color=0:2a7f86,50:2b4c7e,100:1e293b&section=footer&reversal=true" alt="footer"/>
