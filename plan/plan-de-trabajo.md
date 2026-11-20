# Plan de trabajo · Grupo 08

## Integrantes y partes

| Integrante | Rol | Qué hace | Archivos o carpeta propios |
| :--- | :--- | :--- | :--- |
| **Jesús David Ramírez** | Máquinas virtuales, red y Kubernetes | Aloja las dos VMs en su equipo con VirtualBox, instala Pop!_OS (`g08-grafica`) y AlmaLinux (`g08-consola`) con particionado manual, configura la red (NAT y solo-anfitrión), SSH e instantáneas `instalacion-limpia`; ejecuta en las VMs los scripts y despliega Minikube y Kubernetes | `sprint-1.md`, `k8s/`, carpeta `capturas-vm/` |
| **Luis Fernando Dagua** | Seguridad, usuarios, procesos y Docker Engine | Instala paquetes base, configura los usuarios, el grupo `proyecto`, `/srv/proyecto`, permisos `sudo`, llave SSH y `firewalld` (puerto 8080); realiza las pruebas de procesos (`ps`, `top`, `kill`, `nice`, `renice`); instala Docker Engine, construye la imagen localmente y la publica en Docker Hub[span_20](start_span)[span_20](end_span)[span_21](start_span)[span_21](end_span)[span_22](start_span)[span_22](end_span)[span_23](start_span)[span_23](end_span) | `sprint-2.md`, `docker/README-dockerhub.md`, carpeta `capturas-servicios/` |
| **Miguel Ángel Perdomo** | Coordinación, scripts, Dockerfile y sitio web | Crea el repositorio en GitHub, revisa que los commits y fechas cumplan, escribe y prueba en entorno cloud (Cloud Shell / Codespaces) los dos scripts Bash y el `Dockerfile` (Debian), arma el cuadro comparativo de instaladores, junta las páginas del sitio en GitHub Pages y entrega el enlace en el campus[span_24](start_span)[span_24](end_span)[span_25](start_span)[span_25](end_span)[span_26](start_span)[span_26](end_span)[span_27](start_span)[span_27](end_span)[span_28](start_span)[span_28](end_span) | `README.md`, `index.html`, `plan/plan-de-trabajo.md`, `plan/ficha-version.md`, `scripts/`, `docker/Dockerfile`, `sprint-3.md` |

## Fechas de los sprints

| Sprint | Cierre (Santander) | Qué entregamos |
| :--- | :--- | :--- |
| **0 · Arranque** | jueves 19 de noviembre, 11:55 p. m.[span_29](start_span)[span_29](end_span) | Repositorio público con `plan/plan-de-trabajo.md` y `plan/ficha-version.md`[span_30](start_span)[span_30](end_span)[span_31](start_span)[span_31](end_span) |
| **1 · Montaje** | jueves 26 de noviembre, 11:55 p. m.[span_32](start_span)[span_32](end_span) | Dos VMs, red, SSH e instantáneas[span_33](start_span)[span_33](end_span)[span_34](start_span)[span_34](end_span) |
| **2 · Servicios** | jueves 10 de diciembre, 11:55 p. m.[span_35](start_span)[span_35](end_span) | Usuarios, firewall, scripts, procesos y Docker[span_36](start_span)[span_36](end_span)[span_37](start_span)[span_37](end_span) |
| **3 · Cierre** | jueves 17 de diciembre, 11:55 p. m.[span_38](start_span)[span_38](end_span) | Imagen en Docker Hub, Kubernetes y sitio completo[span_39](start_span)[span_39](end_span)[span_40](start_span)[span_40](end_span)[span_41](start_span)[span_41](end_span) |
| **Sustentación** | viernes 18 / sábado 19 de diciembre[span_42](start_span)[span_42](end_span)[span_43](start_span)[span_43](end_span) | Presentación del grupo y prueba individual con VMs encendidas[span_44](start_span)[span_44](end_span)[span_45](start_span)[span_45](end_span)[span_46](start_span)[span_46](end_span) |

## Reglas del grupo

* Cada integrante edita su propio archivo o carpeta[span_47](start_span)[span_47](end_span). Si alguien necesita tocar el de otro, avisa al grupo antes de editarlo[span_48](start_span)[span_48](end_span).
* Cada integrante hace al menos 2 commits por sprint (en los sprints 1, 2 y 3), con un mensaje que diga qué cambió (por ejemplo: `"agrego la partición /var a la ficha"`)[span_49](start_span)[span_49](end_span). Nada de `"update"` ni `"cambios"`[span_50](start_span)[span_50](end_span).
* Los videos se graban el día antes del cierre por videollamada compartiendo pantalla, con las dos VMs encendidas y mostrando el rostro de los tres integrantes[span_51](start_span)[span_51](end_span).
* Si alguien no puede cumplir su parte, lo dice al grupo con tiempo y se reparte.
