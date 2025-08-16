## Descripción del Proceso:

El proceso de agendamiento de servicios médicos modelado representa el flujo completo desde que un paciente solicita una cita hasta que esta queda confirmada y registrada en el sistema. El proceso abarca múltiples tipos de servicios incluyendo citas médicas y exámenes de laboratorio.
El diagrama BPMN desarrollado utiliza cinco participantes principales. El paciente inicia el proceso mediante una solicitud que puede realizarse por canal digital o telefónico. Esta distinción se modela mediante un gateway exclusivo que direcciona el flujo hacia diferentes rutas de procesamiento. El sistema de agendamiento gestiona la lógica central del proceso, mientras que el personal administrativo maneja específicamente las solicitudes telefónicas. Los sistemas de historia clínica y facturación participan mediante integraciones al sistema de agendamiento.
La consulta de disponibilidad constituye el núcleo del proceso, donde el sistema verifica los recursos disponibles considerando todas las sedes de la organización. Esta verificación se representa mediante un segundo gateway exclusivo que determina si existe disponibilidad inmediata para confirmar la cita o si es necesario ofrecer alternativas de reprogramación. Cuando no hay disponibilidad, el proceso incluye un ciclo de retroalimentación que permite ofrecer nuevas opciones al paciente hasta encontrar una fecha y hora convenientes.

## Buenas Prácticas para el Modelado BPMN

El BPMN es un estándar gráfico para representar procesos de negocio de forma clara y comprensible. Aplicar buenas prácticas asegura no solo la legibilidad, sino también la posibilidad de automatización y mejora continua.

#### Principios Fundamentales

Antes de modelar, define el propósito: documentar el proceso actual (as-is) o diseñar el ideal (to-be). Ten siempre en cuenta la audiencia: un equipo técnico requiere más detalle que la dirección. Prioriza la simpleza y claridad, evitando diagramas sobrecargados. Finalmente, mantén consistencia en nombres, símbolos y estilos.

#### Elementos Clave

Las Piscinas (Pools) representan a un participante principal y los Carriles (Lanes) dividen responsabilidades internas. Cada piscina debe incluir un inicio y un fin.
Nombra tareas con la fórmula “Verbo + Objeto”, como “Recibir pedido” o “Enviar confirmación”.
Los flujos de secuencia deben ser rectos y sin cruces innecesarios.
Usa Gateways exclusivos (X) para decisiones, paralelos (+) para acciones simultáneas y compuertas de convergencia para unir caminos.
Agrupa tareas en subprocesos para simplificar la vista general y mostrar detalles solo cuando sea necesario.
