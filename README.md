# linux-utilitarios

## Conexao wifi no linux
Ver nome da interface de rede para conectar
```bash
ip a
```
Acessar arquivo e colocar informacoes
```bash
sudo nano /etc/netplan/01-netcfg.yaml
```
Interface a Utilizar
```bash
network:
  version: 2
  renderer: networkd
  wifis:
    wlp3s0:  # Substitua pelo nome da sua interface Wi-Fi
      dhcp4: true
      access-points:
        "nome-da-rede":  # Substitua pelo nome da sua rede Wi-Fi
          password: "sua-senha"  # Substitua pela senha da sua rede
```
Aplicar  alteracoes
```bash
sudo netplan apply
```
