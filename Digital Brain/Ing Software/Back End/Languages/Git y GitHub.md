
## Inicializar
Introducimos el siguiente codigo:
```Git
git init
```

---
## Ramas

### Ver Ramas:
Para ver las ramas en un repositorio Git, ejecuta el comando:
```shell
git branch
```

Para ver tanto las ramas de seguimiento remoto como las ramas locales, ejecuta el comando:
```shell
git branch -a
```

---
### Cambiar Rama:
Para moverse a una rama existente, ejecuta el comando:
```shell
git checkout NOMBRE-RAMA
```
 ---
### Crear Rama:
Para crear una nueva rama, ejecutar el comando:
```shell
git branch NOMBRE-NUEVA-RAMA
```

Hay un atajo para crear y moverte a la nueva rama al mismo tiempo. Puedes pasar la opción `b`(para rama) con `git checkout`. Los siguientes comandos hacen lo mismo:
```shell
git checkout -b NOMBRE-NUEVA-RAMA
```

---
### Renombrar Rama:
Para renombrar una rama, ejecutar el comando:

```shell
git branch -m VIEJO-NOMBRE-RAMA NUEVO-NOMBRE-RAMA

# Alternativa
git branch --move VIEJO-NOMBRE-RAMA NUEVO-NOMBRE-RAMA
```

---
### Eliminar Rama:
Git no te permitirá eliminar una rama en la que te encuentres actualmente. Primero necesitas moverte a una rama diferente, y luego ejecutar el comando:

```shell
git branch -d RAMA-A-ELIMINAR

# Alternativa:
git branch --delete RAMA-A-ELIMINAR
```

La rama a la que te mueves hace la diferencia. Git arrojará un error si los cambios en la rama que estás intentando eliminar no están completamente combinados con la rama actual. Puedes anular esto y forzar a Git a eliminar la rama con la opción   `-D` (ten en cuenta la letra mayúscula) o usando la opción  `--force` con `-d` o `--delete`:

```shell
git branch -D RAMA-A-ELIMINAR

# Alternativas
git branch -d --force RAMA-A-ELIMINAR
git branch --delete --force RAMA-A-ELIMINAR
```

---
### Comparar Ramas:
Puedes comparar ramas con el comando `git diff`:

```shell
git diff PRIMERA-RAMA..SEGUNDA-RAMA
```

---
## Ssh Keys
### Creacion:
Introducimos el siguiente codigo:
```shell
ssh-keygen -t rsa -b 2048
```

---
### Insertar
Introducimos los siguientes codigos:
```shell
eval $(ssh-agent -s)
```

```shell
ssh-add “nombre de la llave”
```

#EngineeringSoftware