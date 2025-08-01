# 🛠️ Mini Taller de Git y GitHub: "Cocinando con Git"

## 🎯 Objetivo
Que los estudiantes aprendan a colaborar en un proyecto usando Git y GitHub, creando ramas, añadiendo contenido y trabajando con pull requests.

## 👨‍🍳 Participantes
- **1 estudiante** será el Responsable del repositorio (Owner).
- Los demás serán **colaboradores** (2 o 3 personas).

---

## 🪜 Pasos del Taller

### 1. 🔧 Acceso al repositorio desde GitHub Classroom
1.1. Ingresar al enlace proporcionado de **GitHub Classroom**.

1.2. Seleccionar tu nombre en la lista de estudiantes.

1.3. Especificar el equipo al que perteneces (si aplica).

1.4. Una vez creado el repositorio automáticamente, clonarlo en tu computador:
```bash
git clone https://github.com/usuario/recetas-caseras.git
cd recetas-caseras
```

---

### 2. 🌿 Crear una nueva rama para tu receta
Cada estudiante elige una receta del sitio principal y crea una nueva rama con su nombre y el nombre de la receta. Por ejemplo, si el estudiante se llama Ana y va a hacer "Brownies":
```bash
git checkout -b ana-brownies
```

Confirma que estás en la rama:
```bash
git branch
```

---

### 3. 📁 Crear carpeta y HTML para la receta
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

### 4. ✅ Agregar, commitear y subir cambios
```bash
git add recetas/brownies.html
git commit -m "Añadida receta de brownies por Ana"
git push origin ana-brownies
```

---

### 5. 🔀 Crear un Pull Request (PR)
1. Ir al repositorio en GitHub.
2. Verás un mensaje para crear un Pull Request desde tu rama.
3. Crear el PR con un mensaje claro: `"Receta de Brownies por Ana"`.

---

## 6. 👀 Revisión del PR y merge
- El dueño del repositorio (o todos) revisan el PR.
- Si todo está bien, lo aprueban y hacen **Merge**.

---

## 7. 🔄 Actualizar tu rama local con los cambios del repositorio
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

## 🌐 Despliegue con GitHub Pages

Para activar GitHub Pages y desplegar la aplicación, sigue estos pasos:

1. **Configurar GitHub Pages**:
    - Ve al repositorio en GitHub.
    - Haz clic en la pestaña **Settings** (Configuración).
    - En el menú lateral, selecciona **Pages**.
    - En la sección **Source**, selecciona la rama `main` (o la rama principal del repositorio) y la carpeta `/root` como fuente.
    - Haz clic en **Save**.

2. **Verificar el despliegue**:
    - Después de unos minutos, GitHub generará un enlace para tu sitio web. Este enlace estará en la parte superior de la página de configuración de **Pages**.
    - Accede al enlace para verificar que el sitio esté funcionando correctamente.

3. **Actualizar el `index.html`**:
    - Asegúrate de que el archivo `index.html` tenga enlaces correctos a las recetas creadas por los estudiantes.
    - Si es necesario, realiza un commit y un push con los cambios.

4. **Compartir el enlace**:
    - Comparte el enlace generado con los participantes para que puedan ver el resultado final del taller.

---
