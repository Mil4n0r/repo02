# Pasos seguidos
1. Creamos un repositorio remoto en GitHub
2. Clonamos el repositorio mediante el siguiente comando:
    ```
    git clone https://github.com/Mil4n0r/repo02.git
    ```
3. Nos movemos (en local) al repositorio recién creado:
    ```
    cd repo02
    ```
4. Creamos y editamos el readme.md
    ```
    touch readme.md
    code readme.md
    ```
5. Añadimos los cambios al staging area
    ```
    git add readme.md
    ```
6. Realizamos un snapshot
    ```
    git commit -m "Primer snapshot"
    ```

7. Subimos los cambios
    ```
    git push -u origin main
    ```

8. Comprobamos en el repositorio de GitHub que, efectivamente, se han efectuado los cambios

# Resumen de los comandos de Git

![No se puede mostrar la imagen](https://th.bing.com/th/id/R.4fbee69f970f766bd180b039544bfa80?rik=U6LQLMWUSgUEvg&riu=http%3a%2f%2f4.bp.blogspot.com%2f-u6O9eNSOUGg%2fVYLmlbA_n9I%2fAAAAAAAADvU%2fE-7rOPqCjpI%2fs1600%2f20140619-git-logo.jpg&ehk=kYACWBL41E7ItSMUS748s09LWJCyZlU5XLgbBLynJf8%3d&risl=&pid=ImgRaw&r=0 "Logo de git")



## Configuración previa
git config --global user.name "XXX YYY"
git config --global user.email "XXX@YYY.ZZZ"

## Inicialización de repositorio
Creación de un repositorio de manera local
git init repo

También es posible crear el repositorio de forma remota desde la interfaz gráfica proporcionada por GitHub.

## Flujo de trabajo
---

### 1. Preparación de archivos modificados (Staging Area)

Para pasar los cambios al staging area y que estén listos para mandarse al repositorio local empleamos la orden:

```
git add xxx
```

Siendo xxx el nombre del archivo que hemos modificado (o . en caso de querer añadir todo el directorio actual)

---
### 2. Envío de cambios al repositorio local (Snapshots)
---

Tras poner los archivos en el staging area, estos están listos para pasarse al repositorio local:

```
git commit -m "Comentario descriptivo"
```

---
### 3. Subida de cambios al repositorio remoto 

| :warning: Antes de subir cambios, debemos asegurarnos de que hemos asociado el repositorio remoto a nuestro repositorio local   |
|-----------------------------------------|



```
git remote -v
```

En caso de no estar asociado previamente, lo asociamos mediante:

```
git remote add origin https://github.com/NombreUsuario/NombreRepo.git
```

En caso de no tener la rama creada previamente, hacemos la rama main
```
git branch -M main
```

Con todo configurado, mandamos los cambios realizados al repositorio remoto

```
git push -u origin main
```

## Resumen rápido

|Comando | Utilidad |
|:--- |:---- |
|git add| Manda los cambios al staging area |
|git commit| Crea un snapshot de los cambios (repo local) |
|git remote add | Conecta con un repositorio remoto |
|git branch | Crea una rama dentro del proyecto |
|git push | Manda los cambios al repositorio remoto |

:white_check_mark: **Tarea completada**

---