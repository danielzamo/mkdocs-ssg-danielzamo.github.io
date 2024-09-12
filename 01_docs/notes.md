# Mkdocs en versión beta o prueba


Como seria probar ese host virtual de nginx si mi coneccion es via ssh atraves de un salto y desde un navegador web de desktop? Es decir para yo logarme via ssh tengo:

Host h01.vpn
  HostName 179.39.31.16
  User soporte-admin
  IdentityFile ~/.ssh/dz
  ProxyJump salto.vpn


Host salto.vpn
  HostName 17.74.207.190
  User dazamo
  IdentityFile ~/.ssh/dz

logro conectarme utilizando desde el CLI el comando:

ssh h01.vpn

Quiero navegar sobre el virtual http recien creado pero si lo hago normal me esta trayendo la pagina normal de nginx?
Es posible hacer eso, con un ssh directo o algo?



## Supuestos cumplidos/dependencias

```bash
ssh -L 8099:localhost:80 root@grp6-g13.vpn

```
