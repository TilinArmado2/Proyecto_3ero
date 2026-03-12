# Git - Comandos

## 1. Configuración inicial

```bash
# Configurar nombre de usuario
git config --global user.name "Tu Nombre"

# Configurar email
git config --global user.email "tuemail@email.com"

# Ver configuración actual
git config --list
```

---

# 2. Crear o iniciar repositorio

```bash
# Inicializar un repositorio en la carpeta actual
git init
```

---

# 3. Clonar repositorios

```bash
# Clonar repositorio usando HTTPS
git clone https://github.com/usuario/repositorio.git

# Clonar repositorio usando SSH
git clone git@github.com:usuario/repositorio.git

# Clonar en una carpeta específica
git clone https://github.com/usuario/repositorio.git nombre-carpeta
```

---

# 4. Estado y seguimiento de archivos

```bash
# Ver estado del repositorio
git status

# Agregar archivo específico al staging
git add archivo.txt

# Agregar todos los archivos
git add .

# Quitar archivo del staging
git reset archivo.txt
```

---

# 5. Commits

```bash
# Crear commit con mensaje
git commit -m "Mensaje del commit"

# Agregar y hacer commit en un solo comando
git commit -am "Mensaje del commit"
```

---

# 6. Historial de commits

```bash
# Ver historial de commits
git log

# Ver historial resumido
git log --oneline

# Ver historial con gráfico de ramas
git log --oneline --graph --all
```

---

# 7. Ramas (Branches)

```bash
# Ver ramas
git branch

# Crear nueva rama
git branch nombre-rama

# Cambiar de rama
git checkout nombre-rama

# Crear y cambiar de rama
git checkout -b nombre-rama

# Eliminar rama
git branch -d nombre-rama
```

---

# 8. Conectar repositorio remoto

```bash
# Ver repositorios remotos
git remote -v

# Agregar repositorio remoto
git remote add origin https://github.com/usuario/repositorio.git

# Cambiar URL del remoto
git remote set-url origin https://github.com/usuario/repositorio.git

# Eliminar remoto
git remote remove origin
```

---

# 9. Subir cambios al repositorio remoto

```bash
# Subir cambios a la rama principal
git push origin main

# Subir una rama nueva
git push origin nombre-rama

# Subir y establecer upstream
git push -u origin main
```

---

# 10. Obtener cambios del repositorio remoto

```bash
# Descargar cambios sin fusionar
git fetch

# Descargar y fusionar cambios
git pull origin main
```

---

# 11. Fusionar ramas

```bash
# Cambiar a la rama principal
git checkout main

# Fusionar otra rama
git merge nombre-rama
```

---

# 12. Guardar cambios temporalmente

```bash
# Guardar cambios temporalmente
git stash

# Ver stashes
git stash list

# Recuperar último stash
git stash pop
```

---

# 13. Conexión remota con SSH

```bash
# Generar clave SSH
ssh-keygen -t ed25519 -C "tuemail@email.com"

# Iniciar agente SSH
eval "$(ssh-agent -s)"

# Agregar clave al agente
ssh-add ~/.ssh/id_ed25519

# Mostrar clave pública para copiar a GitHub
cat ~/.ssh/id_ed25519.pub

# Probar conexión con GitHub
ssh -T git@github.com
```

---

# 14. Flujo de trabajo típico

```bash
git add .
git commit -m "Descripción de los cambios"
git push origin main
```
