Simulación de Ecosistema 2D en Unity: Defensa verde.

- Características Principales

- Agentes y sus Roles Definidos:
    - Plantas: Defensores fijos que atacan a los zombis disparando proyectiles.
    - Zombis: Atacantes que avanzan hacia la casa, atacando cualquier planta que encuentren en su camino. Algunos zombis aparecen con características aleatorias (más fuertes o más rápidos).
    - Casa: El objetivo principal de los zombis.
    - Estados y Comportamientos: Cada entidad posee estados internos (ejemplo: salud, cooldown de ataque) y comportamientos bien definidos que rigen sus acciones.
    - Recursos Limitados: La salud de las plantas, los zombis y la casa es un recurso limitado.
    - Dinámicas Emergentes: Las interacciones locales entre plantas y zombis dan lugar a patrones de avance y defensa.
    
- Condiciones de Victoria/Fracaso:
    - Victoria: La casa resiste todas las oleadas de zombis.
    - Derrota: Un zombi logra alcanzar y entrar en la casa.
    
- Gestión de Oleadas: El GameManager orquesta la aparición de zombis en oleadas, aumentando progresivamente la dificultad.
- Interfaz de Usuario Básica: Muestra el estado del juego (oleada actual, victoria/derrota) y un botón de reinicio.
- Sonidos: Integración de efectos de sonido para enriquecer la experiencia (spawn de zombis, ataque de zombis, llegada a la casa).

- Cómo Ejecutar la Simulación

1.  Clonar (o descargar directamente) el Repositorio.
2.  Abrir en Unity:
    - Abrir Unity Hub.
    - Hacer clic en "Add Project" y seleccionar la carpeta raíz del repositorio clonado.
    - Abrir el proyecto con la versión de Unity especificada (6000.2.4f1 o compatible).
3.  Navegar a la Escena Principal:
    - En la ventana Project, buscar la carpeta Assets/Scenes.
    - Abrir la escena principal de la simulación.
4.  Iniciar la Simulación:
    - Hacer clic en el botón Play en la parte superior de la ventana de Unity para comenzar. Puede cambiar párametros y estadiísticas tanto de plantas como zombis en  el inspector.

- Componentes Clave del Proyecto:

   - Agent.cs: Clase base abstracta para todas las entidades con salud, estado de vida y un método Simulate.
   - Plant.cs: Implementa el comportamiento de las plantas: fijas, atacan zombis con proyectiles en su carril.
   - Zombie.cs: Implementa el comportamiento de los zombis: avanzan hacia la casa, atacan plantas. Incluye modificadores aleatorios (fuerza, velocidad).
   - Projectile.cs: Define el comportamiento de los proyectiles disparados por las plantas.
   - House.cs: Representa la casa, el objetivo final de los zombis. Maneja la condición de derrota al ser alcanzada.
   - Simulate.cs: Centraliza las llamadas al método Simulate de todas las plantas y zombis activos en la escena, gestionando el flujo principal de la simulación.
   - GameManager.cs: Controla el ciclo de vida de la simulación: generación de oleadas de zombis, condiciones de victoria/derrota, gestión de UI y reinicio.

