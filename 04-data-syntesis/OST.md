<div align="center">
  <p>
    <strong>
      <a href="#katalog-eksperymentów-i-opisów-rozwiązań-flowcraft">🇵🇱 Czytaj po polsku</a>
      &nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
      <a href="#catalog-of-experiments-and-solution-descriptions-flowcraft">🇬🇧 Read in English</a>
    </strong>
  </p>
</div>

---

# Opportunity solution tree

**Cel Dokumentu:** Zdefiniowanie zakresu rozwiązań oraz metod ich taniej weryfikacji (walidacji) przed wdrożeniem.

---

## 1. Opportunity: Zapewnienie "Widoku z lotu ptaka"
**Opis Problemu:** Menedżerowie tracą kontrolę nad postępem prac, gdy inicjatywy są rozproszone na wielu tablicach ("osobne wyspy"). [cite_start]Brakuje jednego miejsca do śledzenia statusu cross-zespołowego [cite: 487-491].

| ID | Rozwiązanie | Krótki Opis | Proponowany Eksperyment (Metoda Walidacji) | Metryki Sukcesu |
| :--- | :--- | :--- | :--- | :--- |
| **1A** | **Prosty System Etykiet Agregujących** | Umożliwienie nadawania tej samej etykiety (np. "Projekt X") zadaniom na różnych tablicach i generowania widoku zbiorczego postępu dla tej etykiety. | **Concierge Test (Manualny Raport):** Ręczne przygotowanie cotygodniowego raportu zbiorczego dla 5 kluczowych klientów na podstawie ich etykiet. | Oszczędzony czas PM-a vs. ręczne zbieranie danych; % klientów chcących zautomatyzować ten raport. |
| **1B** | **Lekki Kontener Nadrzędny ("Inicjatywa")** | Nowy obiekt "Inicjatywa" działający jak folder, do którego można "wrzucać" zadania z różnych tablic, aby widzieć ich wspólny postęp. | **Test Prototypu (Low-Fi):** Klikalny prototyp w Figmie pokazujący proces tworzenia inicjatywy i dodawania zadań. Testy z 5 PM-ami. | Wskaźnik ukończenia zadania w prototypie; Ocena użyteczności (SUS). |
| **1C** | **Pełna Warstwa Strategiczna** | Dedykowana tablica/roadmapa dla Inicjatyw z własnymi statusami i hierarchią (model zbliżony do Jira Epics). | **Test Propozycji Wartości:** Prezentacja makiety High-Fi obok rozwiązania 1B. Pytanie o preferencję: prostota vs. zaawansowana kontrola. | % użytkowników wybierających to rozwiązanie mimo wyższej złożoności. |

---

## 2. Opportunity: Umożliwienie zarządzania zależnościami
[cite_start]**Opis Problemu:** Praca jest blokowana, a terminy niedotrzymywane, ponieważ brakuje wizualizacji powiązań między zadaniami na różnych tablicach (np. Dev blokuje Marketing) [cite: 535-542].

| ID | Rozwiązanie | Krótki Opis | Proponowany Eksperyment (Metoda Walidacji) | Metryki Sukcesu |
| :--- | :--- | :--- | :--- | :--- |
| **2A** | **Proste Powiązania Liniowe** | Funkcja "Połącz zadanie", pozwalająca oznaczyć relację "Blokuje" lub "Jest blokowane przez" z wizualną ikoną kłódki na karcie. | **Painted Door (Fake Door):** Dodanie nieaktywnego przycisku "Dodaj zależność" w menu zadania. Mierzenie zainteresowania. | CTR (Click-Through Rate) na przycisk; Jakościowe ankiety po kliknięciu ("Czego szukałeś?"). |
| **2B** | **Propagacja Stanu** | Automatyzacja, która zmienia status zadania zależnego (np. na "Do zrobienia") w momencie ukończenia zadania blokującego. | **Concierge Automation:** Ręczna symulacja (lub skrypt Zapier) dla wybranych klientów, automatyzująca ich kluczowe hand-offy. | Zadowolenie z płynności procesu; Redukcja liczby wiadomości na Slacku "czy już skończyłeś?". |
| **2C** | **Reguły Statusu Rodzic-Dziecko** | Automatyczna aktualizacja statusu Inicjatywy na podstawie statusów zadań podrzędnych (Roll-up). | **Interaktywny Prototyp:** Symulacja zachowania paska postępu przy zmianie statusów zadań. Test zrozumienia logiki przez użytkownika. | Czy użytkownik rozumie, dlaczego pasek postępu się zmienił? (Test zrozumienia). |
| **2D** | **Wizualna Mapa Zależności** | Widok osi czasu (Gantt) pokazujący zadania i strzałki zależności, ułatwiający planowanie sekwencyjne. | **Walidacja Statycznych Makiet:** Pokazanie wydruku/makiety Gantta PM-om i pytanie o konkretne decyzje planistyczne, które by podjęli. | Postrzegana użyteczność w identyfikacji wąskich gardeł. |

---

## 3. Opportunity: Raportowanie i Audyt
**Opis Problemu:** Klienci eksportują dane do Excela ("protezy"), aby analizować trendy. [cite_start]Brak historii zmian ("dziennika zdarzeń") generuje ryzyko w branżach regulowanych [cite: 558-559, 739-743].

| ID | Rozwiązanie | Krótki Opis | Proponowany Eksperyment (Metoda Walidacji) | Metryki Sukcesu |
| :--- | :--- | :--- | :--- | :--- |
| **3A** | **Platforma Dashboardów** | Konfigurowalny widok z widgetami (wykresy, KPI) na poziomie workspace. | **Wizard of Oz:** Formularz "Zamów raport". Ręczne generowanie wykresów w Looker Studio na życzenie klienta. | Liczba zamówień na raporty; Rodzaje najczęściej zamawianych wykresów. |
| **3B** | **Dashboard "Zdrowie Sprintu"** | Gotowy szablon z metrykami Agile: Burndown, Velocity, Capacity, Zadania wg statusu. | **Wywiad z Makietą:** Pokazanie makiety zespołom pracującym w sprintach. Pytanie: "Czy ten widok zastąpiłby Wasze obecne spotkania/raporty?". | Deklaracja chęci użycia; Ocena kompletności metryk. |
| **3C** | **Zaawansowane Filtrowanie** | Widok tabelaryczny ("Excel w aplikacji") z zaawansowanymi filtrami, grupowaniem i możliwością zapisu widoku. | **Test Użyteczności Prototypu:** Zadanie dla użytkownika: "Znajdź wszystkie zadania Jana z etykietą X, które są przeterminowane". | Czas wykonania zadania; Łatwość znalezienia filtrów. |
| **3D** | **Dedykowane Funkcje Audytu** | Niezmienialne migawki (Snapshots) zamkniętych sprintów oraz szczegółowy log historii zmian (kto, co, kiedy). | **Wywiad Compliance:** Pogłębione wywiady z klientami z branż regulowanych (FinTech, MedTech). Prezentacja logów. | Potwierdzenie przez klienta, że log spełnia wymogi audytora; "Must-have" vs "Nice-to-have". |

---

## 4. Opportunity: Automatyzacja Workflow
**Opis Problemu:** Wzrost skali generuje "work-about-work". [cite_start]Klienci potrzebują elastyczności i redukcji powtarzalnych czynności manualnych [cite: 155-156].

| ID | Rozwiązanie | Krótki Opis | Proponowany Eksperyment (Metoda Walidacji) | Metryki Sukcesu |
| :--- | :--- | :--- | :--- | :--- |
| **4A** | **Wizualny Kreator Reguł** | Narzędzie "Jeśli X to Y" do budowania własnych automatyzacji. | **Papierowe Prototypowanie:** Danie użytkownikom kartki i prośba o "narysowanie" reguły, którą chcieliby stworzyć. | Zrozumienie logiki If/Then; Identyfikacja najczęstszych triggerów. |
| **4B** | **Silnik Zadań Cyklicznych** | Funkcja tworzenia zadań powtarzalnych (np. "Co poniedziałek") z szablonów. | **Fake Door:** Przycisk "Ustaw powtarzanie" w menu zadania. Wyświetlenie ankiety po kliknięciu. | Liczba kliknięć (popyt); Zebrane use-cases (co chcą powtarzać?). |
| **4C** | **Gotowe Szablony Automatyzacji** | Biblioteka "Best Practices" – gotowe reguły do włączenia jednym kliknięciem (np. "Move to Done on Merge"). | **Landing Page / Ankieta:** Lista proponowanych szablonów z pytaniem "Który włączyłbyś dzisiaj?". | Ranking popularności szablonów. |
| **4D** | **Reguły Walidacji** | Wymuszanie warunków (np. "Wypełnij pole X") przed zmianą statusu zadania (Definition of Done). | **Wywiad Problemowy:** Pytanie liderów zespołów: "Jak często wracają do Was zadania z powodu braków?". Prezentacja makiety blokady. | Postrzegana wartość w utrzymaniu higieny pracy. |

---

## 5. Opportunity: Onboarding Nowych Zespołów
[cite_start]**Opis Problemu:** Nowe zespoły nie wykorzystują potencjału narzędzia z powodu braku wiedzy, co prowadzi do szybkiej rezygnacji [cite: 455-457].

| ID | Rozwiązanie | Krótki Opis | Proponowany Eksperyment (Metoda Walidacji) | Metryki Sukcesu |
| :--- | :--- | :--- | :--- | :--- |
| **5A** | **Interaktywne Samouczki** | Wbudowane przewodniki "krok po kroku" i pomoc kontekstowa. | **Test A/B:** Grupa A otrzymuje samouczek przy pierwszym logowaniu, Grupa B nie. | % użytkowników, którzy skonfigurowali pierwszy projekt (Aktywacja). |
| **5C** | **Kreator Konfiguracji** | Prosty wizard prowadzący administratora przez setup przestrzeni roboczej. | **Obserwacja Onboardingu:** Obserwacja nowego użytkownika próbującego skonfigurować konto bez pomocy vs. z makietą kreatora. | Czas do pierwszego "Aha moment"; Liczba błędów konfiguracji. |

---

## 6. Opportunity: Integracje Zewnętrzne
[cite_start]**Opis Problemu:** Słaba synchronizacja z ekosystemem (GitHub, Kalendarz) zmusza do ręcznej aktualizacji statusów w dwóch miejscach [cite: 159-162].

| ID | Rozwiązanie | Krótki Opis | Proponowany Eksperyment (Metoda Walidacji) | Metryki Sukcesu |
| :--- | :--- | :--- | :--- | :--- |
| **6A** | **Głęboka Integracja z GitHub** | Dwukierunkowa synchronizacja statusów (PR <-> Zadanie) i podgląd statusu CI/CD. | **Wizard of Oz:** Ręczna aktualizacja zadań dla wybranego zespołu dev na podstawie ich GitHub activity. | Opinia deweloperów: czy to oszczędza im czas/przełączanie kontekstu? |
| **6B** | **Sync Kalendarza (2-way)** | Niezawodna synchronizacja zadań z kalendarzami Google/Outlook. | **Beta z Zewnętrznym Narzędziem:** Zaoferowanie integracji przez sprawdzone narzędzie (np. Zapier/Cronofy) wybranej grupie. | Stabilność synchronizacji; Satysfakcja z widoczności zadań w kalendarzu. |
| **6C** | **Integracja z Komunikatorami** | Quick Capture (tworzenie zadań ze Slacka) i aktywne powiadomienia (zmiana statusu z poziomu Slacka). | **Prototyp Bota Slack:** Prosty bot pozwalający tylko na tworzenie zadań komendą. | Liczba zadań utworzonych przez bota vs. przez UI aplikacji. |
| **6D** | **Otwarty Framework Integracji** | Publiczne API i Webhooki umożliwiające budowę własnych integracji. | **Program Partnerski:** Udostępnienie dokumentacji API beta wybranym klientom z nietypowymi potrzebami. | Czy klient był w stanie samodzielnie zbudować działającą integrację? |

<br>
<br>

---

<br>
<br>

# Opportunity solution tree

**Purpose:** Defining the scope of solutions and methods for cheap verification (validation) before implementation.

---

## 1. Opportunity: Providing a "Bird's-eye View"
**Problem:** Managers lose control over progress when initiatives are scattered across multiple boards ("isolated islands"). [cite_start]A single place to track cross-team status is missing [cite: 487-491].

| ID | Solution | Short Description | Proposed Experiment (Validation Method) | Success Metrics |
| :--- | :--- | :--- | :--- | :--- |
| **1A** | **Simple Aggregating Labels** | Enabling the same label (e.g., "Project X") to be applied to tasks on different boards and generating a consolidated progress view for that label. | **Concierge Test (Manual Report):** Manually preparing a weekly aggregated report for 5 key clients based on their labels. | Time saved for PM vs. manual data collection; % of clients wanting to automate this report. |
| **1B** | **Lightweight Container ("Initiative")** | A new "Initiative" object acting like a folder, into which tasks from various boards can be "dropped" to view their collective progress. | **Prototype Test (Low-Fi):** Clickable Figma prototype showing the process of creating an initiative and adding tasks. Tests with 5 PMs. | Task completion rate in prototype; Usability Score (SUS). |
| **1C** | **Full Strategic Layer** | Dedicated board/roadmap for Initiatives with its own statuses and hierarchy (similar to Jira Epics). | **Value Proposition Test:** Presentation of High-Fi mockup alongside solution 1B. Preference question: simplicity vs. advanced control. | % of users choosing this solution despite higher complexity. |

---

## 2. Opportunity: Enabling Dependency Management
[cite_start]**Problem:** Work is blocked and deadlines missed because links between tasks across different boards are not visualized (e.g., Dev blocking Marketing) [cite: 535-542].

| ID | Solution | Short Description | Proposed Experiment (Validation Method) | Success Metrics |
| :--- | :--- | :--- | :--- | :--- |
| **2A** | **Simple Linear Dependencies** | "Link Task" feature, allowing to mark a relationship as "Blocks" or "Is blocked by" with a visual lock icon on the card. | **Painted Door (Fake Door):** Adding an inactive "Add dependency" button in the task menu. Measuring interest. | CTR (Click-Through Rate) on the button; Qualitative surveys after click ("What were you looking for?"). |
| **2B** | **Status Propagation** | Automation that changes the status of a dependent task (e.g., to "To Do") when the blocking task is completed. | **Concierge Automation:** Manual simulation (or Zapier script) for selected clients, automating their key hand-offs. | Satisfaction with process fluidity; Reduction in Slack messages "is it done yet?". |
| **2C** | **Parent-Child Status Rules** | Automatic update of Initiative status based on the statuses of child tasks (Roll-up). | **Interactive Prototype:** Simulation of progress bar behavior when task statuses change. Testing user comprehension of logic. | Does the user understand why the progress bar changed? (Comprehension test). |
| **2D** | **Visual Dependency Map** | Timeline view (Gantt) showing tasks and dependency arrows, facilitating sequential planning. | **Static Mockup Validation:** Showing a printout/mockup of Gantt to PMs and asking about specific planning decisions they would make. | Perceived usefulness in identifying bottlenecks. |

---

## 3. Opportunity: Reporting and Audit
**Problem:** Customers export data to Excel ("crutches") to analyze trends. [cite_start]Lack of change history ("event log") creates risks in regulated industries [cite: 558-559, 739-743].

| ID | Solution | Short Description | Proposed Experiment (Validation Method) | Success Metrics |
| :--- | :--- | :--- | :--- | :--- |
| **3A** | **Dashboard Platform** | Configurable view with widgets (charts, KPIs) at the workspace level. | **Wizard of Oz:** "Order a Report" form. Manually generating charts in Looker Studio upon client request. | Number of report orders; Types of most requested charts. |
| **3B** | **"Sprint Health" Dashboard** | Ready-made template with Agile metrics: Burndown, Velocity, Capacity, Tasks by status. | **Interview with Mockup:** Showing the mockup to teams working in sprints. Question: "Would this view replace your current meetings/reports?". | Declaration of intent to use; Assessment of metric completeness. |
| **3C** | **Advanced Filtering** | Table view ("Excel in-app") with advanced filters, grouping, and view saving capabilities. | **Prototype Usability Test:** User task: "Find all tasks assigned to John with label X that are overdue". | Time on task; Ease of finding filters. |
| **3D** | **Dedicated Audit Features** | Immutable snapshots of closed sprints and detailed change history log (who, what, when). | **Compliance Interview:** In-depth interviews with clients from regulated industries (FinTech, MedTech). Presenting logs. | Client confirmation that the log meets auditor requirements; "Must-have" vs "Nice-to-have". |

---

## 4. Opportunity: Workflow Automation
**Problem:** Increasing scale generates "work-about-work". [cite_start]Clients need flexibility and reduction of repetitive manual tasks [cite: 155-156].

| ID | Solution | Short Description | Proposed Experiment (Validation Method) | Success Metrics |
| :--- | :--- | :--- | :--- | :--- |
| **4A** | **Visual Rule Builder** | "If X then Y" tool for building custom automations. | **Paper Prototyping:** Giving users paper and asking them to "draw" a rule they would like to create. | Understanding of If/Then logic; Identification of most common triggers. |
| **4B** | **Recurring Tasks Engine** | Feature to create repeating tasks (e.g., "Every Monday") from templates. | **Fake Door:** "Set recurrence" button in the task menu. Displaying a survey after click. | Number of clicks (demand); Collected use-cases (what do they want to repeat?). |
| **4C** | **Pre-built Automation Templates** | Library of "Best Practices" – ready-made rules to enable with one click (e.g., "Move to Done on Merge"). | **Landing Page / Survey:** List of proposed templates with the question "Which one would you enable today?". | Template popularity ranking. |
| **4D** | **Validation Rules** | Enforcing conditions (e.g., "Fill field X") before changing task status (Definition of Done). | **Problem Interview:** Asking team leaders: "How often do tasks return to you due to missing info?". Presenting the block mockup. | Perceived value in maintaining work hygiene. |

---

## 5. Opportunity: Onboarding New Teams
[cite_start]**Problem:** New teams fail to utilize the tool's potential due to lack of knowledge, leading to quick churn [cite: 455-457].

| ID | Solution | Short Description | Proposed Experiment (Validation Method) | Success Metrics |
| :--- | :--- | :--- | :--- | :--- |
| **5A** | **Interactive Tutorials** | Built-in "step-by-step" guides and contextual help. | **A/B Test:** Group A receives a tutorial upon first login, Group B does not. | % of users who configured their first project (Activation). |
| **5C** | **Setup Wizard** | Simple wizard guiding the administrator through workspace setup. | **Onboarding Observation:** Observing a new user trying to set up an account without help vs. with a wizard mockup. | Time to first "Aha moment"; Number of configuration errors. |

---

## 6. Opportunity: External Integrations
[cite_start]**Problem:** Poor synchronization with the ecosystem (GitHub, Calendar) forces manual status updates in two places [cite: 159-162].

| ID | Solution | Short Description | Proposed Experiment (Validation Method) | Success Metrics |
| :--- | :--- | :--- | :--- | :--- |
| **6A** | **Deep GitHub Integration** | Two-way status synchronization (PR <-> Task) and CI/CD status preview. | **Wizard of Oz:** Manual update of tasks for a selected dev team based on their GitHub activity. | Developer opinion: does it save them time/context switching? |
| **6B** | **Calendar Sync (2-way)** | Reliable synchronization of tasks with Google/Outlook calendars. | **Beta with External Tool:** Offering integration via a proven tool (e.g., Zapier/Cronofy) to a selected group. | Sync stability; Satisfaction with task visibility in the calendar. |
| **6C** | **Messenger Integration** | Quick Capture (creating tasks from Slack) and active notifications (change status from Slack). | **Slack Bot Prototype:** Simple bot allowing only task creation via command. | Number of tasks created by bot vs. via app UI. |
| **6D** | **Open Integration Framework** | Public API and Webhooks enabling construction of custom integrations. | **Partner Program:** Sharing beta API documentation with selected clients having unique needs. | Was the client able to build a working integration independently? |