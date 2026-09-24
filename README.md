# Athenea---Gestor-de-Dinero-3.11
Aplicación web local y bilingüe para controlar gastos, ingresos, presupuestos y metas de ahorro en euros. Sin cuenta, sin backend y con almacenamiento local.

Athenea es una aplicación web local para controlar gastos e ingresos en euros. Está diseñada para funcionar como una SPA autocontenida: la interfaz, los estilos, las fuentes Inter y Fraunces y Chart.js están incluidos dentro de index.html.
Tus datos financieros se guardan en el dispositivo. Este repositorio no contiene backend, base de datos, cuentas de usuario ni sincronización en la nube.
Características
Athenea permite registrar movimientos de gasto e ingreso, consultar el saldo mensual, revisar gráficas, definir presupuestos y gestionar metas de ahorro. Incluye edición y borrado con confirmación, movimientos recurrentes, categorías de ingreso personalizadas y métodos de pago en efectivo, tarjeta y transferencia.
La aplicación también incluye cinco temas visuales, interfaz en español e inglés, modo de privacidad para ocultar importes, bloqueo opcional con WebAuthn o PIN y exportación/importación local de datos. Los movimientos y ajustes permanecen en el navegador mediante window.storage cuando está disponible, con fallback automático a localStorage.
Ejecutar localmente
No hay dependencias que instalar ni proceso de compilación.
Descarga o clona este repositorio.
Sirve la carpeta con cualquier servidor HTTP estático.
Abre la dirección mostrada por el servidor.
Por ejemplo, con Python:
Bash
python3 -m http.server 8000
Después abre http://localhost:8000.
Abrir index.html directamente con file:// puede limitar algunas funciones del navegador, especialmente WebAuthn. Para una experiencia completa, utiliza siempre https:// o http://localhost.
Publicar con GitHub Pages
Este repositorio incluye el workflow .github/workflows/pages.yml. Para publicarlo:
Sube el contenido del repositorio a GitHub.
En GitHub, abre Settings → Pages.
En Build and deployment, selecciona GitHub Actions.
Haz push a la rama main.
GitHub Actions publicará el contenido de index.html.
El workflow no compila ni modifica la aplicación: publica directamente el sitio estático.
Estructura del repositorio
text
.
├── .github/workflows/pages.yml  # Publicación automática en GitHub Pages
├── .gitignore                    # Exclusiones habituales de sistema y editor
├── .nojekyll                     # Evita procesamiento Jekyll innecesario
├── LICENSE                       # Licencia MIT
├── README.md                     # Documentación del proyecto
└── index.html                    # Athenea 3.11, archivo autocontenido
Privacidad y límites
Athenea está pensada para uso local. Este repositorio no añade un servidor ni una capa de sincronización. Al publicar index.html en GitHub Pages, el código de la aplicación queda públicamente accesible, pero los movimientos que introduzcas se guardan en el almacenamiento del navegador de cada dispositivo y no se envían a este repositorio.
La publicación como sitio web no sustituye una copia de seguridad. Utiliza la función de backup de Athenea para conservar una copia JSON en un lugar seguro.
