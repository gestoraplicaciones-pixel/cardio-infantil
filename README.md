# Cardio Infantil

Esta es una página de ejemplo que simula la web de **La Cardio**.  
El objetivo es tener un entorno de pruebas para integrar los scripts de **Webchat** y **Webcall** de Inconsert.

---

## Archivos principales

- `index.html` – Archivo principal de la página.  
- `README.md` – Este archivo de documentación.  
- (Opcional) Carpetas de recursos, como imágenes o CSS adicionales.

---

## Funcionalidades incluidas

1. **Webchat**  
   - Se muestra en la esquina inferior derecha.  
   - Script cargado desde Inconsert:  

   ```html
   <script>
   (function () {
       const s = document.createElement("script");
       s.src = "https://s3.eu-west-1.amazonaws.com/webchat.bundles/channel-bundles/fb67af19-a325-4441-bc17-0830e674e8f6/22002844-b90e-4577-b94a-06b9affa92a9/22002844-b90e-4577-b94a-06b9affa92a9.bundle.js";
       s.async = true;
       s.charset = "UTF-8";
       s.onload = function () { if(window.Webchat) window.Webchat.init({ container: '#webchat-container' }); };
       document.head.appendChild(s);
   })();
   </script>
