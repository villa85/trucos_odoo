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
```
   Para hacer esto, puedes usar el comando git checkout.
    cd /ruta/al/repositorio
    git checkout -b nombre-de-la-rama
    # Realiza los cambios necesarios
    git add .
    git commit -m "Descripción de los cambios"
    git push origin nombre-de-la-rama

```
# Comando cambiar de ramas
```
   Para hacer esto, puedes usar el comando git checkout.
  (mi-función)$ git checkout master
```
# Comando cambiar a un commit especifico
```
  En la primera línea de cada confirmación, después de la palabra commit, hay una larga cadena de caracteres y números: 94ab1fe28727...
  Para ver una confirmación específica, solo necesitas pasar el SHA de la confirmación como parámetro para git checkout:
  
  (mi-función)$ git checkout 035a128d2e66eb9fe3032036b3415e60c728f692
```
# Comandos para trabajar con submodulos
```
  git submodule update --init --recursive -> Busca todos lo submodulos que de lo que dependa la rama donde estoy
  git submodule update --remote -> trae todos los cambios a local

luego en dependencia de lo que necesite agrego todo lo que me trajo a la rama en la que estoy o solo los modulos especificos que estoy trabajando con
git add . -> agregar todo lo que traiga
git add <nombre del módulo>

luego hago un commit
git commit -m "algún comentario"

y por ultimo
git push para subirlo al servidor




```
