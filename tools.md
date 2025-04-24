
### **1. Installazione di OWASP ZAP**
**Scopo:** Strumento gratuito per l’analisi dinamica delle applicazioni web.  

#### **Passaggi:**
1. **Download di ZAP:**  
   - Vai alla pagina ufficiale: [https://www.zaproxy.org/download/](https://www.zaproxy.org/download/).  
   - Scarica la versione per Windows (installer `.exe`).  

2. **Installazione:**  
   - Esegui il file scaricato (`ZAP_Installer.exe`) e segui le istruzioni guidate.  
   - Scegli le opzioni di default.  

3. **Verifica dell’installazione:**  
   - Avvia OWASP ZAP dal menu Start.  
   - Assicurati che l’interfaccia si avvii senza errori.  

4. **Configurazione opzionale:**  
   - Controlla che il proxy di ZAP sia attivo su `localhost:8080`.  
   - Configura il browser per utilizzare ZAP come proxy (opzionale per test avanzati).  

#### **Test rapido:**  
Esegui una scansione di un sito demo (es. [http://testphp.vulnweb.com/](http://testphp.vulnweb.com/)) per verificare che ZAP funzioni correttamente.  

---

### **2. Installazione di Burp Suite Community**
**Scopo:** Strumento per analisi avanzate di sicurezza applicativa.  

#### **Passaggi:**
1. **Download di Burp Suite:**  
   - Vai alla pagina ufficiale: [https://portswigger.net/burp/communitydownload](https://portswigger.net/burp/communitydownload).  
   - Scarica il file `.exe` per Windows.  

2. **Installazione:**  
   - Esegui il file scaricato e segui le istruzioni guidate.  
   - Scegli le opzioni di default.  

3. **Verifica dell’installazione:**  
   - Avvia Burp Suite dal menu Start.  
   - Seleziona "Temporary Project" > "Use Burp Defaults" e fai clic su *Start Burp*.  

4. **Configurazione del proxy:**  
   - Controlla che il proxy sia attivo su `localhost:8080`.  
   - Configura il browser per utilizzare Burp Suite come proxy (opzionale per test avanzati).  

#### **Test rapido:**  
Naviga su un sito demo tramite il browser configurato (es. [https://www.google.com/](https://www.google.com/)) e verifica che Burp intercetti il traffico.  

---

### **3. Configurazione di OWASP Juice Shop con Docker**
**Scopo:** Fornire l’applicazione vulnerabile da usare durante le esercitazioni.  

#### **Passaggi:**
1. **Avvio del Juice Shop con Docker:**  
   - Apri il terminale di Windows (PowerShell o Command Prompt).  
   - Esegui il comando:  
     ```bash
     docker run -d -p 3000:3000 bkimminich/juice-shop
     ```  

2. **Verifica che il Juice Shop sia attivo:**  
   - Apri il browser e vai su [http://localhost:3000](http://localhost:3000).  
   - Dovresti vedere l’interfaccia del Juice Shop.  

3. **Gestione del container:**  
   - Per fermare il Juice Shop:  
     ```bash
     docker stop <CONTAINER_ID>
     ```  
   - Per verificare i container attivi:  
     ```bash
     docker ps
     ```  

---

