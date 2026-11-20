# Plan de trabajo · Grupo 08

## Integrantes y partes

| Integrante | Rol | Qué hace | Archivos o carpeta propios |
| :--- | :--- | :--- | :--- |
| **Jesús David Ramírez** | Máquinas virtuales, red y Kubernetes | Aloja las dos VMs en su equipo con VirtualBox, instala Pop!_OS (`g08-grafica`) y AlmaLinux (`g08-consola`) con particionado manual, configura la red (NAT y solo-anfitrión), SSH e instantáneas `instalacion-limpia`; ejecuta en las VMs los scripts y despliega Minikube y Kubernetes. | `sprint-1.md`, `k8s/`, carpeta `capturas-vm/` |
| **Luis Fernando Dagua** | Seguridad, usuarios, procesos y Docker Engine | Instala paquetes base, configura los usuarios, el grupo `proyecto`, `/srv/proyecto`, permisos `sudo`, llave SSH y `firewalld` (puerto 8080); realiza las pruebas de procesos (`ps`, `top`, `kill`, `nice`, `renice`); instala Docker Engine, construye la imagen localmente y la publica en Docker Hub. | `sprint-2.md`, `docker/README-dockerhub.md`, carpeta `capturas-servicios/` |
| **Miguel Ángel Perdomo** | Coordinación, scripts, Dockerfile y sitio web | Crea el repositorio en GitHub, revisa que los commits y fechas cumplan, escribe y prueba en entorno cloud (Cloud Shell / Codespaces) los dos scripts Bash y el `Dockerfile` (Debian), arma el cuadro comparativo de instaladores, junta las páginas del sitio en GitHub Pages y entrega el enlace en el campus. | `README.md`, `index.html`, `plan/plan-de-trabajo.md`, `plan/ficha-version.md`, `scripts/`, `docker/Dockerfile`, `sprint-3.md` |

## Fechas de los sprints

| Sprint | Cierre (Santander) | Qué entregamos |
| :--- | :--- | :--- |
| **0 · Arranque** | jueves 19 de noviembre, 11:55 p.m. | Repositorio público con `plan/plan-de-trabajo.md` y `plan/ficha-version.md`. |
| **1 · Montaje** | jueves 26 de noviembre, 11:55 p.m. | Dos VMs, red, SSH e instantáneas. |
| **2 · Servicios** | jueves 10 de diciembre, 11:55 p.m. | Usuarios, firewall, scripts, procesos y Docker.) |
| **3 · Cierre** | jueves 17 de diciembre, 11:55 p.m. | Imagen en Docker Hub, Kubernetes y sitio completo. |
| **Sustentación** | viernes 18 / sábado 19 de diciembre | Presentación del grupo y prueba individual con VMs encendidas. |

## Reglas del grupo

* Cada integrante edita su propio archivo o carpeta. Si alguien necesita tocar el de otro, avisa al grupo antes de editarlo.
* Cada integrante hace al menos 2 commits por sprint (en los sprints 1, 2 y 3), con un mensaje que diga qué cambió (por ejemplo: `"agrego la partición /var a la ficha"`). Nada de `"update"` ni `"cambios".
* Los videos se graban el día antes del cierre por videollamada compartiendo pantalla, con las dos VMs encendidas y mostrando el rostro de los tres integrantes.
* Si alguien no puede cumplir su parte, lo dice al grupo con tiempo y se reparte.
