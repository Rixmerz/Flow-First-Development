# Roadmap MVP GeoAyuda · Flow-First Development  
**Stack:** React Native (Expo), Go (Golang), Supabase (Postgres), MongoDB Atlas, Railway, Fly.io

---

## 1. Mapeo de Flujos y Validación UX  
- [x] Interfaces completas en Figma.
- [x] Flujos validados:  
  - Registro/login (con foto biométrica)  
  - Creación de ladidos (alerta geolocalizada)  
  - Likes/verificación  
  - Gestión de perfil de usuario  

---

## 2. Implementación de Interfaces (Figma → React Native)  
**Meta:** Convertir el diseño validado en Figma a componentes React Native/Expo, siguiendo el flujo de usuario.

- [ ] Desglose de pantallas/componentes de Figma por flujo.  
- [ ] Setup de proyecto Expo con estructura modular.  
- [ ] Implementar navegación (React Navigation) y lógica de screens:  
    - [ ] Registro/Login (+ foto y validación Supabase Auth)  
    - [ ] Creación de ladidos (form, multimedia, geolocalización)  
    - [ ] Pantallas de like/verificación  
    - [ ] Perfil y privacidad  
- [ ] Componentización: inputs, botones, cards, modales, headers.  
- [ ] Pixel-perfect y validación UX vs Figma.  
- [ ] Testing visual y de navegación en dispositivos reales.

---

## 3. Setup Técnico Base  
**Meta:** Garantizar la infraestructura mínima viable y conexión stack.

- [ ] Inicializar backend Go (estructura REST, workers para verificación, auth, subida de archivos, integración con Supabase y Mongo).  
- [ ] Configurar Supabase:  
    - Auth (registro/login, JWT)  
    - Storage (fotos/videos ladidos y perfil)  
    - Realtime (likes/verificación y actualizaciones de mapa)  
- [ ] Configurar MongoDB Atlas:  
    - Analítica, tracking, reportes no verificados  
- [ ] CI/CD y despliegue en Railway (backend Go).  
- [ ] Documentación básica de endpoints y arquitectura.

---

## 4. Desarrollo por Flujos Verticales (Flow Slices)  
**Meta:** Entregar funcionalidades completas y usables flujo por flujo, maximizando feedback temprano.

### 4.1. Registro/Login  
- [ ] Frontend: formulario, captura foto, integración Supabase Auth/Storage  
- [ ] Backend: validación, registro, endpoints de usuario  
- [ ] E2E: registro, login, acceso perfil  

### 4.2. Creación de Ladidos  
- [ ] Frontend: formulario, multimedia, geolocalización (Expo APIs)  
- [ ] Backend: endpoints para crear, almacenar (Supabase Storage/Postgres), registro en Mongo  
- [ ] E2E: crear ladido, ver en feed/mapa  

### 4.3. Likes y Verificación  
- [ ] Frontend: UI de like, feedback de verificación  
- [ ] Backend: endpoint like, lógica de verificación (workers Go), notificaciones Realtime  
- [ ] E2E: interacción, ver estado verificado tras 3 likes  

### 4.4. Perfil de Usuario  
- [ ] Frontend: edición perfil, foto, privacidad  
- [ ] Backend: endpoints edición, visibilidad, storage  
- [ ] E2E: editar y visualizar perfil según privacidad

---

## 5. QA, Integración y Escalado  
**Meta:** Validar que todo el MVP sea usable, seguro y listo para escalar.

- [ ] Pruebas end-to-end completas  
- [ ] Corrección de bugs y mejoras UX  
- [ ] Seguridad (validaciones, protección de datos, roles básicos)  
- [ ] Migración backend Go a Fly.io para baja latencia LATAM si es necesario  
- [ ] Documentar arquitectura y procesos

---

## 6. Demo, Feedback y Deploy  
- [ ] Demo funcional para stakeholders/early adopters  
- [ ] Recoger feedback, iterar rápido  
- [ ] Deploy estable y checklist de cierre MVP

---

## Reglas de Flow-First Development  
- **Flujo vertical:** Cada funcionalidad se entrega de extremo a extremo (UI ↔ backend ↔ base de datos), usable y testeada.  
- **Feedback temprano:** Cada flujo se valida con usuarios reales o testers, priorizando iterar sobre lo que más impacto tiene.  
- **Documentación viva:** Todo el stack y flujos documentados para facilitar onboarding y escalar el equipo.  
- **Escalado progresivo:** MVP rápido en Railway, migración a Fly.io cuando la demanda lo justifique.

---

## Justificación de Stack y Metodología

- **React Native (Expo):** Iteración rápida, un solo código para iOS/Android, comunidades y librerías maduras.
- **Go:** Backend performante y concurrente, ideal para eventos geoespaciales y notificaciones.
- **Supabase:** Postgres gestionado, auth, storage y realtime sin devops extra.
- **MongoDB Atlas:** Analítica flexible y tracking sin esquema rígido.
- **Railway/Fly.io:** Despliegue ágil y escalado sin reescritura, latencia baja para usuarios LATAM.
- **Flow-First Development:** Entrega continua, máxima transparencia y validación progresiva.

---

**Este roadmap está alineado al MVP (geoayuda/GeoAyuda#3), al stack propuesto y a la metodología Flow-First Development.  
¿Quieres que el siguiente paso sea el desglose de la checklist de pantallas/componentes Figma → React Native por flujo?