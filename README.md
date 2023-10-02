# Invoke-WMIRemoting
Command Execution or Pseudo-Shell over WMI

The user you run the script as needs to be administrator over the target system

Run as follows:

```
iex(new-object net.webclient).downloadstring('https://raw.githubusercontent.com/Leo4j/Invoke-WMIRemoting/main/Invoke-WMIRemoting.ps1')
```

### Enter Pseudo-Shell

Please note that you're working within a Pseudo-Shell session. If you need to execute interdependent commands, ensure they are concatenated.

```
Invoke-WMIRemoting -ComputerName Server01.domain.local # Authenticate as Current User
```
```
Invoke-WMIRemoting -ComputerName Server01.domain.local -Username domain\user -Password Password # Authenticate as other Domain User
```
```
Invoke-WMIRemoting -ComputerName Server01.domain.local -Username .\Administrator -Password Password # Authenticate as Native Administrator User
```

### Command Execution
```
Invoke-WMIRemoting -ComputerName Server01.domain.local -Command "whoami /all" # Authenticate as Current User
```
```
Invoke-WMIRemoting -ComputerName Server01.domain.local -Username domain\user -Password Password -Command "whoami /all" # Authenticate as other Domain User
```
```
Invoke-WMIRemoting -ComputerName Server01.domain.local -Username .\Administrator -Password Password -Command "whoami /all" # Authenticate as Native Administrator User
```

![image](https://github.com/Leo4j/Invoke-WMIRemoting/assets/61951374/c22072bd-5fb8-499f-88e5-c2f0912bb85c)

![image](https://github.com/Leo4j/Invoke-WMIRemoting/assets/61951374/214aee0c-7083-495a-b961-367375b4f74b)

![image](https://github.com/Leo4j/Invoke-WMIRemoting/assets/61951374/bcbe4e35-d4e4-4fbf-baff-894fb806a3a1)
