# Tareas verificables: Agent Hub

Todas las tareas parten pendientes. Marcar una tarea como completa solo cuando se cumplan sus criterios de aceptacion.

## 1. Integracion visual

- [X] **T01 - Crear el documento unico.** Crear `index.html` con estructura HTML semantica, Tailwind CSS CDN cargado una sola vez y JavaScript vanilla. Criterios: no hay imports de frameworks/dependencias ni configuracion de build; el documento contiene el shell compartido y las seis secciones.
- [X] **T02 - Integrar el shell de Stitch.** Reutilizar la sidebar y topbar de referencia una sola vez. Criterios: aparecen las seis opciones de navegacion en el orden de `spec.md`; el shell sigue disponible al cambiar de seccion.
- [X] **T03 - Adaptar estilos y layout.** Aplicar tokens de `DESIGN_DARK.md` y `DESIGN_LIGTH.md` con clases Tailwind. Criterios: layout fluido en escritorio, tablet y movil; no se usan dimensiones fijas en pixeles para definir la estructura; estilos inline solo se usan si Tailwind no cubre el caso.

## 2. Contenido de las seis secciones

- [X] **T04 - Dashboard.** Reutilizar la base de `1.dashboard.html`. Criterios: hay cuatro KPI (ingresos mensuales, descuentos/cupones, agentes activos y agentes fallando), cada uno con icono, etiqueta, valor hardcodeado y tratamiento visual diferenciable; debajo aparece el placeholder de actividad semanal a ancho disponible. El periodo mostrado es unico.
- [X] **T05 - Gestion de usuarios.** Reutilizar tabla y modal de `2.gestion-usuarios.html`. Criterios: al menos cinco usuarios hardcodeados; columnas nombre, email, plan y estado; cada fila tiene menu `⋮` con Ver detalle y Eliminar.
- [X] **T06 - Gestion de agentes.** Reutilizar tarjetas y acordeones de `3.gestion-agentes.html`. Criterios: al menos cuatro agentes con nombre, propietario, estado y skills; todas las listas de skills empiezan colapsadas; cada agente tiene menu `⋮` con Configurar y Eliminar; Configurar abre un modal con prompt editable.
- [X] **T07 - Skills.** Reutilizar catalogo y modal de `4.skills.html`. Criterios: al menos cuatro skills; cada una muestra nombre, descripcion y cantidad de agentes asociados; se explica brevemente que una skill es una capacidad adjuntable a un agente; cada skill tiene Ver detalle y Eliminar.
- [X] **T08 - Contrataciones.** Reutilizar la tabla de `5.contratos.html`. Criterios: al menos cuatro contratos activos y pasados; se muestran cliente, agente, skills, fechas de inicio/fin e importe; Ver detalle abre un modal con el importe desglosado y precio individual de cada skill.
- [X] **T09 - Log de errores.** Reutilizar la tabla y detalle de traza de `6.log-errores.html`. Criterios: al menos seis errores con timestamp, agente, descripcion, tipo y codigo de error con badge codificado por color; cada fila ofrece Ver detalle y Marcar como resuelto; el detalle muestra la traza.
- [X] **T10 - Unificar datos de muestra.** Definir datos hardcodeados coherentes para todas las secciones. Criterios: nombres y relaciones de clientes, agentes y skills coinciden entre directorio, contratos, catalogo y errores; se cumplen las cantidades minimas de T04-T09.

## 3. Navegacion

- [X] **T11 - Implementar navegacion por pestañas.** Criterios: cada opcion activa su seccion correspondiente sin recargar; la seccion activa queda resaltada; nunca se muestran dos secciones como activas a la vez.

## 4. Dropdowns

- [X] **T12 - Implementar menus de acciones.** Criterios: cada fila/tarjeta requerida tiene control `⋮`; se puede abrir y cerrar con clic; solo queda abierto un menu a la vez; clic fuera cierra el menu. No se agregan filtros de gestion ni periodos adicionales.

## 5. Modales

- [X] **T13 - Implementar modales de detalle y configuracion.** Criterios: funcionan los modales de usuario, agente, skill, contrato y error con los datos del elemento elegido; se cierran con X, clic en backdrop y Escape; no hay IDs duplicados ni un modal que lea datos de otra seccion.
- [X] **T14 - Dar feedback a acciones sin backend.** Criterios: crear, eliminar, resolver, exportar o reiniciar no simula llamadas a API ni confirma persistencia; cuando se muestre feedback, queda claro que es visual/temporal.

## 6. Modo dark/light persistente

- [X] **T15 - Centralizar el selector de tema.** Criterios: un unico toggle cambia la interfaz completa con las utilidades `dark:`; se guarda la preferencia en una sola clave de `localStorage`; el tema persiste al cambiar de pestaña y tras recargar.

## 7. Validacion

- [ ] **T16 - Verificar interacciones y accesibilidad basica.** Probar pestañas, dropdowns, acordeones, acciones y cierre de modales con mouse y teclado; controles con nombre accesible y estado expandido cuando aplique; consola sin errores ni referencias a IDs inexistentes.
- [ ] **T17 - Verificar responsive y requisitos.** Revisar escritorio, tablet y movil; sin desbordamientos que impidan usar tablas o modales; contrastar los criterios de `spec.md`; verificar que el panel no realice solicitudes a API/backend.

T16 y T17 quedan pendientes de inspeccion visual y pruebas interactivas en navegador. La validacion estatica de scripts, IDs, cantidades, ausencia de CSS inline/custom y frameworks, badge de error con tipo/codigo y apertura ascendente/descendente de dropdowns ya paso. La ruta raiz respondia HTTP 200 antes de estos ultimos ajustes; conviene repetir la comprobacion al abrir la vista actualizada.
