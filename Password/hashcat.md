# HASHCAT

### Tool Password cracking

## Installazione 

```bash
sudo apt install hashcat
```

## Check & info 

```bash
hashcat -h
```

## Cracking 

```bash
hashcat -m {valore} -a {valore} {file_contente_hash_da_craccre} {dizionario}
```

-m è la tipologia di crittografia
-a la modalità d'attacco
Qui trovate tutto ciò che vi serve per capire cosa inserire[LINK](https://hashcat.net/wiki/doku.php?id=hashcat)

Per il -a valori più usati  sono 0 per il dizionario e 1 per il combo (N.B. Vedere [Hydra](https://github.com/Jxancestral17/utilitiesCyberSecurity/blob/master/Password/hydra.md) sezione combinazione)