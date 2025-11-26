# Możliwości Zarządzania i Wizualizacji Zależności Międzyzespołowych

Na podstawie analizy problemów i luk w istniejących narzędziach (Asana, ClickUp, Linear, Jira), zidentyfikowano kluczowe obszary możliwości (ang. *opportunities*). Ich wdrożenie ma na celu poprawę przejrzystości, zmniejszenie tarcia operacyjnego oraz wspieranie skalowania małych i średnich zespołów.

---

## 1. Ulepszona Automatyzacja i Propagacja Zależności
Istnieje krytyczna potrzeba wdrożenia niezawodnej automatyzacji, która honoruje i aktualizuje stany zadań w oparciu o ich zależności logiczne.

### Kluczowe funkcjonalności:
* **Wykrywanie Zależności Międzyzespołowych:** Automatyczna identyfikacja zależności pomiędzy różnymi zespołami i projektami oraz prognozowanie współdzielonych kamieni milowych.
* **Wyzwalacze Oparte na Stanach Zależności:** Implementacja triggerów reagujących na zmiany, takie jak:
    * „Zadanie zostało zablokowane”
    * „Zadanie przestało być zablokowane”
* **Propagacja Stanu:** Automatyzacja, która aktualizuje statusy wszystkich zadań zależnych w momencie zmiany stanu zadania blokującego (np. poprzez akcje kaskadowe lub edycję zbiorczą).
* **Reguły Statusu Rodzic-Dziecko:** Logika pozwalająca na odzwierciedlenie stanu zadań podrzędnych w zadaniu nadrzędnym (np. zmiana statusu Epica na „W toku”, gdy pierwsze zadanie potomne ruszy).
* **Niezawodne Harmonogramowanie Zależności:**
    * Gwarantowane ruchy Gantta z walidacją dat i podglądem przesunięć.
    * Wsparcie dla „sztywnych” dat (np. dostawy zewnętrzne), które nie ulegają automatycznemu przesunięciu.

---

## 2. Kompleksowa Wizualizacja i Raportowanie Portfela
Zespoły często cierpią z powodu fragmentaryzacji danych. Rozwiązaniem jest stworzenie **pojedynczego źródła prawdy** dla całej organizacji.

### Kluczowe funkcjonalności:
* **Pulpit Nawigacyjny Portfela (Workspace Level):** Zagregowany widok łączący metryki (czas cyklu, on-time/late) i statusy projektów z całej przestrzeni roboczej.
* **Wspólne Inicjatywy Międzyzespołowe:** Natywne wsparcie dla inicjatyw, które linkują epiki nadrzędne pomiędzy różnymi projektami.
* **Agregacja Międzyprojektowa (Roll-up Reporting):** Automatyczne raporty podsumowujące i mapy drogowe agregujące projekty zespołowe, eliminujące konieczność używania zewnętrznych arkuszy kalkulacyjnych.
* **Wizualizacja Zależności Międzyzespołowych:** Widok osi czasu dla wielu zespołów, umożliwiający zarządzanie rozłożonymi w czasie przekazaniami (ang. *staggered handoffs*).
* **Zaawansowane Filtrowanie:** Możliwość filtrowania wg zespołu, działu lub osoby w całej przestrzeni roboczej oraz filtry referencyjne (np. „pokaż zadania blokowane przez ID #123”).
* **Wspólny Kalendarz:** Natywny kalendarz obejmujący całe konto, agregujący wszystkie zadania bez duplikacji.

---

## 3. Usprawnienie Przepływów Pracy (Workflow Structure)
Dla skalujących się zespołów kluczowe jest wyeliminowanie nieefektywnych mechanizmów przypisywania i śledzenia pracy.

### Kluczowe funkcjonalności:
* **Obsługa Wielu Przypisanych Osób:** Natywna obsługa wielu assignee (np. `Owner` + `Support` lub podział na role) dla lepszego planowania zasobów.
* **Łączenie Międzylistowe (Mirroring):** Mechanizm pozwalający na wyświetlanie tego samego zadania na wielu tablicach (np. Dev Board i QA Board) jako jeden kanoniczny element, bez tworzenia duplikatów.
* **Szablony Międzyfunkcyjne:** Gotowe wzorce mapujące role, podzadania i zależności dla złożonych procesów (np. w agencjach).
* **Agregacja Właścicieli Subtasków:** Raportowanie, które „wyciąga” dane o obciążeniu z poziomu podzadań do poziomu funkcji/projektu, dając menedżerom pełny obraz obciążenia zespołu.
