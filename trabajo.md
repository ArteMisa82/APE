2.6.3.  HEURÍSTICAS DE NIELSEN
2.6.3.1.  Evaluación heurística
Tabla 6. Evaluación de las diez heurísticas de Nielsen. Fuente: elaboración propia con base en Nielsen [5].
N.º	Heurística
	Evaluación	Problema encontrado	Mejora Propuesta
1	Visibilidad del estado del sistema	Parcial	El usuario puede no saber claramente si una acción está procesándose.
	Mostrar mensajes de estado y confirmación
2	Correspondencia con el mundo real	Cumple	Utiliza términos relacionados con servicios bancarios.
	Mantener lenguaje sencillo.
3	Control y Libertad	Parcial	Algunas acciones pueden generar dudas al regresar o cancelar.
	Incorporar botones claros de volver y cancelar.
4	Consistencia y estándares	Cumple	Mantiene patrones similares de navegación.
	Mantener la consistencia.
5	Prevención de errores	Parcial	Algunos formularios pueden requerir mayor orientación
	Validación y mensajes específicos.
6	Reconocer, no recordar	Cumple	Las opciones principales son identificables.
	Mantener etiquetas claras.
7	Flexibilidad y eficiencia	Parcial	Algunas acciones pueden requerir varios pasos.
	Incorporar accesos rápidos.
8	Estética y diseño minimalista	Parcial	Existen bastante información sobre servicios
	Organizar y priorizar contenidos.
9	Diagnóstico y recuperación	Parcial	Los mensajes de error pueden requerir mayor orientación.	Explicar cómo solucionar el error.
10	Ayuda y documentación	Parcial	Algunos servicios requieren información adicional	Mejorar FAQ y ayudas contextuales.

Matriz detallada de las diez heurísticas de Nielsen
ID	Campo	Registro
N01	Heurística	Visibilidad del estado del sistema
	Estado	No cumple
	Pantalla	Transferencia y pago
	Tarea	T2 y T3
	Problema	El usuario puede no reconocer si la operación se procesa, falla o termina.
	Captura o evidencia	Figuras 8, 12 y resultados de tareas
	Severidad	4 - Crítica
	Recomendación	Indicador de proceso, estado textual y comprobante inequívoco.
	Condición de corrección	Cada estado se anuncia visualmente y por aria-live en ≤ 1 s; 0 repeticiones accidentales.
N02	Heurística	Correspondencia entre el sistema y el mundo real
	Estado	Cumple
	Pantalla	Inicio y Banca Web
	Tarea	T1, T2 y T3
	Problema	Algunos términos como transferencia directa e interbancaria pueden no ser cotidianos.
	Captura o evidencia	Figuras 6, 9 y 11
	Severidad	2 - Media
	Recomendación	Añadir descripciones breves y ejemplos junto a términos financieros.
	Condición de corrección	≥ 90 % interpreta correctamente las opciones sin ayuda.
N03	Heurística	Control y libertad del usuario
	Estado	No cumple
	Pantalla	Formularios transaccionales
	Tarea	T2 y T3
	Problema	Cancelar, volver o corregir puede resultar ambiguo y perder contexto.
	Captura o evidencia	Figuras 7, 8 y 12
	Severidad	3 - Alta
	Recomendación	Controles Volver y Cancelar visibles que conserven datos válidos.
	Condición de corrección	El usuario retrocede y corrige sin reiniciar ni perder información.
N04	Heurística	Consistencia y estándares
	Estado	Cumple
	Pantalla	Las tres pantallas
	Tarea	T1, T2 y T3
	Problema	No se detectó inconsistencia grave en los patrones principales.
	Captura o evidencia	Figuras 1, 2, 6 y 9
	Severidad	1 - Baja
	Recomendación	Mantener etiquetas, jerarquía y posición de acciones equivalentes.
	Condición de corrección	Mismos nombres y patrones en el 100 % de flujos equivalentes.
N05	Heurística	Prevención de errores
	Estado	No cumple
	Pantalla	Transferencia y pago
	Tarea	T2 y T3
	Problema	Datos de beneficiario, monto o servicio pueden introducirse con formato incorrecto.
	Captura o evidencia	Figuras 7, 8, 11, 12 y tasa de error 40 %
	Severidad	4 - Crítica
	Recomendación	Validación inmediata, formato visible y resumen antes de confirmar.
	Condición de corrección	≤ 10 % de ejecuciones con error y 0 confirmaciones con datos inválidos.
N06	Heurística	Reconocimiento antes que recuerdo
	Estado	No cumple
	Pantalla	Transferencia y pago
	Tarea	T2 y T3
	Problema	El usuario debe recordar beneficiarios, categorías, formatos y datos externos.
	Captura o evidencia	Figuras 7 y 11
	Severidad	3 - Alta
	Recomendación	Favoritos, historial, ejemplos y selección visible de datos recientes.
	Condición de corrección	La tarea se completa sin consultar fuentes externas en ≥ 90 % de casos.
N07	Heurística	Flexibilidad y eficiencia de uso
	Estado	No cumple
	Pantalla	Inicio y módulos transaccionales
	Tarea	T2 y T3
	Problema	Las operaciones frecuentes requieren varios pasos y búsquedas.
	Captura o evidencia	Figuras 16, 17 y 18
	Severidad	3 - Alta
	Recomendación	Accesos rápidos, recientes, favoritos y búsqueda tolerante.
	Condición de corrección	Reducir el tiempo medio de T2 y T3 al menos 25 %.
N08	Heurística	Estética y diseño minimalista
	Estado	No cumple
	Pantalla	Inicio
	Tarea	Localizar accesos para T1, T2 y T3
	Problema	Carruseles y abundancia de productos compiten con las acciones principales.
	Captura o evidencia	Figuras 13, 14 y 16
	Severidad	2 - Media
	Recomendación	Priorizar operaciones frecuentes y reducir contenido simultáneo.
	Condición de corrección	Las tres acciones oficiales se localizan en ≤ 10 s sin ayuda.
N09	Heurística	Ayudar a reconocer, diagnosticar y recuperarse de errores
	Estado	No cumple
	Pantalla	Inicio de sesión y formularios
	Tarea	T1, T2 y T3
	Problema	Los errores pueden no explicar campo, causa y solución.
	Captura o evidencia	Figura 15 y hallazgo WAVE de etiqueta ausente
	Severidad	3 - Alta
	Recomendación	Mensaje específico junto al campo, resumen y anuncio mediante role="alert".
	Condición de corrección	100 % de errores identifica campo, causa y acción correctiva.
N10	Heurística	Ayuda y documentación
	Estado	No cumple
	Pantalla	Inicio y formularios
	Tarea	T1, T2 y T3
	Problema	La ayuda contextual no siempre acompaña el punto de decisión.
	Captura o evidencia	Figura 1 y recorridos de tareas
	Severidad	2 - Media
	Recomendación	Ayuda breve junto a campos y acceso directo a soporte.
	Condición de corrección	Ayuda localizable en ≤ 2 acciones y ≥ 90 % resuelve la duda sin abandonar.
Tabla 6A. Registro completo de las diez heurísticas de Nielsen.
•	Visibilidad del estado del sistema
Banco de Pichincha presenta diferentes acciones mediante botones y enlaces, permitiendo al usuario identificar que puede realizar dentro del sitio. Sin embargo, en procesos que llevan al usuario hacia otra plataforma o ventana, es importante que el sistema indique claramente qué está ocurriendo después de seleccionar una opción.  (UIX, 2025)

 
Figura 13. Evidencia de visibilidad del estado del sistema en el portal. Fuente: Banco Pichincha [4].

•	Control y libertad del usuario
El sitio permite al usuario navegar entre diferentes categorías de productos y utilizar filtros para encontrar opciones especificadas. Esto proporciona cierto control sobre la navegación. Sin embargo, debido a la cantidad de productos y opciones disponibles, el usuario puede necesitar realizar varios pasos antes de llegar a la información específica que busca.

 
Figura 14. Evidencia de control y libertad durante la navegación. Fuente: Banco Pichincha [4].

•	Prevención de errores
En un sitio bancario, los formularios requieren que el usuario ingrese información correctamente. Banco Pichincha dispone de diferentes procesos digitales relacionados con solicitudes, simuladores y productos en línea. Los formularios pueden generar errores si el usuario no conoce exactamente el formato requerido para cada dato. 

 
Figura 15. Evidencia de prevención de errores en formularios digitales. Fuente: Banco Pichincha [4].

•	Flexibilidad y eficiencia de uso
El sitio proporciona accesos directos a diferentes servicios, lo que facilita que los usuarios puedan encontrar algunas funciones sin ingresar a demasiados menús. La sección de soluciones y las consultas rápidas permiten acceder directamente a servicios específicos. 

 
Figura 16. Evidencia de flexibilidad y eficiencia mediante accesos a servicios. Fuente: Banco Pichincha [4].

La evaluación de las 10 heurísticas de Nielsen permitió identificar que el sitio web de Banco Pichincha presenta un nivel de usabilidad generalmente adecuado, ya que cuenta con una estructura de navegación, categorías de servicios y elementos que permiten al usuario encontrar información y realizar diferentes acciones. Sin embargo, también se identificaron varias oportunidades de mejora relacionadas principalmente con la visibilidad del estado del sistema, el control y libertad del usuario, la prevención y recuperación de errores, la flexibilidad y el diseño minimalista.


