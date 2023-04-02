# CheatSheet nmap

| Command       | Do            | 
| ------------- |:-------------:| 
| -sn     | non esegue una scansione sulle porte dopo che ha trovato dell’host e restituisce solo host che hanno risposto(ARP)  | 
| -n     | No dnslookups      |   
| -v  | Verbosity    |    
| -- reason   | Restituisce lo stato per ogni host     |  
| -PR | Scopre gli host nella lan (metodo migliore e più efficente) | 
|-PS[porte] -PS80,21,22|Invia pacchetto SYN, risposta o SYN_ACK(porta aperta) o RST(porta chiusa)|
|-PA[porte] -PA80,21,22|Invia pacchetto ACK riposta sempre RST (che sia aperta o chiusa)|
|-PU|UDP  poco usata |
|-sT|scan più stealth ma non funziona più|
|-sU|scan UDP|
|-sV|Versione|
|-O|Sistema operativo|
|--max-rate/min-rate=nnn|Minimo e massimo numeri di pacchetti inviati per secondo |
|--max-retries=nnn|Numero massimo di tentativi |
|--max-rtt-timeout=nnn|Attendere n secondi o millisecondi |
|--scan-delay=nnn|Tempo minimo d’attesa per l’invio di un pacchetto tra un target e l’altro |
|-iL filename|File con la lista di target |
|-oA filename|File output|
|-p[xxx]-[yyy] -p1-100|Range di porte|
|-p[xxx] -p80|Una sola porta|
|-p[xxx],[yyy] -p80,21|Solo le porte riportate|
|--top-ports=xxx|Scan solo sulle porte più famose fino ad un massimo di 1000|
|--version-intensity=xxx|“Sfrozo”(e tempo) di nmap per il controllo del servizio e della versione. Predefinito 7, min- 0  - max-9 |
