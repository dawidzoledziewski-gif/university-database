# university-database
# 🎓 System Obsługi Uczelni (Database Studies)

Projekt zawiera zrzut bazy danych PostgreSQL zaprojektowanej do zarządzania procesem dydaktycznym i finansowym uczelni wyższej (studenci, prowadzący, przedmioty, oceny, czesne i płatności).

---

## 🛠️ Technologie
* **Baza danych:** PostgreSQL (wersja 18.4+)
* **Narzędzia:** `pg_dump`, edytor SQL / klient PostgreSQL (np. pgAdmin, DBeaver, psql)

---

## 📂 Struktura Bazy Danych

Baza składa się z 6 głównych tabel powiązanych relacjami:

1. **`students`** – Informacje o studentach (dane osobowe, kontaktowe, adresowe, numer indeksu, PESEL, kierunek, semestr, status, stan legitymacji, konto bankowe).
2. **`teacher`** – Dane pracowników akademickich (tytuł/stopień naukowy, imię, nazwisko, e-mail, telefon).
3. **`courses`** – Lista przedmiotów / kursów oferowanych w ramach różnych kierunków studiów.
4. **`grades`** – Oceny studentów z poszczególnych przedmiotów (z rozróżnieniem na typ oceny, np. egzamin, zaliczenie, data wystawienia, powiązanie z prowadzącym).
5. **`charges`** – Opłaty nałożone na studentów (np. raty czesnego z określoną kwotą i terminem płatności).
6. **`payments`** – Rejestr płatności realizowanych przez studentów na poczet opłat (`charges`), zawierający metody płatności oraz rachunek źródłowy.

---

## 🚀 Jak uruchomić projekt?

### 1. Wymagania wstępne
Upewnij się, że masz zainstalowany serwer PostgreSQL oraz narzędzie do zarządzania bazą danych (np. DBeaver, pgAdmin) lub dostęp do terminala z poleceniem `psql`.

### 2. Utworzenie bazy danych
Stwórz nową pustą bazę danych w swoim PostgreSQL:
```sql
CREATE DATABASE studies_db;
