# Szablon Definicji Ukończenia (Definition of Done - DoD)

## Czym jest Definicja Ukończenia?

Definicja Ukończenia (DoD) to wspólna dla całego zespołu umowa określająca, co to znaczy, że praca nad zadaniem, historyjką użytkownika czy sprintem jest **"ukończona"**. Jest to lista kontrolna (checklist), która gwarantuje jakość i transparentność.

**Dlaczego DoD jest ważne?**
- Zapewnia jednolite standardy jakości.
- Eliminuje problem "prawie gotowych" zadań.
- Zwiększa przejrzystość – każdy w zespole wie, kiedy praca jest naprawdę skończona.
- Pomaga ograniczyć liczbę błędów.

---

# Definicja Ukończenia (DoD)

- **Wersja:** 1.0
- **Data:** [RRRR-MM-DD]
- **Zespół:** [Nazwa zespołu/projektu]

---

## DoD dla Zadania (Task)

Pojedyncze zadanie techniczne jest "ukończone", gdy:

- [ ] Kod został napisany i działa poprawnie na lokalnym środowisku.
- [ ] Zostały napisane i pomyślnie przechodzą testy jednostkowe.
- [ ] Kod został sprawdzony i zatwierdzony w procesie `code review` przez co najmniej jednego innego członka zespołu.
- [ ] Wszelkie zmiany zostały zintegrowane z główną gałęzią kodu (np. `main` lub `develop`).

---

## DoD dla Historyjki Użytkownika (User Story)

Historyjka użytkownika jest "ukończona", gdy:

- [ ] Wszystkie zadania techniczne składające się na historyjkę spełniają swoje DoD.
- [ ] Wszystkie kryteria akceptacji historyjki zostały spełnione.
- [ ] Funkcjonalność została wdrożona na środowisko testowe.
- [ ] Zespół przeprowadził testy manualne, aby upewnić się, że wszystko działa zgodnie z oczekiwaniami.
- [ ] Nie ma żadnych znanych krytycznych błędów.
- [ ] Właściciel Produktu (Product Owner) zaakceptował zaimplementowaną funkcjonalność.
- [ ] Dokumentacja (jeśli była wymagana) została zaktualizowana.

---

## DoD dla Sprintu

Sprint jest "ukończony", gdy:

- [ ] Wszystkie historyjki użytkownika, które były częścią Celu Sprintu, spełniają swoje DoD.
- [ ] Niezakończone historyjki zostały przeniesione z powrotem do backlogu produktu.
- [ ] Odbyło się spotkanie **Sprint Review**, na którym zespół zaprezentował wyniki swojej pracy interesariuszom.
- [ ] Odbyło się spotkanie **Sprint Retrospective**, na którym zespół omówił, co poszło dobrze, a co można poprawić.
- [ ] Zespół zdefiniował konkretne działania usprawniające na następny sprint.

---

## Jak dostosować DoD do swojego projektu?

Definicja Ukończenia powinna być "żywa" i dostosowana do potrzeb Twojego zespołu i projektu.

- **Jeśli macie w zespole testera,** dodajcie punkt "Akceptacja przez QA".
- **Jeśli tworzycie aplikację mobilną,** dodajcie "Przetestowano na urządzeniach z systemem iOS i Android".
- **Jeśli pracujecie nad publicznym API,** dodajcie "Dokumentacja API została zaktualizowana".

## Dobre praktyki

1. **Zacznij prosto:** Lepiej mieć 5 punktów, których wszyscy przestrzegają, niż 20, które są ignorowane.
2. **Uczyń DoD widocznym:** Umieść je w widocznym miejscu (np. w `README.md` projektu, na tablicy w Jirze/Trello).
3. **Automatyzuj, co się da:** Użyj narzędzi CI/CD do automatycznego sprawdzania np. testów czy formatowania kodu.
4. **DoD jest własnością zespołu:** To zespół, a nie manager, powinien tworzyć i rozwijać swoją Definicję Ukończenia.

---

**Pamiętaj:** DoD to narzędzie, które ma pomagać, a nie przeszkadzać. Regularnie je przeglądajcie i dostosowujcie do zmieniających się potrzeb.
