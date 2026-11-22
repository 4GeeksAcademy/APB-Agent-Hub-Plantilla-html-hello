# Plan de implementacion: Agent Hub

## Objetivo

Crear un panel administrativo en un unico `index.html`, usando Tailwind CSS por CDN y JavaScript vanilla. Reutilizar la estructura y los componentes de Stitch cuando cumplan los requisitos de `spec.md`, con seis secciones navegables, datos de muestra coherentes y modo oscuro/claro persistente.

## Enfoque

1. Crear un shell semantico compartido: sidebar persistente, topbar y contenedor de contenido. Cargar Tailwind CDN una sola vez y extraer de las referencias Stitch solo el contenido de cada seccion, no sus documentos ni shells completos.
2. Integrar Dashboard, Gestion de usuarios, Gestion de agentes, Skills, Contrataciones de agentes y Log de errores respetando campos y cantidades minimas de la especificacion.
3. Mantener los datos hardcodeados en una fuente coherente para que usuarios, clientes, agentes, contratos, skills y errores compartan nombres y relaciones.
4. Implementar navegacion por pestañas sin recargar la pagina, resaltando la seccion activa.
5. Implementar dropdowns de acciones, acordeones de skills y modales requeridos, con cierres previsibles y accesibles.
6. Centralizar el modo dark/light con Tailwind `dark:` y persistir la preferencia en `localStorage`; debe conservarse al cambiar de pestaña y al recargar.
7. Validar requisitos funcionales y visuales en escritorio, tablet y móvil.

## Alcance y restricciones

- Entregable: `index.html` como pagina unica.
- Tecnologias: HTML semantico, Tailwind CDN y JavaScript vanilla. Sin frameworks, dependencias adicionales, build, backend ni API.
- Las acciones que requeririan backend seran demostrativas y no persistiran datos. La preferencia de tema si sera persistente.
- No implementar filtros de gestion ni periodos adicionales; mostrar el resumen de un unico mes/periodo.
- Evitar dimensiones fijas en pixeles y preferir utilidades responsive de Tailwind. Usar estilos inline solo cuando Tailwind no permita resolver un caso necesario.
- No modificar las plantillas Stitch, los documentos DESIGN ni `spec.md`.

## Riesgos de integracion

- Las plantillas repiten IDs y funciones globales; al unificarlas se deben evitar colisiones y selectores que afecten secciones ocultas.
- La logica actual del tema varia entre plantillas; un unico controlador debe ser la autoridad para todas las secciones.
- Algunos controles Stitch son solo visuales o muestran feedback simulado. No deben presentarse como operaciones persistentes ni como integraciones de backend.
- Los tokens y la geometria de Stitch no coinciden siempre con los documentos DESIGN; aplicar los tokens de ambos temas de forma consistente y mantener un layout fluido.

## Referencias

- Requisitos: [spec.md](spec.md)
- Temas: [DESIGN_DARK.md](../../DESIGN_DARK.md) y [DESIGN_LIGTH.md](../../DESIGN_LIGTH.md)
- Pantallas: [Dashboard](../../stitch-reference/1.dashboard.html), [Usuarios](../../stitch-reference/2.gestion-usuarios.html), [Agentes](../../stitch-reference/3.gestion-agentes.html), [Skills](../../stitch-reference/4.skills.html), [Contratos](../../stitch-reference/5.contratos.html) y [Errores](../../stitch-reference/6.log-errores.html)
