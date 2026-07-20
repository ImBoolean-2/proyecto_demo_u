# Efecto de un ecosistema virtual inmersivo con zonificación acústica dinámica en el sentido de presencia y la valoración del patrimonio natural en los usuarios de Lima Sur, 2026

Plataforma cooperativa multijugador en Realidad Virtual de Tercera Persona (TPP) desarrollada en **Unity**, diseñada para mitigar la cinetosis (motion sickness) y optimizar el flujo de exploración en metaversos mediante un sistema de **guiado interactivo asimétrico** y soporte de navegación por Inteligencia Artificial (NavMesh).

---

## 🛠️ Especificaciones Técnicas y Arquitectura
El prototipo está estructurado modularmente para garantizar escalabilidad, rendimiento fluido de red y comodidad visual (UX):

### Módulos Principales
* **Módulo Multijugador (Mirror SDK):** Sincronización asíncrona de avatares, estados de animación en red local (LAN) y persistencia de roles asimétricos (Anfitrión/Guía y Turistas).
* **Módulo de Locomoción e IA (NavMesh):** Administra el `AsistenteMagnetico.cs`. Activa un agente en segundo plano si un turista supera un radio de 15 metros del guía, reconduciéndolo de forma orgánica.
* **Módulo Cinemático (CamaraTPP.cs):** Cámara orbital equipada con un trazador de esferas continuas (`Physics.SphereCast`, Radio: 0.4m) que detecta la capa `ObstacleLayer` eliminando la oclusión y el traspaso de mallas (clipping).
* **Módulo UGC Map Manager:** Cargador en tiempo de ejecución (Runtime Layout Manager) que permite al anfitrión importar terrenos `.obj` locales y generar de manera dinámica la superficie de navegación.
* **Módulo de Audio Contextual (AudioTrigger.cs):** Espacialización sonora 3D con atenuación logarítmica activada por triggers en red (evitando bucles redundantes mediante flags booleanas).

---

## 🚀 Requisitos del Sistema (PC Standalone)
* **Sistema Operativo:** Windows 10 / 11 (64-bit)
* **Motor de Desarrollo:** Unity 3D Engine (2022.3 LTS o superior)
* **Arquitectura de Red:** Red Local (LAN) con direccionamiento IP compatible.
* **Hardware Recomendado:** GPU dedicada de gama media (ej. GTX 1660 / RTX 3050) para garantizar los criterios de éxito de rendimiento visual a 60+ FPS sostenidos.

---

## 🔧 Instrucciones de Instalación y Despliegue

## 🔧 Instrucciones de Instalación y Despliegue

### 1. Clonación del Repositorio
```bash
git clone [https://github.com/ImBoolean-2/proyecto_demo_u.git](https://github.com/ImBoolean-2/proyecto_demo_u.git)