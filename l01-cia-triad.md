La **Security Triad (CIA)** è uno dei concetti fondamentali della sicurezza informatica. Integrare questa nozione nella tua prima lezione darà una base solida agli studenti per comprendere i principi alla base di qualsiasi misura di sicurezza, incluse quelle relative all'application security.

### **Security Triad (CIA): Confidenzialità, Integrità e Disponibilità**

#### **1. Confidenzialità (Confidentiality)**  
**Definizione:**  
La confidenzialità si riferisce alla protezione delle informazioni da accessi non autorizzati. Solo le persone autorizzate dovrebbero poter accedere a determinati dati.  

**Aspetti da approfondire:**  
- **Autenticazione e autorizzazione:**  
  - Differenza tra identificare chi accede (autenticazione) e cosa può fare (autorizzazione).  
- **Esempi pratici:**  
  - Crittografia dei dati (in transito e a riposo).  
  - Controlli sugli accessi (es. ACL, ruoli e permessi).  
- **Rischi legati alla confidenzialità:**  
  - Data breach (es. furto di dati sensibili).  
  - Vulnerabilità come Broken Access Control (OWASP Top 10, A01).  

**Materiale e link utili:**  
- Introduzione alla crittografia: [https://cryptobook.nakov.com/](https://cryptobook.nakov.com/)  
- Data breaches famosi: [https://www.upguard.com/blog/biggest-data-breaches](https://www.upguard.com/blog/biggest-data-breaches)  

---

#### **2. Integrità (Integrity)**  
**Definizione:**  
L'integrità garantisce che i dati e i sistemi non vengano alterati o manipolati in modo non autorizzato.  

**Aspetti da approfondire:**  
- **Meccanismi di verifica:**  
  - Utilizzo di checksum e hash (es. SHA-256) per verificare l'integrità dei dati.  
  - Firma digitale per autenticare l'origine dei dati.  
- **Esempi pratici:**  
  - Logging sicuro per tracciare le modifiche.  
  - Controllo della validità dei dati in ingresso (es. protezione contro SQL Injection, OWASP Top 10, A03).  
- **Rischi legati all'integrità:**  
  - Man-in-the-middle (MITM) attack.  
  - Modifica dei dati su sistemi compromessi.  

**Materiale e link utili:**  
- Introduzione agli hash crittografici: [https://en.wikipedia.org/wiki/Cryptographic_hash_function](https://en.wikipedia.org/wiki/Cryptographic_hash_function)  
- Man-in-the-middle attack: [https://www.imperva.com/learn/application-security/man-in-the-middle-attack/](https://www.imperva.com/learn/application-security/man-in-the-middle-attack/)  

---

#### **3. Disponibilità (Availability)**  
**Definizione:**  
La disponibilità si riferisce alla capacità di garantire che sistemi, dati e servizi siano accessibili quando necessario, specialmente per gli utenti autorizzati.  

**Aspetti da approfondire:**  
- **Misure per garantire la disponibilità:**  
  - Ridondanza: sistemi di backup, cluster HA (High Availability).  
  - Protezione contro attacchi DDoS (Distributed Denial of Service).  
  - Monitoring continuo e piani di disaster recovery.  
- **Esempi pratici:**  
  - Sistemi di failover per database.  
  - Distribuzione dei servizi su più data center (es. cloud).  
- **Rischi legati alla disponibilità:**  
  - Downtime non pianificati (es. attacchi DDoS, guasti hardware).  
  - Ransomware che limita l'accesso ai dati.  

**Materiale e link utili:**  
- Guida sugli attacchi DDoS: [https://www.cloudflare.com/it-it/learning/ddos/what-is-a-ddos-attack/](https://www.cloudflare.com/it-it/learning/ddos/what-is-a-ddos-attack/)  
- Piani di disaster recovery: [https://www.ibm.com/topics/disaster-recovery](https://www.ibm.com/topics/disaster-recovery)  

---