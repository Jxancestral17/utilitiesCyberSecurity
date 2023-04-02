# Nessus 


## Installazione
[Download Nessus](https://www.tenable.com/downloads/nessus?loginAttempted=true)

1. Installare Nessus
2. Start
```
systemctl start nessusd.service
systemctl status nessusd
```
3. Vai a [https://localhost:8834](https://localhost:8834) per completare la configurazione, inserendo un email valida per la licenza free
4. Inserisci il codice di attivazione
5. Crea un utente


## SETUP SCAN

Creaiamo un custom policies in base all'uso da fare

1. Andiamo su Policy, poi Scan Templates
2. Inseriamo un nome e se serve una descrizione 
![img-1](https://github.com/Jxancestral17/utilitiesCyberSecurity/blob/master/VA/IMG/nessus-custom-1.png)
3. La sezione Discovery possiamo settare i vari protocolli. Se con nmap troviamo una porta aperta la possiamo aggiungere alla sezione "Destination Ports" -> esempio: "Built-in, 23"
![img-2](https://github.com/Jxancestral17/utilitiesCyberSecurity/blob/master/VA/IMG/img-2.png)
4. La sezione Port Scanning possiamo configurare le porte. Default è un SYN Scan. Default prende porte considerate comuni per Tenable.
![img-3](https://github.com/Jxancestral17/utilitiesCyberSecurity/blob/master/VA/IMG/img-3.png)
5. La sezione Service Discovery settare "Probe all ports to find services", cosi anche se alcuni servizi si trovano su porte non standard vengono trovi.
![img-4](https://github.com/Jxancestral17/utilitiesCyberSecurity/blob/master/VA/IMG/img-4.png)
6. La sezione Identity, se stiamo facendo un white o gray box è possibile estrarre i dati dalle Active Directory
![img-5](https://github.com/Jxancestral17/utilitiesCyberSecurity/blob/master/VA/IMG/img-5.png)
7. La sezione Assessment -> General, settare impostazione Accuracy cosi da non restituire falsi postivi su "Avoid".
![img-6]()
8. La sezione Brute Force, possiamo settare delle defult cred oppure settare Hydra
![img-7](https://github.com/Jxancestral17/utilitiesCyberSecurity/blob/master/VA/IMG/img-7.png)
9. La sezione Web Applications, desettare Generic web application test, rallenta lo scan e non funziona bene 
![img-8]()
10. La sezione Windows, puoi decidere di fare l'enumerazione degli account attraverso Active Directory.
![img-9]()
11. La sezione Malware, scopre malware nei target scansionati utilizzando approci diversi e IoC 
![img-10]()
12. La sezione Database, se sappiamo che hosts ospita un db Oracle possiamo scansionarlo e attivare questto settings.
![img-11]()
13. La sezione Report, puoi fare customizzare le tipologie di info. 
![img-12]()
14. La sezione Advanced, puoi settare equilibri tra velocità e precisione nello scanning del target o con la limitazione magari di un numero massimo di sessioni TCP per evitare blocchi o divieti da parte del target. Es: Firewall CheckPoint Blocca ip se in un minuti genera più di 100 connessioni.
![img-13]()
15. La tab Credentials permette di settare credenziali se siamo in modalita white o gray 
![img-14]()

## SCAN CON LA CUSTOM POLICY 

1. Vai alla Scan Templates e premi su User Defined
![img-15]()
2. Setup dello scan
![img-16]()
3. Vai nella sezione My Scans e premi il tasto start per avviare lo scan 
![img-17]()
4. Puoi monitorare lo status dello scan
5. Quando viene completato per ottenere il report basta premere su Report 
![img-18]()






