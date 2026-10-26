# Guía de Despliegue y Configuración de Seguridad de PokéDex


## 1. Repositorio de Código Fuente
- **Repositorio en GitHub:** `pokedex`
- **Ramificación Principal:** `main`
- **Tecnología Base:** Angular Framework

---

## 2. Proceso de Despliegue en la Nube (Vercel)
1. Iniciar sesión en la consola de Vercel (`https://vercel.com/`).
2. Hacer clic en **Add New...** y seleccionar la opción **Project**.
3. Seleccionar el repositorio `pokedex` dentro del listado de proyectos vinculados desde GitHub.
4. En el panel de configuración de construcción (*Build & Output Settings*):
   - **Framework Preset:** Angular (detectado automáticamente).
   - **Comando de compilación:** `npm run build`
   - **Directorio de salida:** `dist/pokedex-angular`
5. Ejecutar el botón **Deploy** para iniciar la compilación e integración continua.

---

## 3. Configuración de Encabezados de Seguridad (HTTP Headers)
Para prevenir ataques comunes y cumplir con los requisitos de ciberseguridad de Pueblo Paleta Inc., se incorporó el archivo `vercel.json` en la raíz del proyecto. Este archivo inyecta los siguientes encabezados HTTP:

- **Strict-Transport-Security (HSTS):** Forzamiento de conexiones mediante HTTPS seguro.
- **X-Frame-Options (DENY):** Prevención de ataques de Clickjacking.
- **X-Content-Type-Options (nosniff):** Protección contra la interpretación inadecuada de tipos MIME.
- **Referrer-Policy (no-referrer):** Control de la información enviada en las peticiones salientes.
- **Permissions-Policy:** Restricción de APIs del navegador (cámara, micrófono, geolocalización).
- **Content-Security-Policy (CSP):** Declaración explícita de orígenes permitidos para scripts, estilos y la conexión a PokéAPI (`https://pokeapi.co`).

---

## 4. Auditoría de Seguridad
El enlace público generado por la plataforma (`https://pokedex-psi-steel.vercel.app/`) fue auditado en la herramienta **Security Headers** (`https://securityheaders.com/`), obteniendo la máxima calificación posible.
