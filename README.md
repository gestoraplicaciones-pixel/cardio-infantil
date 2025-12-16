# Demo Web – Compensar

Este repositorio contiene una **maqueta web de demostración** que simula la experiencia visual del sitio corporativo de **Compensar**.  
Su objetivo principal es servir como **entorno de pruebas** para la integración de canales digitales como **Webchat** y **Webcall**, así como para la validación de un **agente AI orientador (Lina)**.

> ⚠️ Este proyecto es únicamente para fines de **demo, pruebas técnicas y validación funcional**.  
> No corresponde al sitio oficial de Compensar ni reemplaza sus canales institucionales.

---

## Objetivo del proyecto

- Simular una página institucional con identidad visual cercana a Compensar.
- Integrar y validar scripts de:
  - **Webchat**
  - **Webcall**
- Probar flujos conversacionales del agente AI **Lina** en un entorno controlado.
- Facilitar pruebas técnicas con proveedores y equipos internos.

---

## Estructura del proyecto

- `index.html`  
  Página principal del demo. Contiene:
  - Estructura HTML
  - Estilos CSS embebidos
  - Carga de scripts de Webchat y Webcall

- `README.md`  
  Documento de referencia técnica y funcional del proyecto.

- *(Opcional)*  
  Carpetas adicionales para:
  - Imágenes
  - Hojas de estilo externas
  - Recursos estáticos

---

## Funcionalidades incluidas

### 1. Webchat

- Canal de atención digital integrado en la página.
- Permite interactuar con el agente AI configurado en la plataforma.
- Script cargado dinámicamente desde InConcert.

```html
<script>
(function () {
    const s = document.createElement("script");
    s.src = "https://s3.eu-west-1.amazonaws.com/webchat.bundles/channel-bundles/fb67af19-a325-4441-bc17-0830e674e8f6/61c136aa-f223-473a-a98d-3d595dabd45f/61c136aa-f223-473a-a98d-3d595dabd45f.bundle.js";
    s.async = true;
    s.charset = "UTF-8";
    s.onload = function () {
        window.Webchat.init();
    };
    document.head.appendChild(s);
})();
</script>
