# Flujo del Prototipo - VerisArt

> [!IMPORTANT]
> **Estado del Proyecto:** Este repositorio contiene exclusivamente un **prototipo de interfaces de usuario (Frontend)**. Las funcionalidades de carga de archivos reales, firma criptográfica PKI y almacenamiento en bases de datos están simuladas mediante Javascript y archivos JSON locales. No debe utilizarse en entornos de producción sin el desarrollo del Backend correspondiente.

## 🗺️ Mapa de Navegación (Flow)

El flujo de las interfaces está diseñado para simular la experiencia completa de un artista digital certificando sus obras.

### 1. Punto de Entrada
- **`index.html`**: Landing page principal. Presenta la propuesta de valor de la Bóveda Digital.
  - ➡️ Redirige a `register.html` (Crear cuenta)
  - ➡️ Redirige a `login.html` (Iniciar sesión)
  - ➡️ Redirige a `verificador.html` (Acceso público)

### 2. Autenticación y Credenciales de Prueba
Para propósitos de prueba y demostración del prototipo, se ha configurado una validación de Javascript que permite ingresar al sistema con las siguientes credenciales:
- **Correo Electrónico**: `veris@gmail.com`
- **Contraseña**: `1234`

- **`register.html`**: Formulario interactivo para registro de nuevos artistas y creación de credenciales iniciales.
  - ➡️ Tras el registro exitoso (simulado), redirige a `dashboard.html`.
- **`login.html`**: Interfaz de inicio de sesión seguro.
  - ➡️ Tras iniciar sesión (simulado con las credenciales de prueba), redirige a `dashboard.html`.

### 3. Aplicación Principal (Single Page Application)
- **`dashboard.html`**: Es el corazón del prototipo. Funciona como una SPA (Single Page Application) para evitar recargas en el navegador. Se divide en dos estados principales:
  
  **Estado A: La Bóveda**
  - Muestra la tabla de certificados digitales obtenidos desde `certificates.json`.
  - Contiene un botón para iniciar una "Nueva Certificación".

  **Estado B: Flujo de Certificación Dinámico**
  - Al iniciar una certificación, el Dashboard oculta la tabla y muestra un "Stepper" (barra de progreso).
  - Carga dinámicamente mediante `fetch()` los fragmentos HTML ubicados en la subcarpeta `certification/`:
    - 📄 **`certification/step1.html`**: Carga de archivos forenses (Archivo Maestro `.psd` y Referencia `.png/.jpg`).
    - 📄 **`certification/step2.html`**: Autorización criptográfica (Carga de certificado `.p12` y contraseña).
    - 📄 **`certification/step3.html`**: Confirmación de la obra certificada, visualización de hashes y descarga del documento PDF final.
  - ➡️ El botón "Volver a la Bóveda" regresa al Estado A sin recargar la página.

### 4. Herramientas Públicas
- **`verificador.html`**: Interfaz estilo "Drop-zone" independiente donde un tercero (usuario sin cuenta) puede validar un archivo arrastrándolo a la pantalla.

---

## 🧩 Componentes Reutilizables

Para mantener el código limpio y simular un framework moderno (como React o Angular), se crearon fragmentos (partials) que se inyectan en múltiples páginas mediante Javascript:

- **`Navbar.html`**: Barra de navegación para las vistas públicas (Login, Registro, Verificador, Index).
- **`nav-session.html`**: Barra de navegación para usuarios autenticados (Dashboard), incluye botón de cierre de sesión.
- **`footer.html`**: Pie de página universal.
- **`style.css`**: Hoja de estilos global que contiene las variables del diseño (colores, fuentes) y las clases personalizadas construidas sobre Tailwind CSS.
