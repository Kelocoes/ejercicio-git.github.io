# 🛠️ Mini Taller de Git y GitHub: "Cocinando con Git"

## 🎯 Objetivo
Que los estudiantes aprendan a colaborar en un proyecto usando Git y GitHub, creando ramas, añadiendo contenido y trabajando con pull requests.

## 👨‍🍳 Participantes
- **1 estudiante** será el Responsable del repositorio (Owner).
- Los demás serán **colaboradores** (2 o 3 personas).

---

## 🪜 Pasos del Taller

### 1. 🔧 Preparación del repositorio
#### 👤 Paso del Estudiante 1 (Responsable del repo)
1.1. Iniciar sesión en GitHub y crear un repositorio nuevo:
- **Nombre sugerido:** `recetas-caseras`
- Público o privado, según preferencia.
- Sin README ni archivos extra (opcional).

1.2. Clonar el repositorio en su computador:
```bash
git clone https://github.com/usuario/recetas-caseras.git
cd recetas-caseras
```

1.3. Copiar todos los archivos HTML y CSS (como los del código que compartiste) dentro del repositorio clonado.

1.4. Agregar los archivos al control de versiones y hacer el primer commit:
```bash
git add .
git commit -m "Primer commit: Estructura base del sitio de recetas"
git push origin main
```

---

### 2. 🤝 Invitar colaboradores
El dueño del repositorio va a **Settings → Collaborators → Invite collaborators** y añade el usuario GitHub de cada estudiante.

---

### 3. 👯‍♂️ Clonar el repositorio (colaboradores)
Cada colaborador debe ejecutar:
```bash
git clone https://github.com/usuario/recetas-caseras.git
cd recetas-caseras
```

---

### 4. 🌿 Crear una nueva rama para tu receta
Cada estudiante elige una receta del sitio principal y crea una nueva rama con su nombre y el nombre de la receta. Por ejemplo, si el estudiante se llama Ana y va a hacer "Brownies":
```bash
git checkout -b ana-brownies
```

Confirma que estás en la rama:
```bash
git branch
```

---

### 5. 📁 Crear carpeta y HTML para la receta
Dentro del proyecto, crear una carpeta `recetas/` si no existe y luego crear tu archivo. Ejemplo:
```bash
mkdir -p recetas
cd recetas
touch brownies.html
```

Editar `brownies.html` con un contenido muy simple, por ejemplo:
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Brownies Caseros</title>
</head>
<body>
    <h1>Receta de Brownies Caseros</h1>
    <p>Ingredientes: chocolate, mantequilla, azúcar, huevos, harina.</p>
    <p>Preparación: Mezcla todo, hornea 30 min a 180°C y listo.</p>
</body>
</html>
```

---

### 6. ✅ Agregar, commitear y subir cambios
```bash
git add recetas/brownies.html
git commit -m "Añadida receta de brownies por Ana"
git push origin ana-brownies
```

---

### 7. 🔀 Crear un Pull Request (PR)
1. Ir al repositorio en GitHub.
2. Verás un mensaje para crear un Pull Request desde tu rama.
3. Crear el PR con un mensaje claro: `"Receta de Brownies por Ana"`.

---

### 8. 👀 Revisión del PR y merge
- El dueño del repositorio (o todos) revisan el PR.
- Si todo está bien, lo aprueban y hacen **Merge**.

---

### 9. 🔄 Actualizar tu rama local con los cambios del repositorio
Después de que el PR se ha hecho merge, los estudiantes deben actualizar su rama local:
```bash
git checkout main
git pull origin main
```

(O si deseas seguir trabajando desde tu rama, puedes también hacer merge):
```bash
git checkout ana-brownies
git pull origin main
```

---

### 🧼 Opcional: Eliminar tu rama (luego de merge)
```bash
git branch -d ana-brownies        # local
git push origin --delete ana-brownies  # remoto
```

---

## 📝 Recomendaciones
- Cada estudiante debe modificar **solo su archivo de receta**.
- Si modifican `index.html`, asegúrense de sincronizar y no generar conflictos.
- Usar `git pull origin main` antes de crear nuevas ramas.

---

## 🏁 Final del Taller
- Abrir el archivo `index.html` en el navegador y verificar que los links de recetas funcionan correctamente.
- Cada estudiante puede verificar que su receta esté enlazada desde el sitio principal (esto puede hacerlo el dueño del repositorio como parte de una edición centralizada o cada uno por PR si el tiempo lo permite).