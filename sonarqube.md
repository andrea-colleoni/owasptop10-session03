Ecco una guida dettagliata per eseguire una scansione SAST di **OWASP Juice Shop** utilizzando **SonarQube**. 
---

### **1. Pre-requisiti**
1. **SonarQube**:
   - Installa o avvia un server SonarQube.
   - Assicurati che SonarQube sia configurato correttamente e raggiungibile tramite il browser.
   - Scarica e configura **SonarScanner**, lo strumento necessario per eseguire l'analisi.
   - **Plugin richiesti**:
     - SonarJS (per JavaScript/TypeScript).
     - SonarHTML (per HTML).
     - SonarCSS (per CSS).
     - SonarSecurity (per le vulnerabilità di sicurezza).

2. **OWASP Juice Shop**:
   - Clona il repository Juice Shop:
     ```bash
     git clone https://github.com/juice-shop/juice-shop.git
     cd juice-shop
     ```
   - Assicurati che il progetto sia completo e non modificato per ottenere risultati consistenti.

3. **Java**:
   - SonarScanner richiede Java per funzionare (consigliata versione 11+).

---

### **2. Configurare SonarQube**
1. **Crea un nuovo progetto su SonarQube**:
   - Accedi all’interfaccia web di SonarQube.
   - Crea un progetto chiamato, ad esempio, `JuiceShop`.
   - Genera un **token di autenticazione** per collegare il progetto al SonarScanner.

2. **Configura il file `sonar-project.properties`**:
   - All'interno della directory del progetto Juice Shop, crea un file `sonar-project.properties` con il seguente contenuto:
     ```properties
     sonar.projectKey=JuiceShop
     sonar.organization=default-organization
     sonar.sources=.
     sonar.exclusions=node_modules/**,test/**,dist/**,docs/**
     sonar.javascript.lcov.reportPaths=coverage/lcov.info
     sonar.host.url=http://localhost:9000
     sonar.login=YOUR_GENERATED_TOKEN
     ```
   - Sostituisci `YOUR_GENERATED_TOKEN` con il token generato su SonarQube.

---

### **3. Eseguire la scansione con SonarScanner**
1. **Installa le dipendenze del progetto**:
   - Esegui `npm install` nella directory del progetto per assicurarti che tutte le dipendenze siano installate.
   - Esegui i test per generare un report di copertura del codice (facoltativo ma utile):
     ```bash
     npm test
     ```

2. **Esegui SonarScanner**:
   - Assicurati che SonarScanner sia installato e configurato.
   - Nella directory del progetto, esegui:
     ```bash
     sonar-scanner
     ```
   - Questo comando avvierà l'analisi e caricherà i risultati su SonarQube.

---

### **4. Analisi dei risultati**
1. **Visualizza i risultati**:
   - Accedi all’interfaccia web di SonarQube e vai al progetto `JuiceShop`.
   - Analizza:
     - **Bug**: Problemi di programmazione che possono portare a malfunzionamenti.
     - **Code Smells**: Miglioramenti suggeriti per la qualità del codice.
     - **Vulnerabilities**: Problemi di sicurezza nel codice.
     - **Security Hotspots**: Aree di codice che richiedono revisione per potenziali rischi.

2. **Filtra i risultati**:
   - Utilizza i filtri per concentrarti sulle vulnerabilità legate all'OWASP Top 10 (es. Injection, XSS).

---