# Ficha de verificación de versión · Grupo 08


Distribuciones del grupo 08: **Pop!_OS** (gráfica), **AlmaLinux** (consola) y **Debian** (imagen base).

---

## 1. Pop!_OS (VM gráfica · `g08-grafica`)

| Pregunta | Respuesta | Enlace donde lo comprobamos |
| :--- | :--- | :--- |
| **Versión elegida y fecha de lanzamiento** | Pop!_OS 24.04 LTS (lanzada en diciembre de 2025) | https://pop.system76.com/ |
| **Hasta cuándo recibe actualizaciones de seguridad** | Al estar basada en Ubuntu 24.04 LTS, recibe actualizaciones estándar de seguridad por 5 años (hasta abril de 2029) | https://support.system76.com/ |
| **Requisitos de hardware y si funciona en VirtualBox** | Mínimo recomendado por System76: 4 GB de RAM, procesador de 64 bits (2 núcleos) y 20 GB de almacenamiento. Sí funciona en VirtualBox (64-bit Ubuntu/Debian) | https://support.system76.com/articles/install-pop/ |
| **¿El instalador permite particionado manual?** | Sí. El instalador propio de Pop!_OS (`distinst`) incluye la opción «Custom (Advanced)» para crear y asignar manualmente `/`, `swap` y `/home` | https://support.system76.com/articles/install-pop/ |
| **Guía oficial para instalar Docker Engine en esa familia** | Aunque Docker Engine se instalará en la VM de consola, Docker cuenta con guía oficial para la familia Ubuntu/Debian usando `apt` | https://docs.docker.com/engine/install/ubuntu/ |
| **Imagen base del Dockerfile para esa versión** | No aplica como imagen base del grupo (usamos Debian), pero existen imágenes base oficiales de Ubuntu/Debian en Docker Hub | https://hub.docker.com/_/ubuntu |

**Memoria RAM asignada a `g08-grafica`:** Le asignamos **4 GB de RAM (4096 MB)** porque cuenta con entorno de escritorio gráfico completo (COSMIC) y ejecutará simultáneamente dos navegadores web, dos editores de texto y el script gráfico requerido en el proyecto[span_2](start_span)[span_2](end_span)[span_3](start_span)[span_3](end_span).

---

## 2. AlmaLinux (VM de consola · `g08-consola`)

| Pregunta | Respuesta | Enlace donde lo comprobamos |
| :--- | :--- | :--- |
| **Versión elegida y fecha de lanzamiento** | AlmaLinux OS 10 (lanzada en mayo de 2025) | https://almalinux.org/get-almalinux/ |
| **Hasta cuándo recibe actualizaciones de seguridad** | AlmaLinux 10 tiene soporte activo hasta el 31 de mayo de 2030 y soporte de seguridad hasta el 31 de mayo de 2035 | https://wiki.almalinux.org/release-notes/ |
| **Requisitos de hardware y si funciona en VirtualBox** | Requisitos mínimos: 1.5 GB de RAM, 1 vCPU y 10 GB de disco. Sí funciona en VirtualBox; la configuramos con 2 GB de RAM (y 3 GB para Minikube en Sprint 3), 2 CPU y 25 GB de disco | https://wiki.almalinux.org/documentation/installation-guide.html |
| **¿El instalador permite particionado manual?** | Sí. El instalador Anaconda permite seleccionar almacenamiento «Personalizado» (`Custom`) para configurar `/`, `swap`, `/home` y `/var` | https://wiki.almalinux.org/documentation/installation-guide.html |
| **Guía oficial para instalar Docker Engine en esa familia** | Docker no tiene una página exclusiva para AlmaLinux; usamos la guía oficial de la familia RHEL/CentOS mediante el repositorio `dnf` | https://docs.docker.com/engine/install/rhel/ |
| **Imagen base del Dockerfile para esa versión** | Existe imagen oficial `almalinux` en Docker Hub, aunque nuestro Dockerfile usará Debian según la asignación del Grupo 08 | https://hub.docker.com/_/almalinux |

---

## 3. Debian (imagen base del Dockerfile)

| Pregunta | Respuesta | Enlace donde lo comprobamos |
| :--- | :--- | :--- |
| **Versión elegida y fecha de lanzamiento** | Debian 13 (`trixie`), versión estable lanzada en agosto de 2025 | https://www.debian.org/releases/trixie/ |
| **Hasta cuándo recibe actualizaciones de seguridad** | Debian 13 (`trixie`) recibe soporte oficial de seguridad por 3 años (hasta agosto de 2028) y soporte LTS extendido hasta junio de 2030 | https://wiki.debian.org/DebianReleases |
| **Requisitos de hardware y si funciona en VirtualBox** | Como contenedor Docker corre directamente sobre el kernel Linux de `g08-consola` dentro de VirtualBox sin requerir virtualización anidada adicional | https://hub.docker.com/_/debian |
| **¿El instalador permite particionado manual?** | No aplica para imágenes de contenedor (el sistema de archivos del contenedor se construye por capas mediante instrucciones `RUN` en el `Dockerfile`) | https://docs.docker.com/reference/dockerfile/ |
| **Guía oficial para instalar Docker Engine en esa familia** | Docker cuenta con documentación oficial para Debian (`apt`), y dentro del contenedor usaremos `apt-get` para instalar `git`, `curl`, editor y compilador | https://docs.docker.com/engine/install/debian/ |
| **Imagen base del Dockerfile para esa versión** | Sí existe la imagen oficial `debian` en Docker Hub con las etiquetas `trixie-slim` y `stable-slim`, usando el gestor de paquetes `apt` / `apt-get` | https://hub.docker.com/_/debian |
