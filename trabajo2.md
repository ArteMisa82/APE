2.6.6.  PRINCIPIOS POUR Y BARRERA PERCEPTIBLE
2.6.6.1.  Principios POUR
WCAG organiza la accesibilidad mediante cuatro principios. Perceptible exige que la información pueda captarse por distintos sentidos mediante contraste, texto alternativo y equivalentes. Operable requiere que todos los controles funcionen con teclado, presenten foco visible y no produzcan trampas. Comprensible demanda etiquetas claras, navegación predecible y mensajes que expliquen el problema y la corrección. Robusto busca que el contenido mantenga semántica compatible con navegadores y tecnologías de asistencia mediante HTML y ARIA válidos [8].

2.6.6.2.  Contraste y alternativas textuales
El criterio WCAG 1.4.3 establece un contraste mínimo de 4,5:1 para texto normal y 3:1 para texto grande. WAVE detectó cinco casos de contraste muy bajo en textos superpuestos a imágenes del carrusel y mostró una relación calculada de 1:1 respecto del color de fondo de respaldo, por debajo del mínimo. Como el fondo real contiene fotografías, la relación puede variar entre zonas y debe medirse sobre el píxel más desfavorable. En los enlaces azules de contenido se obtuvo aproximadamente 4,51:1 sobre blanco, valor que cumple AA por un margen reducido y conviene elevar para resistir variaciones de pantalla [8].
La inspección estructural registró 44 imágenes. Ninguna carecía del atributo alt, 39 presentaron alternativa textual informativa y 3 utilizaron alt vacío, una práctica válida solo cuando la imagen es decorativa. WAVE también señaló cinco contrastes insuficientes. Por ello, los avatares, logotipos o imágenes que comuniquen productos deben conservar descripciones breves y específicas, mientras que los adornos deben permanecer con alt vacío para evitar ruido en lectores de pantalla.

Elemento revisado	Evidencia	Resultado	Acción medible
Texto sobre banners	5 errores WAVE y razón de respaldo 1:1.	No cumple 4,5:1 de forma garantizada.	Añadir capa oscura o fondo sólido hasta alcanzar ≥ 4,5:1 en toda la imagen.
Enlaces azules sobre blanco	Relación aproximada 4,51:1.	Cumple AA con margen mínimo.	Elevar a ≥ 5:1 para tolerar variaciones.
Imágenes	44 imágenes, 0 sin alt y 3 con alt vacío.	Base adecuada con revisión semántica pendiente.	Confirmar que cada alt vacío corresponda solo a contenido decorativo.
Tabla 9. Resultado de la barrera perceptible. Fuente: evaluación propia con WAVE y revisión del DOM.







2.6.6.3.  Matriz específica POUR
Principio	Criterio WCAG	Resultado	Evidencia	Problema	Severidad	Recomendación
Perceptible	1.1.1 y 1.4.3	No cumple completamente	WAVE: 5 contrastes; 44 imágenes, 3 alt vacíos	Contraste no garantizado sobre banners y revisión semántica pendiente	3 - Alta	Garantizar 4,5:1 en texto normal y validar que todo alt vacío sea decorativo.
Operable	2.1.1, 2.1.2, 2.4.3 y 2.4.7	Cumple parcialmente	Recorrido Tab/Shift+Tab; 66 focos; 0 tabindex positivo	Algunos contornos automáticos son de 1 px y falta cierre con NVDA	2 - Media	Aplicar :focus-visible ≥ 2 px y ejecutar recorrido completo con teclado y NVDA.
Comprensible	3.3.1, 3.3.2 y 3.3.3	No cumple	WAVE: 1 etiqueta ausente; errores 40 % en T2 y T3	Campos y errores pueden carecer de nombre, causa o solución claros	3 - Alta	Asociar label y mostrar error específico con corrección y conservación de datos.
Robusto	4.1.2 y 4.1.3	No cumple	WAVE: 1 referencia ARIA y 1 menú ARIA rotos	Nombre, rol, relación o estado puede anunciarse incorrectamente	3 - Alta	Corregir id/ARIA y validar árbol accesible y anuncios dinámicos sin errores.
Tabla 9A. Matriz específica de principios POUR y criterios WCAG. Fuente: elaboración propia.


2.6.7.  BARRERA OPERABLE
2.6.7.1.  Navegación por teclado y foco
Se recorrió la interfaz con Tab y Shift+Tab desde el aviso de cookies hasta la navegación principal y el carrusel. El orden inicial avanzó por Configuración de cookies, Aceptar cookies, enlace para pasar al contenido principal, Menú, logotipo, Buscar, Abrir cuenta, Acceso clientes y controles del carrusel. No se identificaron valores tabindex positivos ni una trampa de teclado en el tramo evaluado. Los controles mostraron indicadores de foco del navegador o contornos definidos, entre ellos un borde azul sólido de 2 px en Menú y uno celeste de 3 px en los controles del carrusel. La presencia de algunos focos con contorno automático de 1 px justifica reforzar el estilo :focus-visible para que la ubicación actual sea inequívoca [8], [9].
La estructura de accesibilidad expuso nombres y roles para los controles principales, lo cual permite anticipar una lectura comprensible. Sin embargo, WAVE detectó una referencia ARIA rota y un menú ARIA incompleto, hallazgos que pueden afectar el anuncio de relaciones o estados. La validación exacta de voz con NVDA requiere ejecutarse en Windows con el lector de pantalla activo y debe conservarse como prueba de aceptación final. El procedimiento consiste en recorrer toda la página con Tab, Shift+Tab, flechas, Enter y Escape y registrar para cada control el nombre anunciado, el rol, el estado, el orden y la posibilidad de salir sin usar el ratón [11].

2.6.7.2.  Registro de prueba manual con teclado
Aspecto	Resultado registrado	Estado	Evidencia o criterio
Controles inaccesibles	No se identificaron en el tramo inicial evaluado; debe completarse el recorrido de las tres pantallas.	Parcial	66 elementos enfocables detectados.
Orden de Tab	Cookies → salto al contenido → Menú → logotipo → Buscar → Abrir cuenta → Acceso clientes → carrusel.	Cumple en el tramo	Secuencia observada con Tab y retorno con Shift+Tab.
Foco visible	Contorno azul 2 px en Menú, celeste 3 px en carrusel y automático 1 px en otros controles.	Parcial	Estilos computados durante el recorrido.
Trampas de teclado	No se detectó bloqueo en el tramo evaluado.	Cumple en el tramo	Fue posible continuar y retroceder el foco.
Enter, Espacio y Esc	Enter activa enlaces y botones estándar; Espacio debe verificarse en botones y Esc en menús o diálogos.	Parcial	Prueba final pendiente en componentes abiertos.
Tarea completada	Navegación inicial completada; T1, T2 y T3 requieren sesión y datos de prueba para cierre integral.	Parcial	No se usaron credenciales ni operaciones reales.
Tiempo	No registrado para el recorrido de accesibilidad.	NR	Debe cronometrarse en la repetición.
Número de errores	0 bloqueos observados en el tramo; conteo total no registrado.	Parcial	No equivale a una prueba completa de las tres pantallas.
Captura o evidencia	Capturas Lighthouse y WAVE y registro textual de foco.	Disponible	Figuras 20 y 21; tabla presente.
