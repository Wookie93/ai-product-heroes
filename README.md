<div align="center">
  <p>
    <strong>
      <a href="#strategia-produktowa-flowcraft--ai-product-heroes-certification-project">🇵🇱 Czytaj po polsku</a>
      &nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
      <a href="#flowcraft-product-strategy--ai-product-heroes-certification-project">🇬🇧 Read in English</a>
    </strong>
  </p>
</div>

---

# Strategia Produktowa FlowCraft – AI Product Heroes Certification Project

**Rola:** Product Manager  
**Cel:** Podniesienie rocznej retencji klientów z **78% do 90%**.  
**Prototyp:** [👉 **Zobacz Live Demo (v0)**](https://v0-flow-craft-task-management-three.vercel.app/)

### 📝 Streszczenie Projektu
Projekt ten prezentuje kompleksowy proces strategii produktowej (Product Discovery & Strategy) mający na celu rozwiązanie problemu churnu w skalującym się startupie B2B SaaS. Wykorzystując **AI Agents** do symulacji wywiadów oraz automatyzację **n8n** do analizy rynku, zidentyfikowano lukę w koordynacji międzyzespołowej ("Paradoks Prostoty"). Na podstawie tych danych, przy użyciu frameworków **OST** i **RICE**, zaprojektowano i zweryfikowano prototypem **"Pakiet Koordynacji"**, który pozwala rosnącym zespołom na zarządzanie złożonością bez utraty prostoty narzędzia.

---

## Spis Treści
1. [Problem: "Wyrastanie" z Narzędzia](#1-problem-wyrastanie-z-narzędzia)
2. [Discovery & Analiza Danych](#2-discovery--analiza-danych)
3. [Definiowanie Możliwości (Opportunity Solution Tree)](#3-definiowanie-możliwości-opportunity-solution-tree)
4. [Ideacja i Rozwiązania](#4-ideacja-i-rozwiązania)
5. [Priorytetyzacja RICE](#5-priorytetyzacja-rice)
6. [Strategiczna Rekomendacja: "Pakiet Koordynacji"](#6-strategiczna-rekomendacja-pakiet-koordynacji)
7. [Użyte Narzędzia](#użyte-narzędzia)

---

## 1. Problem: "Wyrastanie" z Narzędzia

FlowCraft wygrał rynek prostotą, stając się ulubionym narzędziem małych startupów. Jednak dane pokazały niepokojący trend: gdy firmy osiągały skalę 30-50 pracowników, migrowały do konkurencji (Jira, Linear), mimo że uwielbiały nasz UX.

**Kluczowe wyzwanie ("Paradoks Prostoty"):** Jak dodać głębię funkcjonalną niezbędną dla większych zespołów, nie niszcząc prostoty, za którą klienci nas wybrali?

## 2. Discovery & Analiza Danych

Proces badawczy wykorzystywał zaawansowane techniki AI do symulacji i analizy danych:

* **Analiza Rynku (Automatyzacja AI):** Wykorzystano integrację **n8n** do przeszukania wybranych subredditów pod kątem problemów użytkowników konkurencyjnych narzędzi. Zebrane dane przetworzono w **NotebookLLM**, identyfikując **5 kluczowych pain pointów** branży.
* **Analiza Jakościowa (Symulacja AI):** Przeprowadzono wywiady pogłębione (IDI) z wykorzystaniem **syntetycznych użytkowników (AI Agents)**, którzy wcielili się w role utraconych klientów (Michał W. - PM, Jan - Founder).
* **Synteza:** Wnioski z wywiadów zostały przeanalizowane i pogrupowane tematycznie metodą **Affinity Mapping**, a następnie skonfrontowane z ilościowymi danymi rynkowymi.

**Kluczowe Wnioski (Insights):**
1.  **Problem "Osobnych Wysp":** Każda tablica w FlowCraft działała w izolacji. Menedżerowie nie widzieli postępu inicjatyw przecinających wiele zespołów (Dev + Marketing + QA).
2.  **Protezy Excelowe:** Klienci masowo eksportowali dane do arkuszy kalkulacyjnych, aby raportować postępy i zarządzać zależnościami – to silny sygnał niezaspokojonej potrzeby (*Jobs to be Done*).
3.  **Ryzyko Audytowe:** Brak historii zmian dla całych inicjatyw generował ryzyko w branżach regulowanych (np. MedTech), zmuszając klientów do odejścia.

## 3. Definiowanie Możliwości (Opportunity Solution Tree)

Zamiast wdrażać losowe funkcje, zdefiniowaliśmy 6 kluczowych obszarów (Opportunities), które bezpośrednio wpływają na churn w segmencie 30-50 osób:

1.  **Widok "z lotu ptaka":** Zapewnienie wglądu w postęp inicjatyw międzyzespołowych.
2.  **Zarządzanie Zależnościami:** Wizualizacja i zarządzanie blokadami między zadaniami.
3.  **Raportowanie i Audyt:** Zastąpienie "protez" Excela i zapewnienie historii zmian.
4.  **Automatyzacja Workflow:** Redukcja manualnej koordynacji ("work-about-work").
5.  **Onboarding:** Redukcja tarcia dla nowych zespołów (edukacja i szablony).
6.  **Integracje:** Głęboka synchronizacja z ekosystemem (GitHub, Kalendarz, Slack).

## 4. Ideacja i Rozwiązania

Dla każdego obszaru wygenerowaliśmy zestaw rozwiązań. Oto kluczowe z nich:

* **Dla Widoku Strategicznego:** Prosty system etykiet agregujących (1A) vs. Nowy obiekt "Inicjatywa" (1B).
* **Dla Zależności:** Proste powiązania liniowe "Blokuje/Jest Blokowane" (2A) vs. Automatyzacja propagacji statusu (2B).
* **Dla Raportowania:** Zaawansowane filtrowanie i zapisane widoki (3C) vs. Dedykowana platforma dashboardów (3A).
* **Dla Automatyzacji:** Gotowe szablony automatyzacji (4C) vs. Dedykowany silnik zadań cyklicznych (4B).

## 5. Priorytetyzacja RICE

Zastosowaliśmy framework RICE, kalibrując wskaźniki pod realia firmy (Reach = liczba firm, Effort = osobo-miesiące).

**Top 5 Wyników RICE:**

| Rank | Rozwiązanie | RICE Score | Dlaczego wygrało? |
| :--- | :--- | :--- | :--- |
| **1** | **Zaawansowane Filtrowanie i Zapisane Widoki (3C)** | **600** | Ogromny zasięg, niski koszt wdrożenia, natychmiastowa wartość (zastępuje Excela). |
| **2** | **Proste Powiązania Liniowe (2A)** | **350** | Krytyczne dla koordynacji pracy, relatywnie proste w implementacji (Effort: 2). |
| **3** | **Dedykowany Silnik Zadań Cyklicznych (4B)** | **333.3** | Rozwiązuje bardzo częsty, irytujący ból klientów ("low hanging fruit"). |
| **4** | **Prosty System Etykiet Agregujących (1A)** | **320** | Umożliwia "widok z lotu ptaka" bez budowania skomplikowanych nowych obiektów (Inicjatyw). |
| **5** | **Ulepszona Integracja z Komunikatorami (6C)** | **216.7** | Wspiera "Quick Capture" i przepływ informacji na Slack/Teams. |

## 6. Strategiczna Rekomendacja: "Pakiet Koordynacji"

Analiza strategiczna wykazała, że wdrożenie *tylko* zwycięzcy rankingu (Filtrowanie) byłoby niewystarczające, aby zatrzymać churn w segmencie 30-50 osób. Filtrowanie daje *dostęp* do danych, ale nie zarządza *przepływem* pracy.

**Ostateczna Decyzja:** Wdrożenie **zintegrowanego pakietu funkcji (MVP)**:

1.  **Filtrowanie 2.0 (Dostęp):** Aby znaleźć igłę w stogu siana.
2.  **Zależności Liniowe (Blokady):** Aby zapobiec chaosowi i blokowaniu pracy między zespołami.
3.  **Etykiety Agregujące (Widoczność):** Aby dać menedżerom wgląd w postęp inicjatyw na jednym ekranie.

*Zadania Cykliczne (Rank #3) zostały zakolejkowane jako osobna ścieżka ("Quick Win").*

### 🎨 Prototypowanie (v0)
Aby zweryfikować założenia, wykorzystano narzędzie **v0** do wygenerowania **interaktywnego prototypu High-Fidelity** "Pakietu Koordynacji". Pozwoliło to na natychmiastową wizualizację rozwiązania i sprawdzenie, czy zachowuje ono "DNA Prostoty" FlowCraft przed rozpoczęciem prac deweloperskich.

👉 **[Zobacz Interaktywny Prototyp (v0)](https://v0-flow-craft-task-management-three.vercel.app/)**

## 7. Użyte Narzędzia
* **Data Gathering:** n8n (Reddit scraping integration).
* **AI Analysis:** NotebookLLM (Data synthesis & Pain Point extraction).
* **Simulation:** Synthetic AI Users (Simulated Customer Interviews).
* **Strategy:** Opportunity Solution Tree (OST), Affinity Mapping, RICE Framework.
* **Prototyping:** v0 (Generative UI).

<br>
<br>

---

<br>
<br>

# FlowCraft Product Strategy – AI Product Heroes Certification Project

**Role:** Product Manager  
**Goal:** Increase annual customer retention from **78% to 90%**.  
**Prototype:** [👉 **View Live Demo (v0)**](https://v0-flow-craft-task-management-three.vercel.app/)

### 📝 Project Abstract
This project showcases an end-to-end Product Discovery & Strategy process aimed at arresting churn in a scaling B2B SaaS startup. Leveraging **AI Agents** for customer simulation and **n8n automation** for market analysis, we identified a critical cross-team coordination gap (the "Simplicity Paradox"). Based on these insights, using **OST** and **RICE** frameworks, we designed and validated a **"Coordination Bundle"**—a solution that enables scaling teams to manage complexity without losing the tool's core simplicity.

---

## Table of Contents
1. [The Problem: "Outgrowing" the Tool](#1-the-problem-outgrowing-the-tool)
2. [Discovery & Data Analysis](#2-discovery--data-analysis)
3. [Defining Opportunities (Opportunity Solution Tree)](#3-defining-opportunities-opportunity-solution-tree)
4. [Ideation & Solutions](#4-ideation--solutions)
5. [RICE Prioritization](#5-rice-prioritization)
6. [Strategic Recommendation: The "Coordination Bundle"](#6-strategic-recommendation-the-coordination-bundle)
7. [Tools Used](#tools-used)

---

## 1. The Problem: "Outgrowing" the Tool

FlowCraft won the market with simplicity, becoming the go-to tool for small tech startups. However, data revealed a concerning trend: once companies reached a scale of 30-50 employees, they migrated to competitors (Jira, Linear), even though they loved our UX.

**Key Challenge ("The Simplicity Paradox"):** How to add the functional depth required by larger teams without destroying the simplicity that customers chose us for?

## 2. Discovery & Data Analysis

We employed a data triangulation approach combining qualitative and quantitative insights with AI automation:

* **Market Analysis (AI Automation):** Used **n8n** integration to scrape selected subreddits for competitor user complaints. This data was fed into **NotebookLLM**, which synthesized and identified **5 key pain points** driving churn.
* **Qualitative Analysis (AI Simulation):** Conducted in-depth interviews (IDI) with **synthetic users (AI Agents)** acting as churned customer personas (Product Manager, Founder).
* **Synthesis:** Interview findings were analyzed using **Affinity Mapping** to cluster themes and then validated against quantitative market data.

**Key Insights:**
1.  **The "Isolated Islands" Problem:** Each Kanban board in FlowCraft functioned in isolation. Managers lacked visibility into initiatives that spanned multiple teams (Dev + Marketing + QA).
2.  **Excel Crutches:** Customers were exporting data to spreadsheets to report progress and manage dependencies—a strong signal of unmet needs (*Jobs to be Done*).
3.  **Audit Risk:** The lack of change history for entire initiatives created risks in regulated industries (e.g., MedTech), forcing customers to leave.

## 3. Defining Opportunities (Opportunity Solution Tree)

Instead of implementing random features, we defined 6 key Opportunity areas that directly impact churn in the 30-50 employee segment:

1.  **Bird's-eye View:** Providing visibility into the progress of cross-team initiatives.
2.  **Dependency Management:** Visualizing and managing blockers between tasks.
3.  **Reporting & Audit:** Replacing Excel "crutches" and ensuring change history.
4.  **Workflow Automation:** Reducing manual coordination overhead ("work-about-work").
5.  **Onboarding:** Reducing friction for new teams (education and templates).
6.  **Integrations:** Deep synchronization with the ecosystem (GitHub, Calendar, Slack).

## 4. Ideation & Solutions

For each opportunity, we generated a set of solutions. Key considerations included:

* **For Strategic View:** Simple Aggregating Labels (1A) vs. New "Initiative" Object (1B).
* **For Dependencies:** Simple Linear Links "Blocks/Is Blocked" (2A) vs. Automated Status Propagation (2B).
* **For Reporting:** Advanced Filtering & Saved Views (3C) vs. Dedicated Dashboard Platform (3A).
* **For Automation:** Pre-built Automation Templates (4C) vs. Dedicated Recurring Tasks Engine (4B).

## 5. RICE Prioritization

We applied the RICE framework to make an objective decision, calibrating metrics to our specific context (Reach = # of companies, Effort = person-months).

**Top 5 RICE Scores:**

| Rank | Solution | RICE Score | Why it won? |
| :--- | :--- | :--- | :--- |
| **1** | **Advanced Filtering & Saved Views (3C)** | **600** | Massive reach, low implementation cost, immediate value (replaces Excel). |
| **2** | **Simple Linear Dependencies (2A)** | **350** | Critical for coordination, relatively simple to implement (Effort: 2). |
| **3** | **Dedicated Recurring Tasks Engine (4B)** | **333.3** | Solves a very frequent, high-friction pain point ("low hanging fruit"). |
| **4** | **Simple Aggregating Labels (1A)** | **320** | Enables a "bird's-eye view" without building complex new objects (Initiatives). |
| **5** | **Enhanced Messenger Integration (6C)** | **216.7** | Supports "Quick Capture" and information flow via Slack/Teams. |

## 6. Strategic Recommendation: The "Coordination Bundle"

Strategic analysis demonstrated that implementing *only* the top-ranked solution (Filtering) would be insufficient to stop churn in the 30-50 employee segment. Filtering provides *access* to data but does not manage the *flow* of work.

**Final Decision:** Implement an **integrated feature bundle (MVP)**:

1.  **Filtering 2.0 (Access):** To find the needle in the haystack.
2.  **Linear Dependencies (Blocking):** To prevent chaos and blocked work between teams.
3.  **Aggregating Labels (Visibility):** To give managers insight into initiative progress on a single screen.

*Recurring Tasks (Rank #3) were queued as a separate "Quick Win" track.*

### 🎨 Prototyping (v0)
To validate the concepts quickly, **v0** was used to generate a **High-Fidelity interactive prototype** of the "Coordination Bundle". This allowed us to visualize the solution and ensure it adheres to FlowCraft's "DNA of Simplicity" before writing a single line of code.

👉 **[View Interactive Prototype (v0)](https://v0-flow-craft-task-management-three.vercel.app/)**

## 7. Tools Used
* **Data Gathering:** n8n (Reddit scraping integration).
* **AI Analysis:** NotebookLLM (Data synthesis & Pain Point extraction).
* **Simulation:** Synthetic AI Users (Simulated Customer Interviews).
* **Strategy:** Opportunity Solution Tree (OST), Affinity Mapping, RICE Framework.
* **Prototyping:** v0 (Generative UI).
