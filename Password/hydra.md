# HYDRA

### Tool password guessing 

## Installare HYDRA 

```bash
sudo apt install hydra
```

## Check & Info 

```bash
hydra -h
```

## Comando base 

```bash
hydra -l {username} -p {password} {ip} {servizio}
```

## Comando base v2

```bash
hydra -l {username} -p {password} {servizio}://{ip}
```

La parte finale può essere applicato anche ad attacchi con dizionario.
Esempio parte finale: 
ssh://127.0.0.1


## Con dizionario 

```bash
hydra -L {path_dizionario_username} -P {path_dizionario_password} {ip} {servizio} -v
```

Con -v abbiamo la verbosity


## Con porte 

```bash
hydra -l {username} -p {password} {ip} {serivzio} -s {porta}
```

## Più host

```bash
hydra -l {username} -p {password} -M {path_file_host} {servizio}
```

## A combinazioni 

Se si disponde di un file con combinazioni(N.B. detto anche combos )
Esempio di scrittura file combos(estensione più comune txt)

```bash
    username1:password1
    username2:password2
```

```bash
hydra -C {path_file_combos} {ip} {servizi}
```

