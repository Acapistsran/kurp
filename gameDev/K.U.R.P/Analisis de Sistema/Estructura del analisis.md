#### 1. **Introducción**

- **Objetivo**: Planificar el desarrollo de los módulos y las características del videojuego
- **Alcance**: Requisitos previamente descritos

#### 2. **Descripción General del Sistema**

- **Visión del Juego**: Sandbox/survival de exploración espacial con combate escalable
- **Plataformas**: PC principalmente (Posiblemente tenga potencial en consola pero se tendria que adaptar a un estilo de juego mas veloz, o dinamico para jugadores casuales)

#### 3. **Módulos del Sistema**
(Consultar por separado en su carpeta)
- [[Modulo de personajes]]
- [[Modulo de construcción]]
- [[Modulo de combate]]
- [[Modulo de Multijugador]]
- [[Modulo de inventarios]]
- [[Modulo de Vuelo]]

#### 4. **Datos y Flujos de Información**

- **Estructura de Datos**: Define qué datos manejará el sistema (ej. estadísticas de personajes, datos de construcción de naves, inventarios de recursos).
	- Personajes
		- Estadisticas
			- Nombre
			- Raza
			- HP
			- XP (Nivel)
			- Inventario
		- Apariencia
	- Naves
		- Tripulacion
		- Inventario
			- Municion
			- Cargamento
		- Armamento
		- Sistemas de defensa
	- Bases
		- Almacenamiento
			- Contenedores
		- Torretas
			- Tipo de daño
			- Municion
			- Control (Personaje o IA)
- **Flujo de Información**: 
	- Inventarios
		- Limites: Los inventarios tendran una capacidad limitada de espacios o "slots" de inventario, y cada item tendra un limite especifico de cuantas unidades de ese item se pueden guardar en ese slot
		- Restricciones: Habra inventarios para tipos especificos de objetos, como los inventarios de municion en torretas automaticas, o los espacios de municion en los inventarios de los jugadores. Sin embargo, aunque algunos inventarios parezcan tener restricciones, no siempre las tendran (Por ejemplo, poder guardar objetos que no sean comida en un refrigerador)
	- Combate
		- Municion: La municion se resta en tiempo real de los inventarios, sea municion balistica o de energia, dependiendo de que arma la este usando
		- Daño: El daño se calcula en base al blindaje que hay en el objetivo restado al daño base del arma. 
		- Precision: Dependiendo del nivel del arma y del objetivo, puede haber una pequeña posibilidad de fallar un ataque, o de bloquear todo el daño. Esto es mas aparente en armas de nivel bajo, como combate melee de early game
#### 5. **Reglas del Sistema**

- **Reglas de Juego**: 
	- Personajes
		- Humanos
			- Necesidades basicas: Agua, comida y oxigeno
			- Riesgos de los elementos: Los planetas pueden ser muy inhospitos en el espacio exterior fuera de casa, ya sea que su atmosfera no resista la radiacion de su estrella, o que sufra de tormentas que lo enfrien casi al cero absoluto, necesitan tener alguna manera de mantenerse con vida
			- Mayor capacidad de aprendizaje: Los humanos son curiosos por naturaleza, y aprenden mas rapido que las demas especies, dandoles un bonus en la experiencia que ganan y permitiendoles desbloquear tecnologias mas rapido
		- Aliens
			- Adaptaciones: Dependiendo del planeta en el que se desarrollen estas criatuas, pueden contar con ojos extras que les permitan ver en la oscuridad, un exoesqueleto blindado y resistente a la radiacion, o incluso alas que les permitan volar en planetas con atmosfera. Pero cada adaptacion viene con sus desventajas, como menor capacidad de carga o velocidad de movimiento, o fotosensibilidad para los que tienen muchos ojos, por mirones
			- Necesidades: Los aliens tambien son seres vivos, y como casi cualquier forma de vida, necesitan agua y comida. Lo que coman dependera de la base de su especie, ya sean herbivoros, carnivoros u omnivoros. 
		- Robots
			- Modificacion de partes: Los robots pueden cambiar distintas partes de su cuerpo por otras, cada una con sus ventajas y desventajas como mayor coste de energia o peso, pero a cambio de armas laser, mayor capacidad de energia, etc
			- Desgaste: Los robots resisten el vacio del espacio y la dureza de los elementos en la mayoria de los planetas, pero sus partes sufren desgaste despues de un tiempo y necesitan mantenimiento, ya sea de ellos mismos o por otro personaje
			- Energia: Los robots consumen carga electrica para mantenerse en funcionamiento, y se pueden recargar de diferentes maneras, o incluir pequeños generadores dentro de si mismos que les permitan recargarse despues de un descanso
	- Multijugador
		- Early-game
			- El juego se centraria en un modelo PVE Cooperativo mientras dos o mas amigos juegan con sus personajes que aparecen en un mismo planeta. Tendrian que recolectar recursos para todos los personajes que lo necesiten, y defenderse de las amenzas del planeta, como invasiones de aliens o criaturas de la tierra. El PVP estaria desactivado por defecto 
		- Mid-Game
			- Los jugadores tendrian la oportunidad de viajar a otros planetas del sistema solar, explorando, avanzando y construyendo bases. El juego se seguiria centrando en el modo cooperativo, pero considerando que los jugadores en diferentes planetas podrian tener momentos dificiles para colaborar, dependerian de su tripulacion no comandada (Personajes no activos) para apoyarse mutuamente. El PVP se permite, pero no se sugiere a los jugadores (Desactivado por defecto, activable en la configuracion)
		- Late-Game
			- En esta fase del juego, el grupo inicial de amigos ya se encuentra con otros grupos de jugadores a medida que crece su influencia en la galaxia. Las alianzas seran necesarias de no querer enfrentarse en feroces guerras estelares de flotas espaciales. El PVP no es opcional en este punto, pero el fuego amigo esta desactivado (Con la posibilidad de causar daño colateral a tus aliados con ataques en area que causen, por efecto, quemaduras)
	- combate
		- Early-game
			- Esta es la fase del juego en la que apenas puedes fabricar armas de fuego basicas con lo que se encuentra tirado en el planeta. Pistolas, rifles y escopetas, suponiendo que puedes aprender a fabricarlas, desbloqueando su tecnologia al subir de nivel. De lo contrario, puedes subir de nivel el combate melee, que te ayudara a combatir contra enemigos desarmados y cualquier cosa que se acerque lo suficiente como para pegarle un golpe 
		- Mid-game
			- En esta fase puedes aprender nuevas tecnologias de combate. Armas con modificaciones, diferentes tipos de municion (Antiblindaje, punta hueca, incendiarias, trazadoras, etc) ademas de investigar calibres mas grandes, que te permitiran fabricar cañones pesados para tus vehiculos (En esta fase, los vehiculos se vuelven muy importantes)
			- Las armas laser empiezan a ser una posibilidad, pero al necesitar tanta energia, mejor le das otro uso a esos laseres, como designadores de objetivos para bombas o misiles guiados por laser
			- Tus nuevas tecnologias que te permitieron salir del planeta tambien te permiten lanzar objetos explosivos muy rapido. Misiles!
			- Y para darle energia a toda tu base, necesitaras el poder del atomo! Los reactores nucleares, ademas de energia, producen material nuclear fisible, que puede convertirse en potentes bombas nucleares que acaban con bases enteras en un abrir y cerrar de ojos
		- Late-game
			- En este punto, probablemente ya seas una civilizacion de clase 2, y lo unico que te impide progresar son los demas jugadores avariciosos que acaparan todas esas estrellas... entonces, por que no usar el poder de tu estrella, y construir armas con su energia nuclear? Descubres tecnologias que te permiten concentrar cantidades considerables de antimateria, y utilizas eso para convertirlo en un arma de destruccion masiva, capaz de destruir una luna con tan solo un kilogramo de anti-hidrogeno
			- Pero... eso no es ninguna luna... es una estacion espacial! (Guerra de las estrellas referencia)
			- Las naves ahora son colosales, se construyen en el espacio, y llevan otras naves mas pequeñas protegiendolas
	- construccion
		- El sistema de construccion de naves y bases debe estar unificado, pero debe diferenciar cuando el jugador intente construir algo pequeño (Avion de combate atmosferico) y algo grande (invernadero, o una estacion espacial)
		- Construccion de naves
			- El sistema debe tener la flexibilidad de poder personalizar la forma de las alas y estructuras de la nave, pero debe hacer esto con componentes prefabricados para poder permitir que las plantillas tengan una cantidad especifica de materiales, pero tambien que los jugadores experimentados creen sus propios diseños
		- Construccion de bases
			- Utilizando los prefabricados que se utilizan para las naves, se pueden crear prefabricados mas grandes y resistentes, que sirvan como muros de habitaciones, almacenes y hasta hangares para las estaciones espaciales
			- Se debe incluir la fabricacion de maquinas para el procesamiento de recursos, como hornos, centrales quimicas, cultivos hidroponicos automaticos, etc
				- Se debe incluir una capa de automatizacion, ya sea con los propios personajes manejando las maquinas sin necesidad ncesidad de interaccion del jugador, o que se construyan lineas de fabricacion con cintas transportadoras y brazos roboticos que se encarguen de mover los objetos entre maquinas y contenedores
- **Reglas de Interacción entre Jugadores y Mundo**: Explica cómo las acciones de los jugadores afectan el mundo del juego (ej. la terraformación de un planeta cambia su atmósfera).

#### 6. **Restricciones Técnicas**

- **Limitaciones de Rendimiento**: El motor Godot, aunque muy flexible, se ve limitado por la capacidad de la computadora en la que se ejecute, que en este caso, es mi pc principal, que tiene un CPU i5 6600 K, 16 gb RAM ddr3, y una tarjeta grafica geforce 1650 de 4gb de vram
- **Consideraciones de Seguridad**: Tratandose de un juego open source, los problemas que puedan surgir seran publicamente disponibles en cuanto se publique una situacion en la pagina de github. La manera mas apropiada de evitar exploits, seria primero construyendo un sistema robusto que resista intentos de manipulacion, y despues con un equipo de moderacion que vigile los diferentes aspectos del juego y este pendiente de posibles intentos de exploits o hackers

#### 7. **Evaluación de Riesgos**

- **Posibles Problemas**: 
	- desbalance de combate (Las armas de late game serian totalmente devastadoras contra jugadores nuevos)
	- problemas de rendimiento (Simular un sistema planetario es *bastante* pesado en cuestion de recursos)
	- dificultad para integrar tecnologías avanzadas (falta de conocimiento con el motor de godot pueden llevar a no saber como realizar algunas acciones o caracteristicas)
	- Falta de presupuesto(tiempo, y $)
- **Medidas de Mitigación**: Propón soluciones para prevenir o resolver esos problemas.
	- Darle su espacio a los jugadores nuevos, o hacer un early game exclusivamente offline, y que solamente se necesite conectar al internet despues de salir del sistema solar en el que aparece el jugador
	- Simular del lado del jugador unicamente lo que se esta viendo en ese momento, como puede ser el planeta, y utilizar diferentes tecnicas de renderizado escalar para que solamente lo mas relevante sea procesado por la computadora del jugador. El combate PVP tendria un periodo de sincronizacion un poco mas lento, pero se podria utilizar como excusa la "velocidad de la luz" para decir que tarda un rato en llegar una señal o la imagen de punto a punto
	- Tengo que seguir investigando sobre godot. Por mas que me guste hacer la planeacion, tengo miedo de cuando termine esta fase y de verdad tenga que empezar a escribir codigo, y yo este en blanco por nunca haber visto ni siquiera un tutorial ni tener ningun tipo de experiencia...
	- Se recurrira al Crowdsourcing para que la gente interesada en el juego tambien pueda apoyar al desarrollo creando sus propios modulos o corrigiendo errores mediante las versiones open source que se publicarian en github