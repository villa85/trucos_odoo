# Clave SSH en Windows
```
ssh-keygen -t rsa
```
# Comando para clonar un rama determinada de un repositorio
```
Ejemplo: git clone https://github.com/Odoo/odoo.git --depth 1 --branch 17.0 --single-branch odoo

Nota: el (odoo) al final del comando se refiere al nombre del repositorio
```
# Comando listar ramas
```
  Este comando te mostrará ramas remotas. La bandera -r es la abreviación de --remotes.
  git branch -r
```
# Comando crear de rama y pasar a la misma
   Para hacer esto, puedes usar el comando git checkout.
  (master)$ git checkout -b mi-función
# Comando cambiar de ramas
   Para hacer esto, puedes usar el comando git checkout.
  (mi-función)$ git checkout master
