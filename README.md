# PokéDex - Despliegue en Azure Static Web Apps

Documentación para el despliegue y configuración de la aplicación Angular **PokéDex** en Azure Static Web Apps.

---

## Requisitos previos

- Un correo institucional activo de la universidad (**Tecnológico Comfenalco**).
- Una cuenta activa en **GitHub**.
- Navegador web actualizado.

![Requisitos y arquitectura](./assets/requisitos-preview.png)

---

## 1. Crear el grupo de recursos

> **¿Qué es un Grupo de Recursos?**  
> Es un contenedor lógico que organiza y administra los recursos asignados a una solución en Azure.

### Pasos en el portal de Azure:

1. En la barra superior de búsqueda del portal de Azure, busque **Grupos de recursos** y haga clic en **Crear**.
2. Configure los siguientes parámetros:
   - **Suscripción:** `Azure for Students`
   - **Nombre del grupo de recursos:** `rg-pokedex`
   - **Región:** `(US) East US 2`
3. Haga clic en **Revisar y crear** y posteriormente en **Crear**.

![Creación del grupo de recursos rg-pokedex](./assets/crear-grupo-recursos.png)

---

## 2. Preparar el repositorio en GitHub

1. Crear un repositorio público llamado `pokedex` en su cuenta de GitHub.
2. Subir el código fuente de la aplicación Angular a la rama principal (`main`).
3. Incluir en la raíz del proyecto los archivos de documentación:
   - `README.md`
   - `Despliegue.md`

> **Nota para StackEdit:**  
> Si usas **StackEdit** para redactar y sincronizar estos archivos directamente con GitHub:
> 1. Haz clic en el icono del archivo (esquina superior izquierda) y selecciona **Workspace** > **Sync with GitHub**.
> 2. Vincula tu repositorio (`tu-usuario/pokedex`) y especifica la ruta del archivo (`README.md` o `Despliegue.md`).
> 3. Las imágenes deben almacenarse dentro de una carpeta como `assets/` o `img/` dentro del repositorio para garantizar que se visualicen correctamente en GitHub.
