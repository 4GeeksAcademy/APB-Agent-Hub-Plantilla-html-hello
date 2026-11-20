# Especificación inicial: Agent Hub

## Descripción del producto

Agent Hub es una startup que alquila agentes de IA a empresas. Estos agentes son asistentes inteligentes preconfigurados que pueden equiparse con diferentes skills y desplegarse para tareas específicas.

## Usuario administrador

El usuario administrador utiliza el panel interno de Agent Hub para gestionar usuarios, agentes, skills y contrataciones, así como consultar el dashboard y el log de errores.

## Alcance

Se desarrollará desde cero un panel administrativo interno, presentado como un único `index.html`. El panel debe sentirse profesional e inmediatamente utilizable como referencia para el desarrollo futuro.

## Secciones

Las siguientes secciones serán accesibles desde una navegación lateral persistente:

1. Dashboard
2. Gestión de usuarios
3. Gestión de agentes
4. Skills
5. Contrataciones de agentes
6. Log de errores

La sección activa debe estar resaltada.

## Especificaciones por sección

### Dashboard

- Mostrar cuatro tarjetas de métricas, cada una con un icono, una etiqueta y un valor hardcodeado. Usar colores diferentes según el KPI.
- Las métricas serán: ingresos totales generados este mes; pérdida total por descuentos y cupones; número de agentes activos en todos los clientes; y número de agentes actualmente marcados como «fallando».
- Debajo de las tarjetas, mostrar un área de ancho completo como marcador de posición para un gráfico de actividad semanal.

### Gestión de usuarios

- Mostrar una tabla con todos los usuarios registrados y las columnas nombre, email, plan y estado. El estado se mostrará mediante un badge.
- La tabla tendrá al menos cinco filas de usuarios hardcodeados.
- Cada fila tendrá un dropdown `⋮` con las opciones «Ver detalle» y «Eliminar».
- «Ver detalle» abrirá un modal con el registro completo del usuario. El modal se cerrará con el botón de cierre y al hacer clic en el backdrop.

### Gestión de agentes

- Mostrar un listado de todos los agentes registrados en la plataforma, con al menos cuatro agentes. Cada uno mostrará nombre del agente, propietario y estado actual mediante un badge: Activo, Inactivo o Fallando.
- Mostrar la lista de skills de cada agente colapsada por defecto, con un botón de control que la expanda y revele las skills mediante una transición suave. Al volver a hacer clic, la lista se colapsará.
- Cada agente tendrá un dropdown de acciones con las opciones «Configurar» y «Eliminar».
- «Configurar» abrirá un modal con el prompt de sistema del agente en un `textarea` editable.

### Skills

- Mostrar un catálogo con al menos cuatro skills.
- Cada skill mostrará su nombre, descripción y número de agentes que la tienen habilitada.
- El panel incluirá una breve explicación de qué es una skill en el contexto de Agent Hub: una capacidad que se puede adjuntar a los agentes.
- Cada skill tendrá un dropdown con las opciones «Ver detalle» y «Eliminar».
- «Ver detalle» abrirá un modal.

### Contrataciones de agentes

- Mostrar una tabla con al menos cuatro contratos de alquiler, activos y pasados.
- Cada contrato mostrará cliente, agente, skills contratadas, fecha de inicio, fecha de fin e importe pagado.
- Cada fila tendrá un dropdown con la opción «Ver detalle».
- «Ver detalle» abrirá un modal con el desglose completo del contrato, incluidas las skills desglosadas y sus precios individuales.

### Log de errores

- Mostrar al menos seis entradas hardcodeadas de errores de ejecución de los agentes, con timestamp, nombre del agente y descripción breve.
- Cada entrada mostrará un badge con el tipo y el código de error, utilizando un código de color para categorizarlo visualmente.
- Cada entrada tendrá un dropdown con las opciones «Ver detalle» y «Marcar como resuelto».
- «Ver detalle» abrirá un modal con la traza completa del error.

## Inventario de componentes UI reutilizables

- Sidebar o navegación lateral.
- Barra superior.
- Tarjeta de métrica.
- Tabla y fila de datos.
- Dropdown de acciones.
- Modal.
- Badge.
- Lista de skills colapsable.
- Toggle de modo claro y oscuro.

## Requisitos generales

- La barra superior tendrá un toggle para cambiar toda la interfaz entre modo claro y oscuro, utilizando las utilidades `dark:` de Tailwind. El modo seleccionado debe conservarse al navegar entre secciones.
- El diseño será responsive, con prioridad para los layouts de escritorio y tablet.
- Todos los dropdowns usarán el símbolo `⋮`. Todas las filas de datos tendrán un dropdown que se abrirá y cerrará al hacer clic. Los dropdowns también se cerrarán al hacer clic fuera.
- Los modales se cerrarán mediante la `X` y al hacer clic en el backdrop.
- Los datos estarán hardcodeados y serán consistentes entre secciones, incluidos los nombres de agentes y clientes.

## Tecnologías

- HTML5 semántico.
- Tailwind CSS vía CDN, sin atributos `style` en línea ni CSS personalizado.
- JavaScript vanilla.
- Sin frameworks ni herramientas de build.
- Sin conexiones a API ni backend.

## Criterios de aceptación

1. El panel se presenta en un único `index.html` y permite acceder a las seis secciones desde una navegación lateral persistente.
2. La sección activa aparece resaltada.
3. El toggle de la barra superior cambia toda la interfaz entre modo claro y oscuro mediante utilidades `dark:` de Tailwind. El modo elegido se conserva al navegar entre secciones.
4. La interfaz es responsive, con prioridad para escritorio y tablet.
5. Todos los dropdowns usan el símbolo `⋮`. Cada fila de datos tiene un dropdown que se abre y cierra al hacer clic y se cierra al hacer clic fuera.
6. Los modales se cierran con la `X` y al hacer clic en el backdrop.
7. Los datos hardcodeados son consistentes entre secciones, incluidos los nombres de agentes y clientes.
8. Se utiliza HTML5 semántico, Tailwind CSS vía CDN y JavaScript vanilla, sin atributos `style` en línea, CSS personalizado, frameworks ni herramientas de build.
9. Dashboard muestra las cuatro métricas indicadas en tarjetas con icono, etiqueta, valor hardcodeado y colores diferentes según el KPI, además de un marcador de posición para un gráfico de actividad semanal a ancho completo debajo de ellas.
10. Gestión de usuarios muestra al menos cinco usuarios hardcodeados con nombre, email, plan y estado mediante un badge. Cada fila incluye «Ver detalle» y «Eliminar»; «Ver detalle» abre un modal con el registro completo que se cierra con el botón de cierre o el backdrop.
11. Gestión de agentes muestra al menos cuatro agentes con nombre, propietario, estado mediante un badge y skills. Las skills están colapsadas por defecto y el control permite expandirlas con una transición suave y volver a colapsarlas. El dropdown incluye «Configurar» y «Eliminar», y «Configurar» abre un modal con el prompt de sistema en un `textarea` editable.
12. Skills muestra al menos cuatro skills con nombre, descripción y número de agentes que las tienen habilitadas; explica que una skill es una capacidad que se puede adjuntar a los agentes e incluye un dropdown por skill con «Ver detalle» y «Eliminar». «Ver detalle» abre un modal.
13. Contrataciones de agentes muestra al menos cuatro contratos activos y pasados con los campos indicados. Cada fila ofrece «Ver detalle», que abre un modal con el desglose completo y los precios individuales de las skills.
14. Log de errores muestra al menos seis entradas hardcodeadas de errores de ejecución de los agentes con los campos y el badge con código de color indicados. Cada entrada ofrece «Ver detalle» y «Marcar como resuelto», y «Ver detalle» abre un modal con la traza completa.
15. El panel no realiza conexiones a API ni backend.