# John the ripper 

### Tool passwrod Cracking usa la CPU

## Installazione 

```bash
sudo apt install John
```

## Check & info 

```bash
john -h
```

## Singola password 

```bash
john --single --format=raw-sha1 {path_file_name}
```

Con format puo cambiare con md5, sha-2 , ecc
Il file in questione deve essere un singolo combo(N.B. Vedere [Hydra](https://github.com/Jxancestral17/utilitiesCyberSecurity/blob/master/Password/hydra.md) sezione combinazione)

## Con dizionario 

```bash
john --wordlist={path_file_dizionario} --format={formato} {file_con_password criptata}
```

N.B. in questo caso non è un combo 

## Incremental mode

```bash
john -i:digits {nome_file_password}
```

Qui prova tutte le combinazioni possibili ma processo molto molto molto lungo 

Sostituire digits con un numero massimo di caratteri

Puoi aggiungre il formato 


## Windows

```bash
--format=lm
```

Per cracckare passwword hashes di windows, visto che viene usato SAM database
e il formato delle password è LM/NTLM


## Linux 

```bash
unshadow /etc/passwd /etc/shadow > output.db
```

```bash
john output.db
```

output.db potete cambiarlo come volte importante rispettare l'estensione 

unshadow tool che fa parte di john 

## Zip file 

```bash
zip2john file.zip > zip.hashes 
```

```bash
john zip.hashes
```

Anche qui il nome potete pure cambiarlo, l'estensione rispettatela
