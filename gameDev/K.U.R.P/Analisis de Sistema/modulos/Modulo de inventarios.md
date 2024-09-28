- **Descripción del modulo**: Modulo encargado del manejo de objetos y recursos necesarios para que el jugador realize todas las acciones que necesiten alguna materia prima, o tambien del maneja de armadura en los personajes, y de su capacidad de carga
- **Requisitos Funcionales**: Se debe permitir que el usuario tenga espacios de inventario en sus personajes para que puedan utilizar armas y objetos para la construccion de bases y naves. Este sistema se encarga de manejar el almacenamiento de recursos y materias primas en diferentes maneras, pudiendo tratar con liquidos como combustibles en tanques estacionarios y portatiles, municion en cajas, y metales y compuestos para la construccion de estructuras
- **Requisitos No Funcionales**: Se debe balancear el sistema para que no se puedan almacenar demasiados objetos, pero permitiendo aumentar la capacidad de almacenamiento. Por ejemplo, una caja de 100 balas de cualquier tipo se puede almacenar normalmente en cualquier espacio de inventario vacio que permita almacenarlas, pero se puede modificar para que despues puedan apilarse las cajas, y puedan almacenar hasta 200 con una investigacion de tecnologia de apilamiento, y luego el doble con una investigacion mas avanzada
- **Interacciones con otros Módulos**: 
	- [[Modulo de personajes]] (Manejo de inventarios en personajes, y su capacidad de carga).
	- [[Modulo de construcción]]: Manejo de materias primas y recursos necesarios para su refinamiento, procesamiento y su utilizacion en la construccion de naves y estructuras
	- 