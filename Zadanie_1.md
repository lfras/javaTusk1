Zadanie 1 - setup
=========================

#### 1. Zaimportować aplikację
- skopiować repozytorium git z projektem startowym

        git clone http://code.impaqgroup.com/jkot/todo_training_1.git
       
- zaimportować projekt startowy do IDE (zalecane IntelliJ Idea)

- zaimportować w git bazową wersje aplikacji z tagiem "0.1"

        git checkout 0.1        

#### 2. Uruchomic aplikacje lokalnie

- z poziomu IDE (RightMouseClick na Application -> Run)
- za pomocą Mavena (użyć komend z pliku README)
- za pomocą Mavena z IDE 
     - zaznaczyć odpowiednie kroki w Lifecycle, 
     - nast RMC -> "run Maven Build"

Każdorazowo sprawdzić w przeglądarce czy aplikacja działa (adres w pliku README)
     
#### 3. Utworzyć własny branch GITa 

Każdy tworzy własny branch, na którym od tej pory będzie pracował. Niech branch nazywa się skrótem 
utworzonym z litery imienia oraz nazwiska (np. `jkowalski` dla Jana Kowalskiego)
 
        git checkout -b <i_nazwisko>
        
Branch "master" będzie zawierał punkty wejścia do kolejnych zadań oraz rozwiązania poprzednich.

**Nie wolno komitować do "mastera"!!.**        

#### 4. Dodać możliwość używania standardowych endpointów SpringBoot
     
- dodać zależność mavena w pliku `pom.xml` do artefaktu `spring-boot-starter-actuator`
- zbudować i uruchomić aplikację
- otworzyć w przeglądarce endpointy
  - `http://localhost:8080/info`
  - `http://localhost:8080/health`

#### 5. Zmienić port serwera

- w pliku `application.properties` dodać wpis ustawiający port Tomcata na 8181
- uruchomić aplikację i sprawdzić `/info` oraz `/health` w przeglądarce
- przestawić port serwera na 8080

#### 6. Zapisać własne zmiany

- Sprawdzenie brancha, na którym jesteśmy

         git branch
- Lokalny commit: 
    - z konsoli 
         
             git commit -m "komentarz" 
    - lub z IDE         


- Wypchnięcie lokalnych zmian na serwer
         
         git push origin <i_nazwisko>
         