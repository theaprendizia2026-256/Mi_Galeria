# Informe de Ingeniería: Mi Galería Digital

<p align="center">
  <img src="images/logo.png" alt="Logo Galería" width="300">
</p>

Galería digital de libre acceso, desarrollada de manera nativa con HTML, CSS y JavaScript como una Progressive Web App (PWA) para la exhibición de obras plásticas, óleos y dibujos.

## Índice
I. Introducción  
II. Identificación del Problema  
III. Objetivos del Proyecto  
      Objetivo General  
      Objetivos Específicos  
IV. Características del Negocio  
V. Requerimientos del Proyecto  
      Metodología (Scrum)  
      Historias de Usuario  
      Requerimientos funcionales y no funcionales  
VI. Diseño de la Solución  
      BPMN  
      Casos de uso  
      Componentes  
      Modelo de datos  
VII. Planificación del Proyecto  
      Cronograma  
      Product Backlog  
VIII. Desarrollo  
* Especificación de Arquitectura  
* Descripción de las tecnologías  
* Integración de las tecnologías  
* Implementación de la solución  
* Aplicación de métodos, estándares y buenas prácticas  
* Ajuste del Cronograma  
IX. Conclusiones  
X. Marco Teórico y fuentes bibliográficas  
XI. Referencias Bibliográficas

---

## I. Introducción
El presente informe documenta el desarrollo de una Progressive Web App (PWA) de exhibición artística, diseñada bajo el paradigma de la Ingeniería de Invisibilidad. La aplicación tiene como propósito fundamental ofrecer un espacio minimalista para la visualización de obras plásticas, óleos y dibujos, optimizado para una navegación fluida y absoluta autonomía digital. A diferencia de las plataformas convencionales, este software se rige por el principio de mínimos recursos y máxima eficiencia, eliminando cualquier componente estético o lógico que no cumpla una función crítica demostrable. La simplicidad de su interfaz oculta una ingeniería basada en Vanilla JavaScript y CSS Grid, garantizando que la tecnología se funda con la experiencia del usuario de manera silenciosa.

## II. Identificación del Problema
En el ecosistema digital actual, las plataformas de arte suelen estar saturadas de interfaces pesadas, menús redundantes y un consumo excesivo de memoria RAM debido al uso de frameworks innecesarios. Esta "deuda técnica" y visual genera fricción en el espectador. Los problemas detectados son:
* **Distracción Visual:** Las interfaces convencionales impiden que el usuario mantenga el enfoque exclusivo en las obras expuestas.
* **Degradación del Rendimiento:** El uso excesivo de bibliotecas de terceros y elementos pesados satura el hardware en dispositivos de gama media o baja.
* **Falta de Autonomía:** Dependencia de ecosistemas cerrados que dificultan el acceso libre, rápido y multiplataforma a los trabajos visuales.

## III. Objetivos del Proyecto
### Objetivo General
Desarrollar una infraestructura de software robusta y minimalista mediante una Progressive Web App (PWA), que proporcione un entorno de exhibición artística de libre acceso. El sistema debe operar bajo el paradigma de la Optimización, garantizando una experiencia de usuario fluida y un consumo mínimo de recursos, facilitando su despliegue y ejecución en la plataforma Vercel.
### Objetivos Específicos
* **Eficiencia de Hardware:** Eliminar el uso de frameworks pesados y dependencias de terceros, utilizando exclusivamente HTML5, CSS3 y Vanilla JavaScript para asegurar la ligereza absoluta del sistema.
* **Arquitectura Cloud-Native:** Implementar una solución preparada para Vercel, aprovechando su infraestructura para garantizar disponibilidad global, seguridad SSL nativa y tiempos de carga instantáneos.
* **Ergonomía Funcional:** Diseñar una interfaz limpia que suprima elementos distractores, centrando la atención únicamente en la visualización de alta resolución de las obras.
* **Instalación Nativa (PWA):** Integrar un Web Manifest y Service Worker para permitir la instalación directa en dispositivos móviles y de escritorio.

## IV. Características del Negocio
El proyecto se define como un activo digital de acceso abierto y gratuito, diseñado para difundir creaciones artísticas sin barreras económicas ni fricción. Sus características principales son:
* **Finalidad Artística:** Herramienta de uso libre orientada a la exposición permanente de óleos, dibujos y obras plásticas del autor.
* **Modelo sin Fricción:** Al ser de libre acceso y no requerir registro de usuario, se elimina cualquier barrera de entrada, priorizando la visualización inmediata.
* **Ausencia de Monetización Invasiva:** El software está libre de publicidad y sistemas de rastreo comerciales, garantizando un espacio limpio y privado.
* **Bajo Costo Operativo:** Gracias a su arquitectura técnica simplificada y al despliegue en la capa gratuita de Vercel, el mantenimiento del sistema es de costo cero.

## V. Requerimientos del Proyecto
### Metodología (Scrum)
Se aplicó un Scrum de ciclo único, priorizando la agilidad y la entrega de un producto funcional inmediato.
* **Planificación:** Definición de la estructura de la galería y los recursos visuales requeridos.
* **Ejecución:** Desarrollo diario enfocado en la maquetación responsiva y la compatibilidad PWA.
* **Revisión:** Pruebas en tiempo real sobre Vercel para asegurar la velocidad de carga y la correcta persistencia de caché.

### Historias de Usuario
* **Como visitante**, quiero una interfaz sin distracciones para explorar obras plásticas y óleos con un solo click.
* **Como crítico o coleccionista**, necesito que la app consuma el mínimo de recursos para visualizar los detalles de las obras sin bloqueos.
* **Como usuario móvil**, deseo instalar la galería como una app nativa (PWA) para acceder rápidamente desde mi pantalla de inicio.

### Requerimientos Funcionales (RF)
* **RF1 - Visualización de Obras:** El sistema debe renderizar en una cuadrícula ergonómica las piezas artísticas almacenadas.
* **RF2 - Adaptabilidad Responsiva:** Redimensionamiento fluido de las imágenes según el viewport del dispositivo.
* **RF3 - Persistencia PWA:** Uso de un Manifest y Service Worker para permitir la instalación y el funcionamiento optimizado en dispositivos.

### Requerimientos No Funcionales (RNF)
* **RNF1 - Simplicidad de Código:** Desarrollo basado exclusivamente en Vanilla Stack (HTML, CSS, JS) sin compiladores.
* **RNF2 - Velocidad de Carga:** El sitio debe estar operativo en menos de 2 segundos tras el despliegue en Vercel.
* **RNF3 - Disponibilidad:** Funcionamiento garantizado 24/7 mediante infraestructura Cloud-Native.

## VI. Diseño de la Solución
En este capítulo se detalla la arquitectura lógica y funcional del sistema, orientada a la Optimización absoluta de los recursos y la eficiencia del despliegue en la nube mediante diagramas Mermaid.

### 1. BPMN (Diagrama de Procesos)
```mermaid
graph TD
    A[Inicio: Usuario accede a la Web/PWA] --> B{¿Desea instalar?}
    B -- Sí --> C[Instalar PWA en pantalla de inicio]
    B -- No --> D[Navegar directamente en navegador]
    C --> E[Cargar activos desde caché y Supabase]
    D --> E
    E --> F[Visualización de Galería y Obras]
    F --> G[Fin del flujo interactivo]
