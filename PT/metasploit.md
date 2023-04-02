# METASPLOIT 

* Start Metasploit
```bash
msfconsole
```

* Cercare un exploit 
```bash
search type:exploit platform:linux tomcat
```
Modificando i parametri type e plataform potreste cercare altre stuff

* Usare exploit
```bash
use nome_exploit 
```

oppure 

```bash
use numero_della_ricerca 
```

* Settare i paramentri 

Cosi fai un set globale che non cambia mai
```bash
setg RHOSTS x.x.x.x
```

Cosi fai un set solo per quel exploit 
```bash
set RHOSTS x.x.x.x
```

* Run Exploit
```bash
run
```

* Mandare in background una sessione 
```bash
bg
```

* Vedere le sessioni 
```bash
sessions
```

* Riprendere la sessione 
```bash
session {numero della sessione}
```
