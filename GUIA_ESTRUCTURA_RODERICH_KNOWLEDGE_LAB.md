# Guía de organización — Roderich Knowledge Lab

Este documento explica la estructura de carpetas recomendada para mi sistema personal de aprendizaje técnico, apuntes, laboratorios, proyectos, incidentes, runbooks, decisiones y portafolio.

La idea es que esta estructura me sirva no solo para el plan actual de Linux, DevOps, ciberseguridad, backend, cloud e IA aplicada, sino también para cualquier tema nuevo que quiera estudiar en el futuro.

---

# 1. Objetivo general

La estructura está diseñada para separar claramente cuatro cosas distintas:

- **Conocimiento:** lo que ya entiendo y quiero conservar como referencia permanente.
- **Aprendizaje:** lo que estoy estudiando actualmente.
- **Laboratorios:** lo que experimento o pruebo de forma práctica.
- **Proyectos:** lo que construyo como producto, práctica o evidencia de portafolio.

Alrededor de estas cuatro áreas también existen carpetas para:

- roadmaps;
- runbooks;
- incidentes;
- decisiones técnicas;
- recursos;
- cheatsheets;
- evidencias;
- plantillas;
- portafolio;
- notas sin clasificar;
- archivo histórico.

La estructura debe crecer de forma orgánica. No hace falta crear cientos de subcarpetas vacías desde el primer día.

---

# 2. Estructura principal

```text
Roderich-Knowledge-Lab/
│
├── 00_HOME/
├── 01_ROADMAPS/
├── 02_KNOWLEDGE/
├── 03_LEARNING/
├── 04_LABS/
├── 05_PROJECTS/
├── 06_RUNBOOKS/
├── 07_INCIDENTS/
├── 08_DECISIONS/
├── 09_RESOURCES/
├── 10_CHEATSHEETS/
├── 11_EVIDENCE/
├── 12_TEMPLATES/
├── 13_PORTFOLIO/
├── 90_INBOX/
└── 99_ARCHIVE/
```

---

# 3. Qué va en cada carpeta

## 00_HOME

Es el punto de entrada de todo el sistema.

Aquí no deben ir apuntes técnicos profundos. Deben ir documentos que expliquen cómo navegar la base de conocimiento y cuál es mi estado actual.

Estructura sugerida:

```text
00_HOME/
├── README.md
├── INDEX.md
├── CURRENT_STATUS.md
├── LEARNING_SYSTEM.md
└── KNOWLEDGE_MAP.md
```

### README.md

Explica:

- qué es este repositorio;
- para qué sirve;
- cómo está organizado;
- reglas generales de uso.

### INDEX.md

Índice general con enlaces a las áreas principales.

Ejemplo:

```text
Linux
Networking
Docker
Backend
Ciberseguridad
DevOps
Cloud
IA
```

### CURRENT_STATUS.md

Estado actual del aprendizaje.

Ejemplo:

```text
Actualmente estudiando:
- Linux Fundamental
- SSH Hardening

Próximo:
- Networking

Homelab:
- Ubuntu Server 26.04
- 192.168.100.50
- SSH configurado
```

No guardar aquí contraseñas, claves privadas, tokens ni secretos.

### LEARNING_SYSTEM.md

Explica cómo estudio:

```text
Roadmap
↓
Aprendizaje
↓
Laboratorios / Proyectos
↓
Conocimiento consolidado
↓
Runbooks / Incidentes / Decisiones
↓
Portafolio
```

### KNOWLEDGE_MAP.md

Mapa conceptual de las áreas de conocimiento.

Ejemplo:

```text
Linux
├── Filesystem
├── Processes
├── systemd
└── Security

Networking
├── TCP/IP
├── DNS
├── Routing
└── Firewalls
```

---

## 01_ROADMAPS

Aquí guardo los planes de estudio.

No es el lugar para apuntes detallados, sino para responder:

> ¿Qué quiero aprender y en qué orden?

Estructura sugerida:

```text
01_ROADMAPS/
├── active/
├── future/
└── completed/
```

### active

Roadmaps que estoy siguiendo actualmente.

Ejemplo:

```text
01_ROADMAPS/active/linux-devops-cybersecurity/
├── roadmap.md
├── progress.md
└── checklist.md
```

### future

Temas que quiero aprender en el futuro.

Ejemplo:

```text
future/
├── backend/
├── cybersecurity/
├── cloud/
├── artificial-intelligence/
└── rust/
```

### completed

Roadmaps terminados.

La idea es poder mover un tema:

```text
future/
↓
active/
↓
completed/
```

sin reorganizar el resto de la base de conocimiento.

---

## 02_KNOWLEDGE

Esta es la base de conocimiento permanente.

Aquí va lo que ya estudié, procesé, entendí y quiero conservar como referencia a largo plazo.

No representa el orden en que estudio. Representa el conocimiento por área.

Estructura sugerida:

```text
02_KNOWLEDGE/
├── computer-science/
├── operating-systems/
├── networking/
├── programming/
├── backend/
├── databases/
├── containers/
├── virtualization/
├── cybersecurity/
├── devops/
├── kubernetes/
├── cloud/
├── artificial-intelligence/
└── software-engineering/
```

Ejemplos de subestructura:

```text
operating-systems/
├── linux/
├── windows/
└── concepts/
```

```text
backend/
├── http/
├── rest/
├── authentication/
├── oauth/
└── distributed-systems/
```

```text
databases/
├── sql/
├── postgresql/
└── redis/
```

```text
artificial-intelligence/
├── fundamentals/
├── llm/
├── embeddings/
├── rag/
├── agents/
└── mlops/
```

### Ejemplo dentro de Linux

```text
02_KNOWLEDGE/operating-systems/linux/
├── README.md
├── fundamentals/
├── filesystem/
├── users-groups/
├── permissions/
├── processes/
├── packages/
├── systemd/
├── storage/
├── networking/
├── security/
└── troubleshooting/
```

Dentro de permisos:

```text
permissions/
├── README.md
├── rwx.md
├── chmod.md
├── chown.md
├── umask.md
├── acl.md
└── examples.md
```

Regla principal:

> Aquí va conocimiento consolidado, no notas crudas.

Si estoy estudiando algo y todavía no lo entiendo bien, primero va a `03_LEARNING`.

---

## 03_LEARNING

Aquí va mi proceso activo de aprendizaje.

Esta carpeta responde:

> ¿Qué estoy estudiando ahora?

Estructura:

```text
03_LEARNING/
├── active/
├── paused/
└── completed/
```

Para el plan actual:

```text
03_LEARNING/active/linux-professional/
├── 00-hardware/
├── 01-linux-fundamentals/
├── 02-linux-administration/
├── 03-networking/
├── 04-ssh-hardening/
├── 05-git/
├── 06-docker/
├── 07-backend-data/
├── 08-virtualization/
├── 09-cybersecurity/
├── 10-blue-team-observability/
├── 11-devops/
├── 12-kubernetes/
├── 13-cloud/
├── 14-ai-mlops/
└── 15-capstone/
```

Cada módulo puede tener:

```text
01-linux-fundamentals/
├── README.md
├── notes/
├── exercises/
├── questions/
├── mistakes/
└── checkpoint.md
```

Flujo recomendado:

```text
03_LEARNING/.../notes/
        ↓
refinar
        ↓
02_KNOWLEDGE/...
```

No copiar automáticamente todo lo estudiado a `KNOWLEDGE`.

Solo mover lo que realmente quedó entendido y organizado.

---

## 04_LABS

Aquí van experimentos y prácticas reproducibles.

Un laboratorio no es lo mismo que un apunte.

Debe contener:

- objetivo;
- entorno;
- hipótesis;
- comandos;
- resultado esperado;
- resultado real;
- errores;
- diagnóstico;
- solución;
- validación;
- rollback;
- lecciones aprendidas;
- evidencia.

Estructura sugerida:

```text
04_LABS/
├── linux/
├── networking/
├── docker/
├── databases/
├── virtualization/
├── cybersecurity/
├── devops/
├── kubernetes/
├── cloud/
└── ai/
```

Ejemplo:

```text
04_LABS/networking/
└── LAB-NET-003-dns-failure/
    ├── README.md
    ├── commands.md
    ├── results.md
    ├── troubleshooting.md
    ├── rollback.md
    └── evidence/
```

Regla:

> Si estoy probando algo para entender cómo funciona, probablemente va aquí.

---

## 05_PROJECTS

Aquí van cosas que construyo.

Los proyectos no deben mezclarse con notas.

Estructura:

```text
05_PROJECTS/
├── learning/
├── experiments/
├── portfolio/
└── completed/
```

### learning

Proyectos pequeños creados para aprender.

Ejemplos:

```text
linux-systemd-service/
docker-api-postgres/
kvm-lab/
```

### experiments

Ideas rápidas o pruebas de concepto.

### portfolio

Proyectos que quiero convertir en evidencia profesional.

Ejemplos:

```text
homelab-infrastructure/
production-api-lab/
cyber-lab/
observability-lab/
devops-pipeline/
rag-app/
```

### completed

Proyectos terminados que ya no están activos.

Regla importante:

> Los proyectos grandes deberían convertirse en repositorios Git independientes.

El Knowledge Lab puede contener documentación y enlaces, pero no necesariamente todo el código del proyecto.

---

## 06_RUNBOOKS

Aquí van procedimientos operativos.

Un apunte explica cómo funciona algo.

Un runbook explica qué hacer cuando necesito operar o recuperar algo.

Ejemplos:

```text
06_RUNBOOKS/
├── server/
├── networking/
├── docker/
├── databases/
├── backups/
├── security/
└── disaster-recovery/
```

Archivos ejemplo:

```text
restore-postgresql.md
recover-ssh-access.md
disk-full.md
docker-service-down.md
restore-homelab.md
replace-failed-disk.md
```

Ejemplo de diferencia:

```text
KNOWLEDGE:
¿Cómo funciona PostgreSQL?

RUNBOOK:
PostgreSQL no inicia. ¿Qué hago?
```

---

## 07_INCIDENTS

Aquí se documentan fallos reales.

Los errores no se borran: se convierten en conocimiento.

Estructura:

```text
07_INCIDENTS/
├── linux/
├── networking/
├── docker/
├── security/
├── databases/
└── hardware/
```

Ejemplos:

```text
INC-2026-001-ssh-lockout.md
INC-2026-002-docker-volume-permissions.md
INC-2026-003-dns-resolution.md
```

Cada incidente debería registrar:

- resumen;
- impacto;
- timeline;
- causa raíz;
- factores contribuyentes;
- qué funcionó;
- qué no funcionó;
- solución;
- acciones correctivas;
- acciones preventivas;
- cómo validar que no se repite.

---

## 08_DECISIONS

Aquí documento decisiones técnicas importantes usando ADR.

ADR significa:

> Architecture Decision Record

Sirve para responder:

> ¿Por qué elegí esta solución y no otra?

Ejemplos:

```text
08_DECISIONS/
├── ADR-001-ubuntu-server-as-host.md
├── ADR-002-use-lvm.md
├── ADR-003-dhcp-reservation.md
├── ADR-004-ssh-key-authentication.md
└── ADR-005-docker-before-kubernetes.md
```

Plantilla:

```text
# ADR-XXX — Título

Estado:
Aceptado / Propuesto / Reemplazado

Contexto:
...

Opciones:
1. ...
2. ...
3. ...

Decisión:
...

Razón:
...

Consecuencias:
...
```

Esta carpeta es importante porque desarrolla capacidad de justificar decisiones técnicas, no solo ejecutar comandos.

---

## 09_RESOURCES

Aquí van fuentes externas.

Ejemplos:

```text
09_RESOURCES/
├── books/
├── courses/
├── documentation/
├── papers/
├── videos/
└── websites/
```

Es mejor guardar índices o referencias que descargar todo indiscriminadamente.

Ejemplo de archivo:

```text
linux-resources.md
docker-resources.md
networking-courses.md
```

Cada recurso puede incluir:

```text
Nombre:
URL:
Autor:
Nivel:
Tema:
Por qué vale la pena:
Estado:
```

Estados sugeridos:

```text
Pendiente
En curso
Completado
Referencia
Descartado
```

---

## 10_CHEATSHEETS

Aquí van referencias rápidas.

Responde:

> Ya entiendo esto, solo olvidé la sintaxis.

Ejemplos:

```text
10_CHEATSHEETS/
├── linux.md
├── git.md
├── ssh.md
├── networking.md
├── docker.md
├── postgresql.md
├── kubernetes.md
└── vim.md
```

Diferencia:

```text
KNOWLEDGE
→ entender profundamente

CHEATSHEET
→ recordar rápidamente
```

---

## 11_EVIDENCE

Aquí se guardan evidencias pequeñas de aprendizaje y laboratorio.

Estructura:

```text
11_EVIDENCE/
├── screenshots/
├── logs/
├── terminal/
├── diagrams/
├── pcaps/
└── reports/
```

Regla importante:

> Git no debe convertirse en almacenamiento masivo.

No subir:

- ISO;
- backups;
- dumps grandes;
- imágenes de VM;
- PCAP enormes;
- datasets pesados.

Para esos archivos usar `/srv/storage`.

---

## 12_TEMPLATES

Aquí van plantillas reutilizables.

Estructura sugerida:

```text
12_TEMPLATES/
├── note.md
├── concept.md
├── lab.md
├── project.md
├── incident.md
├── postmortem.md
├── runbook.md
├── adr.md
├── cheatsheet.md
├── weekly-review.md
└── monthly-review.md
```

La idea es no empezar cada documento desde cero.

---

## 13_PORTFOLIO

Aquí se selecciona lo mejor de lo aprendido.

No se copia todo.

Solo lo que merece mostrarse profesionalmente.

Estructura:

```text
13_PORTFOLIO/
├── projects/
├── case-studies/
├── diagrams/
├── reports/
├── demos/
└── README.md
```

Ejemplo:

```text
case-studies/
└── ubuntu-homelab/
    ├── problem.md
    ├── architecture.md
    ├── implementation.md
    ├── security.md
    ├── lessons-learned.md
    └── results.md
```

Esto puede reutilizarse después en:

- GitHub;
- LinkedIn;
- CV;
- portfolio web;
- entrevistas;
- demostraciones técnicas.

---

## 90_INBOX

Esta carpeta es para capturar cosas rápidamente.

Si encuentro un concepto nuevo y no sé dónde colocarlo todavía:

```text
90_INBOX/ebpf.md
```

Después, durante una revisión semanal, decido dónde pertenece.

Ejemplo:

```text
90_INBOX/ebpf.md
        ↓
02_KNOWLEDGE/operating-systems/linux/ebpf/
```

Regla:

> La organización nunca debe interrumpir el aprendizaje.

Primero capturo. Después clasifico.

---

## 99_ARCHIVE

Aquí va contenido antiguo que ya no debe formar parte del sistema activo.

Estructura sugerida:

```text
99_ARCHIVE/
├── completed-learning/
├── deprecated/
├── old-notes/
└── abandoned-projects/
```

No eliminar algo útil solo porque ya no está vigente.

Pero tampoco dejar material obsoleto mezclado con documentación actual.

---

# 4. Diferencias importantes entre carpetas

## LEARNING vs KNOWLEDGE

```text
LEARNING
→ estoy aprendiendo

KNOWLEDGE
→ ya lo entendí y quiero conservarlo
```

## KNOWLEDGE vs CHEATSHEET

```text
KNOWLEDGE
→ explicación profunda

CHEATSHEET
→ referencia rápida
```

## LAB vs PROJECT

```text
LAB
→ experimentar y aprender

PROJECT
→ construir algo
```

## INCIDENT vs LAB

```text
LAB
→ experimento controlado

INCIDENT
→ algo falló de verdad
```

## KNOWLEDGE vs RUNBOOK

```text
KNOWLEDGE
→ cómo funciona

RUNBOOK
→ cómo operar o recuperar
```

## PROJECT vs PORTFOLIO

```text
PROJECT
→ trabajo completo

PORTFOLIO
→ selección presentable del trabajo
```

---

# 5. Flujo recomendado de aprendizaje

El flujo general debe ser:

```text
ROADMAP
   ↓
LEARNING
   ↓
LABS / PROJECTS
   ↓
¿Qué aprendí?
   ↓
KNOWLEDGE
   ↓
RUNBOOKS / INCIDENTS / DECISIONS
   ↓
PORTFOLIO
```

Ejemplo real:

```text
Quiero aprender Docker
        ↓
01_ROADMAPS
        ↓
03_LEARNING/docker
        ↓
04_LABS/docker
        ↓
05_PROJECTS/docker-api-postgres
        ↓
02_KNOWLEDGE/containers/docker
        ↓
06_RUNBOOKS/docker
        ↓
13_PORTFOLIO
```

---

# 6. Regla para nuevos temas futuros

Si mañana quiero estudiar algo que hoy no existe en la estructura, por ejemplo:

```text
Rust
eBPF
Blockchain
Data Engineering
Machine Learning
Embedded Systems
Go
SRE
FinOps
```

no debo rehacer la estructura.

Solo hago:

```text
01_ROADMAPS/future/rust/
```

cuando quiera estudiarlo:

```text
03_LEARNING/active/rust/
```

cuando consolide conocimiento:

```text
02_KNOWLEDGE/programming/rust/
```

si hago laboratorios:

```text
04_LABS/rust/
```

si creo proyectos:

```text
05_PROJECTS/learning/rust-...
```

La estructura está diseñada para crecer sin reorganizar todo.

---

# 7. No crear todas las carpetas posibles desde el inicio

No hacer esto:

```text
knowledge/
├── aws/
├── azure/
├── rust/
├── go/
├── blockchain/
├── ml/
├── data-engineering/
└── ...
```

si están vacías.

Regla:

> Crear una subcarpeta cuando realmente exista contenido para ella.

La estructura debe crecer de forma orgánica.

---

# 8. Separación entre conocimiento y almacenamiento operativo

La base de conocimiento no debe mezclarse con datos reales del servidor.

## Base de conocimiento

```text
/home/roderich/knowledge-lab/
```

Aquí:

- Markdown;
- documentación;
- scripts pequeños;
- índices;
- plantillas;
- evidencias pequeñas;
- Git.

## SSD rápido

```text
/srv/fastdata/
├── containers/
├── databases/
├── vm-fast/
└── project-runtime/
```

Aquí:

- datos de servicios;
- bases de datos;
- Docker volumes;
- VMs rápidas;
- runtime de proyectos.

## HDD grande

```text
/srv/storage/
├── backups/
├── iso/
├── datasets/
├── vm-images/
├── archives/
└── large-evidence/
```

Aquí:

- backups;
- imágenes ISO;
- datasets;
- VMs grandes;
- dumps;
- archivos pesados;
- evidencias grandes.

---

# 9. Seguridad del repositorio

Nunca guardar en Git:

```text
contraseñas
tokens
API keys
SSH private keys
secrets
credentials
.env reales
certificados privados
datos personales sensibles
```

Usar `.gitignore` cuando corresponda.

Ejemplos:

```gitignore
.env
*.key
*.pem
secrets/
credentials/
private/
*.log
*.pcap
*.iso
*.img
*.qcow2
*.dump
```

Ajustar según el proyecto.

---

# 10. Convenciones de nombres recomendadas

Usar nombres consistentes.

## Laboratorios

```text
LAB-LINUX-001
LAB-NET-001
LAB-DOCKER-001
LAB-SEC-001
```

## Incidentes

```text
INC-2026-001
INC-2026-002
```

## ADR

```text
ADR-001
ADR-002
ADR-003
```

## Runbooks

Preferir nombres por acción:

```text
recover-ssh-access.md
restore-postgresql.md
rotate-logs.md
replace-failed-disk.md
```

## Notas

Preferir nombres claros:

```text
linux-permissions.md
tcp-three-way-handshake.md
docker-volumes.md
oauth-authorization-code-flow.md
```

Evitar:

```text
nota1.md
nuevo.md
cosas.md
prueba.md
```

---

# 11. Regla de oro para decidir dónde guardar algo

Preguntarme:

### ¿Estoy aprendiendo esto ahora?

```text
03_LEARNING
```

### ¿Ya lo entiendo y quiero conservarlo?

```text
02_KNOWLEDGE
```

### ¿Estoy haciendo una práctica controlada?

```text
04_LABS
```

### ¿Estoy construyendo algo?

```text
05_PROJECTS
```

### ¿Necesito instrucciones para operar o recuperar algo?

```text
06_RUNBOOKS
```

### ¿Algo falló realmente?

```text
07_INCIDENTS
```

### ¿Tomé una decisión técnica importante?

```text
08_DECISIONS
```

### ¿Es una fuente externa?

```text
09_RESOURCES
```

### ¿Solo necesito recordar sintaxis rápidamente?

```text
10_CHEATSHEETS
```

### ¿Es una captura, log o evidencia?

```text
11_EVIDENCE
```

### ¿Quiero reutilizar el formato?

```text
12_TEMPLATES
```

### ¿Quiero mostrarlo profesionalmente?

```text
13_PORTFOLIO
```

### ¿No sé todavía dónde va?

```text
90_INBOX
```

### ¿Ya está obsoleto o fuera de uso?

```text
99_ARCHIVE
```

---

# 12. Resumen visual final

```text
Roderich-Knowledge-Lab/
│
├── 00_HOME/          → navegación y estado general
├── 01_ROADMAPS/      → qué quiero aprender
├── 02_KNOWLEDGE/     → conocimiento consolidado
├── 03_LEARNING/      → aprendizaje en curso
├── 04_LABS/          → experimentos reproducibles
├── 05_PROJECTS/      → cosas que construyo
├── 06_RUNBOOKS/      → operación y recuperación
├── 07_INCIDENTS/     → errores reales y postmortems
├── 08_DECISIONS/     → decisiones técnicas / ADR
├── 09_RESOURCES/     → fuentes externas
├── 10_CHEATSHEETS/   → referencia rápida
├── 11_EVIDENCE/      → capturas, logs y evidencias
├── 12_TEMPLATES/     → formatos reutilizables
├── 13_PORTFOLIO/     → selección profesional
├── 90_INBOX/         → captura rápida sin clasificar
└── 99_ARCHIVE/       → material histórico
```

---

# 13. Principio final

Este sistema no debe convertirse en una colección de archivos.

Debe convertirse en un ciclo continuo:

```text
Aprendo
↓
Practico
↓
Fallo
↓
Diagnostico
↓
Documento
↓
Consolido
↓
Construyo
↓
Demuestro
```

El objetivo final no es tener muchos apuntes.

El objetivo es construir una base de conocimiento técnica personal que me permita:

- recordar;
- aprender más rápido;
- diagnosticar problemas;
- reutilizar soluciones;
- justificar decisiones;
- operar sistemas;
- documentar proyectos;
- crear portafolio;
- enseñar lo aprendido;
- seguir creciendo durante años sin perder organización.
