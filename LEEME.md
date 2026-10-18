# Misión Roma v3.0.1 · edición para GitHub Pages

Proyecto «Las manos que construyeron la historia». Geometría, patrimonio histórico y realidad aumentada en Educación Primaria (5.º y 6.º).

## El proceso evolutivo

La actividad sigue el orden de una obra hidráulica real, en cinco etapas. Cada etapa se desbloquea al completar la anterior.

| Etapa | Área | Qué hace el alumnado con las manos | Contenidos |
|---|---|---|---|
| 1. Leer el terreno | Geografía | Estira las alturas del perfil y señala el valle donde el canal queda en el aire. | Perfil topográfico, cota, exageración vertical. |
| 2. Nivelar el canal | Matemáticas | Sube o baja el pilar hasta que los dos tramos bajan igual. | Pendiente en porcentaje, números enteros. |
| 3. Construir el pilar | Medida y geometría | Coloca sillares de 0,40 m hasta llegar a 3,20 m. | Prisma, volumen, arco de medio punto (radio y luz). |
| 4. Cómo lo hacían los romanos | Historia | Nivela un corobate con una cuña y quita la exageración del canal. | Instrumentos romanos, pendiente real, patrimonio. |
| 5. El agua en Canarias | Transferencia al territorio | Sube o baja las tablas de una cantonera para repartir el agua en 1/2, 1/4 y 1/4. | Fracciones, porcentajes, proporcionalidad, patrimonio hidráulico canario. |

Todas las etapas se pueden hacer de tres formas:
- con las manos ante la cámara, haciendo pinza;
- con el dedo o el ratón;
- con los controles de «Otra forma de mover» (deslizadores y botones accesibles con teclado).

## Para el profesorado

- **Modo docente.** Añade `?docente` a la dirección (por ejemplo, `http://localhost:8000/?docente`) para abrir cualquier etapa sin completar las anteriores.
- **Progreso.** Las etapas completadas se recuerdan solo en ese navegador. Para reiniciar, borra los datos del sitio en el navegador.
- **«Saber más».** Cada etapa tiene un panel con la explicación, preguntas y la fuente.

### Datos inventados y simplificaciones (declarados en la propia actividad)
- El terreno de la etapa 1 y las fincas y cifras de la etapa 5 son inventados.
- Las etapas 2 y 3 usan exageración vertical (−8 %). La etapa 4 muestra la pendiente de ejemplo, 0,3 %.
- En la cantonera, el caudal de cada boca se toma proporcional a su abertura y las tablas encajan cada 5 cm.

### Fuentes de contenido
- Vitruvio, *De architectura*, VIII, 5: descripción del corobate. VIII, 6: pendiente de los canales.
- Lewis, M. (1999). Vitruvius and Greek aqueducts. *Papers of the British School at Rome*, *67*, 145-172. https://doi.org/10.1017/S0068246200004530. Explica que los manuscritos de Vitruvio y de Plinio dan cifras de pendiente distintas.
- UNESCO, «Old Town of Segovia and its Aqueduct», inscrito en 1985: https://whc.unesco.org/en/list/311
- Real Academia Española, *Tesoro de los diccionarios históricos de la lengua española*, entrada «cantonera»: https://www.rae.es/tdhle/cantonera
- Heredad de Aguas de Arucas y Firgas. Se cita sin fecha porque solo se ha consultado una fuente secundaria; conviene contrastarla con la bibliografía del Archivo Histórico Provincial o de la propia Heredad.

Los saberes deben contrastarse con el Decreto 211/2022 (currículo de Primaria en Canarias) antes de redactar la situación de aprendizaje.

## Puesta en marcha

### 1. Instalar el modelo de manos

No se incluye. Descárgalo desde:

`https://storage.googleapis.com/mediapipe-models/hand_landmarker/hand_landmarker/float16/1/hand_landmarker.task`

Guárdalo como `modelo/hand_landmarker.task`. Antes de redistribuirlo fuera del centro, revisa sus condiciones de uso en la documentación de MediaPipe.

### 2. Modelo remoto (desactivado en esta edición)

Esta edición trae `PERMITIR_MODELO_REMOTO = false`: la página nunca descarga el modelo de Google. Si quieres permitirlo, cambia el valor a `true`.

### 2 bis. Valores posibles

En `index.html` está la línea `const PERMITIR_MODELO_REMOTO = true;`.
- Con `true`, si falta el modelo local, se descarga de Google.
- Con `false`, nada sale del centro. Si falta el modelo, la actividad pasa al modo táctil con un aviso.

### 3. Publicar en GitHub Pages

1. En github.com, crea un repositorio **público** (por ejemplo, `mision-roma`). Con la cuenta gratuita, Pages solo funciona en repositorios públicos.
2. Entra en «Add file → Upload files» y arrastra **el contenido** de esta carpeta, de modo que `index.html` quede en la raíz. Pulsa «Commit changes».
3. Entra en «Settings → Pages» y elige «Deploy from a branch», `main` y `/ (root)`. Pulsa «Save».
4. Abre `https://TU-USUARIO.github.io/mision-roma/`. Para el modo docente, añade `?docente` al final.

GitHub registra la IP de quienes visitan el sitio. Comunícalo al delegado o la delegada de protección de datos antes de usarlo con alumnado.

### 3 bis. Servir la carpeta en otro sitio

No funciona con doble clic: los navegadores bloquean los módulos y la cámara en `file://`.

- **En el propio equipo:** ejecuta `python3 -m http.server 8000` en la carpeta y abre `http://localhost:8000`.
- **En las tabletas:** publica la carpeta en un servidor con **https**. Sin https funciona en modo táctil, pero no con las manos.

### 4. Comprobar la integridad

Ejecuta `sha256sum -c MANIFIESTO.txt`. Además, la página verifica `lib/three.module.js` y `lib/vision_bundle.mjs` con SRI.

## Privacidad

- La imagen se procesa en el dispositivo y no se graba ni se envía.
- Por defecto solo se ven unas manos dibujadas, no la imagen del alumnado.
- La cámara se apaga al salir, al ocultar la página y si falla el arranque.
- El progreso guardado solo contiene qué etapas están hechas, sin datos personales.

Su uso con menores debe valorarse con el delegado o la delegada de protección de datos del centro.

## Verificación realizada (Chromium sin interfaz)

- Recorrido completo de las cinco etapas con controles y con arrastres reales de puntero.
- Ninguna violación de accesibilidad con axe-core (WCAG 2.2 AA) en las cinco etapas ni en sus paneles. El foco se gestiona en los diálogos.
- HTML válido.
- Encuadre comprobado en móvil vertical, móvil horizontal y tableta.
- Sin peticiones externas salvo el modelo, cuando falta y está permitido.
- La cámara se apaga cuando el detector no arranca.

**Pendiente:**
- Prueba de la pinza real con alumnado y en las tabletas del aula.
- Revisión de Safari para iPad.
- Revisión humana de los contenidos y de la adecuación curricular.
