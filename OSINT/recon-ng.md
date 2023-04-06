# RECON-NG

### Installazione

```bash
git clone https://github.com/lanmaster53/recon-ng.git
```
```bash
cd recon-ng
```
```bash
pip3 install -r REQUIREMENTS
```

### Start
```bash
./recon.ng
```

### Accessibilità da WEB

IP per accedere da browser http://127.0.0.1:5000/

### Ricerca 

Vedi tutti i moduli 
```bash
marketplace search
```

Ricerca per un modulo x

```bash
marketplace search {keyword}
```

### Installare moduli 

```bash
marketplace install {nome_modulo}
```

### Info Modulo 

```bash
marketplace info {nome_modulo}
```

### Caricare modulo

```bash
modules load {nome_modulo}
```

### Help da usare quando il modulo è caricato 

```bash
help
```

### Opzioni del modulo 

```bash
show options 
```

### Settare opzioni 

```bash
options set {nome_opzione} {valore}
```

### Vedere le opzioni settate 

```bash
info
```

### Avviare 

```bash
run
```

### Vedere gli hosts prodotti 

```bash
show hosts
```

### Aggiungere API 

Per maggiori info 
```bash
keys add
```

```bash
keys add {nome_api} {token}
```