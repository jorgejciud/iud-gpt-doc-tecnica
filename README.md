# Documentación Técnica Completa para Entrega Formal
## Proyecto: Asistente Virtual IUD GPT

**Equipo Investigador:**
- Boris Alberto Salleg Royero (Coinvestigador)
- Jorge Armando Julio Cruz (Coinvestigador)

**Fecha de Entrega:** Enero 2026

---

## ANEXO A: Pruebas Funcionales y Criterios de Aceptación

### 1. Marco de Pruebas Realizadas

Las pruebas funcionales del sistema IUD GPT se ejecutaron en dos fases durante el período de desarrollo (2024-2025), siguiendo una metodología de pruebas iterativas con usuarios reales en ambiente de pruebas de Canvas LMS.

### 2. Criterios de Aceptación Definidos

**Criterio General:** El sistema debe estar operativo y funcional en ambiente de pruebas Canvas LMS, cumpliendo con los siguientes requisitos técnicos y funcionales.

#### 2.1 Criterios de Integración con Canvas LMS

| ID | Criterio | Estado | Proceso realizado |
|----|----------|--------|-----------|
| CA-INT-001 | Autenticación SSO mediante Canvas exitosa | ✓ Aprobado | Integración LTI 1.3 validada |
| CA-INT-002 | Renderización correcta en iframe de Canvas | ✓ Aprobado | Probado en Chrome, Edge |
| CA-INT-003 | Persistencia de sesión durante navegación | ✓ Aprobado | Sesiones mantenidas por 2 horas |
| CA-INT-004 | Acceso contextual a datos del curso | ✓ Aprobado | API Canvas integrada correctamente |

#### 2.2 Criterios Funcionales del Asistente

| ID | Criterio | Estado | Método de Verificación |
|----|----------|--------|------------------------|
| CA-FUN-001 | Respuesta a consultas en lenguaje natural | ✓ Aprobado | 150+ consultas de prueba procesadas |
| CA-FUN-002 | Tiempo de respuesta < 3 segundos | ✓ Aprobado | Promedio 2.1 segundos medido |
| CA-FUN-003 | Precisión de respuestas > 80% | ✓ Aprobado | 85% de satisfacción en encuestas |
| CA-FUN-004 | Preguntas frecuentes accesibles | ✓ Aprobado | Panel lateral funcional |
| CA-FUN-006 | Manejo de consultas simultáneas | ✓ Aprobado | Hasta 40 usuarios concurrentes |

#### 2.3 Criterios de Seguridad y Privacidad

| ID | Criterio | Estado | Implementación |
|----|----------|--------|----------------|
| CA-SEG-001 | Validación de tokens LTI | ✓ Aprobado | Middleware de autenticación activo |
| CA-SEG-002 | No persistencia de datos sensibles | ✓ Aprobado | Sin almacenamiento de credenciales |
| CA-SEG-003 | Cumplimiento políticas institucionales | ✓ Aprobado | Aval Dirección Tecnología |

#### 2.4 Criterios de Usabilidad

| ID | Criterio | Estado | Resultado Encuesta |
|----|----------|--------|--------------------|
| CA-USA-001 | Interfaz intuitiva para estudiantes | ✓ Aprobado | 4.2/5.0 en encuesta |
| CA-USA-002 | Navegación sin capacitación previa | ✓ Aprobado | 90% usó sin ayuda |
| CA-USA-003 | Accesibilidad web (contraste, fuentes) | ✓ Aprobado | Ajustado post-feedback |

### 3. Casos de Prueba Ejecutados

#### 3.1 Pruebas de Integración LTI

**CP-INT-001: Autenticación desde Canvas**
- **Objetivo:** Verificar que estudiantes puedan acceder sin login adicional
- **Pasos ejecutados:**
  1. Usuario inicia sesión en Canvas
  2. Navega a curso con IUD GPT habilitado
  3. Clic en módulos
  4. Ir a sección de recursos
  5. Hace clic en IUD GPT II
  6. Sistema abre interfaz chat sin solicitar credenciales
- **Resultado:** ✓ APROBADO - 100% de intentos exitosos (n=45 usuarios)
- **Fecha ejecución:** Septiembre 2024


#### 3.2 Pruebas Funcionales del Asistente

**CP-FUN-001: Consultas Frecuentes Predefinidas**
- **Objetivo:** Verificar respuestas a preguntas frecuentes
- **Preguntas probadas:**
  - "¿Cuál es el contenido del curso?" ✓
  - "¿Cuáles son los objetivos de aprendizaje?" ✓
  - "¿Cómo se evalúa este curso?" ✓
  - "¿Cuándo debo entregar los trabajos?" ✓
  - "¿Dónde encuentro el material de estudio?" ✓
  - "¿Cómo contacto a mi profesor?" ✓
- **Resultado:** ✓ APROBADO - Todas respondidas correctamente
- **Fecha ejecución:** Septiembre-Octubre 2024

**CP-FUN-002: Procesamiento Lenguaje Natural**
- **Objetivo:** Validar respuestas a consultas abiertas
- **Consultas de prueba:** 150+ consultas variadas de estudiantes
- **Tasa de éxito:** 85% de respuestas consideradas útiles
- **Resultado:** ✓ APROBADO
- **Fecha ejecución:** Octubre-Noviembre 2024


**CP-PERF-002: Carga Concurrente**
- **Objetivo:** Evaluar estabilidad con múltiples usuarios
- **Escenario:** 50 usuarios simultáneos
- **Resultado:** Sistema estable, sin degradación significativa
- **Criterio aceptación:** Soportar 30+ usuarios concurrentes
- **Resultado:** ✓ APROBADO
- **Fecha ejecución:** Noviembre 2024

#### 3.4 Pruebas de Usabilidad con Usuarios Reales

**Fase 1 - Versión Inicial (Diseño Rojo)**
- **Participantes:** 15 estudiantes, 3 docentes
- **Fecha:** Septiembre 2024
- **Metodología:** Observación de uso + encuesta post-interacción
- **Hallazgos principales:**
  - Interfaz funcional pero colores distractivos
  - Necesidad de mejor contraste para accesibilidad
  - Solicitud de reorganización de preguntas frecuentes
- **Resultado:** Retroalimentación incorporada en Fase 2

**Fase 2 - Versión Mejorada (Diseño Neutro)**
- **Participantes:** 25 estudiantes, 5 docentes
- **Fecha:** Octubre-Noviembre 2024
- **Mejoras implementadas:**
  - Paleta de colores neutral (azul/gris/blanco)
  - Mejor contraste en elementos de texto
  - Reorganización de preguntas frecuentes
  - Optimización de espaciado y tipografía
- **Resultados cuantitativos:**
  - Satisfacción general: 4.2/5.0
  - Facilidad de uso: 4.5/5.0
  - Utilidad de respuestas: 4.0/5.0
  - Diseño visual: 4.3/5.0
- **Resultado:** ✓ APROBADO para implementación

### 4. Registro de Defectos y Resolución

| ID Defecto | Severidad | Descripción | Estado | Resolución |
|------------|-----------|-------------|--------|------------|
| DEF-001 | Media | Colores rojos causan distracción | Resuelto | Rediseño visual Fase 2 |
| DEF-002 | Baja | Preguntas frecuentes desorganizadas | Resuelto | Reorganización por prioridad |
| DEF-003 | Media | Contraste insuficiente en texto | Resuelto | Ajuste de paleta de colores |
| DEF-004 | Alta | Sesión expira en navegación entre páginas | Resuelto | Ajuste configuración LTI |

**Nota:** Todos los defectos identificados durante las pruebas fueron resueltos antes de la entrega del sistema.


### 5. Conclusión de Pruebas

El sistema IUD GPT cumple con todos los criterios de aceptación definidos y ha sido validado exitosamente en ambiente de pruebas con usuarios reales. Las pruebas demuestran que el sistema es:

- **Funcional:** Todas las características principales operan correctamente
- **Integrado:** Integración LTI con Canvas es robusta y estable
- **Usable:** Interfaz intuitiva con alta satisfacción de usuarios
- **Seguro:** Cumple con políticas institucionales

El sistema está listo para transición a ambiente productivo bajo gestión de la Dirección de Tecnología.

---

## ANEXO B: Manuales de Usuario

### Manual de Usuario - Estudiantes

#### Acceso al Asistente Virtual IUD GPT

**Paso 1: Ingresar al Curso en Canvas**
- Inicie sesión en Canvas LMS con sus credenciales institucionales
- Navegue al curso donde está habilitado IUD GPT

**Paso 2: Abrir el Asistente**
- En el menú lateral del curso, haga clic en Asistente del Curso o IUD GPT
- El asistente se abrirá automáticamente sin requerir login adicional

**Paso 3: Realizar Consultas**

*Opción A - Preguntas Frecuentes:*
- Use el panel lateral izquierdo
- Haga clic en cualquier pregunta predefinida
- El asistente responderá automáticamente

*Opción B - Consulta Personalizada:*
- Escriba su pregunta en el campo de texto inferior
- Presione Enter o haga clic en el botón de enviar
- Espere la respuesta del asistente (generalmente < 3 segundos)

**Categorías de Consultas Disponibles:**
- Contenido del curso
- Fechas de entrega
- Métodos de evaluación
- Material de estudio
- Contacto con profesor

**Buenas Prácticas:**
- Sea específico en sus consultas
- Use lenguaje natural (escriba como hablaría)
- Si la respuesta no es clara, reformule su pregunta
- Su historial de conversación se guarda automáticamente

---

### Manual de Usuario - Docentes

#### Configuración del Asistente en Canvas

**Activación en el Curso:**
1. Ingrese a su curso en Canvas como instructor
2. Vaya a "Configuración" > "Aplicaciones"
3. Localice "IUD GPT" en aplicaciones externas
4. Active la aplicación para su curso

**Personalización de Respuestas (Opcional):**
1. Acceda a la interfaz administrativa de IUD GPT
2. Agregue información específica de su curso
3. Personalice preguntas frecuentes según necesidades

**Monitoreo de Uso:**
- Revise estadísticas de consultas frecuentes
- Identifique temas que requieren mayor clarificación
- Ajuste contenido del curso según patrones identificados

---

### Manual de Usuario - Administradores

#### Gestión del Sistema IUD GPT

**Requisitos Previos:**
- Acceso administrativo a Canvas LMS
- Credenciales de administrador de IUD GPT
- Acceso a consola AWS (para gestión de costos)

**Configuración Inicial:**
1. Instalar aplicación LTI en Canvas (ver Manual de Instalación)
2. Configurar variables de entorno en servidor
3. Verificar conectividad con AWS Bedrock
4. Habilitar cursos autorizados

**Monitoreo del Sistema:**
- **Uso de tokens AWS:** Revisar semanalmente en consola AWS
- **Disponibilidad:** Monitorear health checks en Render/servidor
- **Logs de error:** Revisar diariamente logs de aplicación
- **Estadísticas de uso:** Dashboard administrativo

**Mantenimiento:**
- **Actualizaciones:** Coordinar con equipo investigador
- **Respaldos:** Base de datos MongoDB respaldada semanalmente
- **Escalamiento:** Ajustar recursos según demanda

---

## ANEXO C: Manual de Instalación y Despliegue

### Requisitos del Sistema

**Servidor de Aplicación:**
- Node.js v16.x o superior
- Memoria RAM: mínimo 2GB
- Almacenamiento: 10GB disponibles
- Sistema operativo: Linux (Ubuntu 20.04+ recomendado) o compatible

**Servicios Externos Requeridos:**
- Cuenta AWS con acceso a Bedrock
- Instancia MongoDB (local o Atlas)
- Canvas LMS con permisos de administrador
- Servidor con capacidad de exponer puerto HTTPS (443)

### Procedimiento de Instalación

#### 1. Preparación del Entorno

```bash
# Instalar Node.js (si no está instalado)
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt-get install -y nodejs

# Verificar instalación
node --version  # Debe mostrar v16.x o superior
npm --version
```

#### 2. Clonar Repositorios

**Frontend:**
```bash
git clone https://gitlab.iudigital.edu.co/ds-iudigital/iud-gpt/iud-gpt-front-end-nodejs.git
cd iud-gpt-front-end-nodejs
npm install
```

**Backend:**
```bash
git clone https://gitlab.iudigital.edu.co/ds-iudigital/iud-gpt/iud-gpt-backend.git
cd iud-gpt-backend
npm install
```

#### 3. Configuración de Variables de Entorno

**Backend (.env):**
```
# MongoDB
MONGODB_URI=mongodb://localhost:27017/iudgpt
# o para MongoDB Atlas:
# MONGODB_URI=mongodb+srv://usuario:password@cluster.mongodb.net/iudgpt

# AWS Bedrock
AWS_REGION=us-east-1
AWS_ACCESS_KEY_ID=<tu_access_key>
AWS_SECRET_ACCESS_KEY=<tu_secret_key>
BEDROCK_MODEL_ID=anthropic.claude-haiku-v1

# Canvas LTI
LTI_KEY=<lti_consumer_key_generado>
LTI_SECRET=<lti_consumer_secret_generado>
CANVAS_API_URL=https://canvas.iudigital.edu.co/api/v1

# Aplicación
PORT=3000
NODE_ENV=production
SESSION_SECRET=<generar_string_aleatorio_seguro>
FRONTEND_URL=https://tu-dominio-frontend.com
```

**Frontend (.env):**
```
REACT_APP_BACKEND_URL=https://tu-dominio-backend.com
REACT_APP_CANVAS_URL=https://canvas.iudigital.edu.co
```

#### 4. Configuración de Base de Datos

```bash
# Iniciar MongoDB (si es local)
sudo systemctl start mongod
sudo systemctl enable mongod

# Crear base de datos y colecciones iniciales
mongo
> use iudgpt
> db.createCollection("conversations")
> db.createCollection("courses")
> db.createCollection("users")
> exit
```

#### 5. Construcción y Despliegue

**Backend:**
```bash
cd iud-gpt-backend
npm run build  # Si aplica
npm start  # Para producción
# o usar PM2 para gestión de procesos:
npm install -g pm2
pm2 start server.js --name iudgpt-backend
pm2 save
pm2 startup
```

**Frontend:**
```bash
cd iud-gpt-front-end-nodejs
npm run build
npm start
# o con PM2:
pm2 start npm --name iudgpt-frontend -- start
pm2 save
```

#### 6. Configuración de Proxy Inverso (Nginx)

```nginx
# /etc/nginx/sites-available/iudgpt

# Backend
server {
    listen 443 ssl;
    server_name api-iudgpt.iudigital.edu.co;

    ssl_certificate /path/to/certificate.crt;
    ssl_certificate_key /path/to/private.key;

    location / {
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }
}

# Frontend
server {
    listen 443 ssl;
    server_name iudgpt.iudigital.edu.co;

    ssl_certificate /path/to/certificate.crt;
    ssl_certificate_key /path/to/private.key;

    location / {
        proxy_pass http://localhost:3001;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}
```

```bash
# Activar configuración
sudo ln -s /etc/nginx/sites-available/iudgpt /etc/nginx/sites-enabled/
sudo nginx -t
sudo systemctl reload nginx
```

#### 7. Configuración LTI en Canvas

**Paso 1: Generar Credenciales LTI**
- Consumer Key: (generar string alfanumérico único)
- Consumer Secret: (generar string aleatorio seguro, 32+ caracteres)

**Paso 2: Configurar en Canvas**
1. Ir a "Admin" > "Configuración" > "Aplicaciones"
2. Clic en "+ App"
3. Tipo de configuración: "Por URL" o "Manual"
4. Completar campos:
   - **Consumer Key:** (del paso 1)
   - **Consumer Secret:** (del paso 1)
   - **Launch URL:** https://iudgpt.iudigital.edu.co/lti/launch
   - **Domain:** iudgpt.iudigital.edu.co
   - **Privacidad:** "Public" (para acceso a nombre y email)
5. Guardar configuración

**Paso 3: Habilitar en Cursos**
1. Ir al curso deseado
2. "Configuración" > "Navegación"
3. Arrastrar "IUD GPT" desde herramientas ocultas a visibles
4. Guardar

### Verificación de Instalación

**Checklist post-instalación:**
- [ ] Backend responde en `https://api-iudgpt.iudigital.edu.co/health`
- [ ] Frontend accesible en `https://iudgpt.iudigital.edu.co`
- [ ] MongoDB conectado (verificar logs)
- [ ] AWS Bedrock responde (hacer prueba de consulta)
- [ ] LTI Canvas funciona (probar desde un curso)
- [ ] SSL certificados válidos
- [ ] Logs funcionando correctamente
- [ ] PM2 procesos corriendo

---

## ANEXO D: Documentación de API

### Endpoints Principales del Backend

#### Autenticación LTI

**POST /lti/launch**
```
Descripción: Endpoint de lanzamiento LTI desde Canvas
Content-Type: application/x-www-form-urlencoded

Parámetros:
- oauth_consumer_key (string): LTI consumer key
- oauth_signature (string): Firma OAuth
- user_id (string): ID de usuario Canvas
- context_id (string): ID del curso Canvas
- [otros parámetros estándar LTI 1.3]

Respuesta exitosa (200):
{
  "session_token": "jwt_token_aqui",
  "user": {
    "id": "12345",
    "name": "Juan Pérez",
    "role": "student"
  },
  "course": {
    "id": "67890",
    "name": "Programación Web I"
  }
}

Errores:
- 401: Credenciales LTI inválidas
- 400: Parámetros faltantes
```

#### Gestión de Conversaciones

**POST /api/conversations**
```
Descripción: Crear nueva conversación o enviar mensaje
Authorization: Bearer <session_token>
Content-Type: application/json

Body:
{
  "user_id": "12345",
  "course_id": "67890",
  "message": "¿Cuáles son las fechas de entrega?"
}

Respuesta exitosa (200):
{
  "conversation_id": "conv_abc123",
  "response": {
    "text": "Las fechas de entrega para este curso son...",
    "timestamp": "2024-11-15T10:30:00Z",
    "source": "ai" // o "faq"
  },
  "tokens_used": 150
}

Errores:
- 401: Token de sesión inválido
- 400: Mensaje vacío
- 500: Error al procesar con AWS Bedrock
```

**GET /api/conversations/:conversation_id**
```
Descripción: Obtener historial de conversación
Authorization: Bearer <session_token>

Respuesta exitosa (200):
{
  "conversation_id": "conv_abc123",
  "messages": [
    {
      "role": "user",
      "content": "Hola",
      "timestamp": "2024-11-15T10:25:00Z"
    },
    {
      "role": "assistant",
      "content": "Hola, ¿en qué puedo ayudarte?",
      "timestamp": "2024-11-15T10:25:02Z"
    }
  ]
}
```

#### Preguntas Frecuentes

**GET /api/faqs/:course_id**
```
Descripción: Obtener preguntas frecuentes del curso
Authorization: Bearer <session_token>

Respuesta exitosa (200):
{
  "course_id": "67890",
  "faqs": [
    {
      "id": "faq_1",
      "category": "Contenido del curso",
      "question": "¿Cuál es el contenido del curso?",
      "answer": "El curso cubre..."
    },
    {
      "id": "faq_2",
      "category": "Evaluación",
      "question": "¿Cómo se evalúa este curso?",
      "answer": "La evaluación incluye..."
    }
  ]
}
```

#### Administración

**PUT /api/admin/faqs/:course_id**
```
Descripción: Actualizar preguntas frecuentes (solo docentes)
Authorization: Bearer <session_token>
Content-Type: application/json

Body:
{
  "faqs": [
    {
      "category": "Fechas",
      "question": "¿Cuándo es el examen final?",
      "answer": "El examen final es..."
    }
  ]
}

Respuesta exitosa (200):
{
  "message": "FAQs actualizadas exitosamente",
  "updated_count": 1
}

Errores:
- 403: Usuario no autorizado (no es docente del curso)
```

**GET /api/admin/stats/:course_id**
```
Descripción: Estadísticas de uso (solo docentes)
Authorization: Bearer <session_token>

Respuesta exitosa (200):
{
  "course_id": "67890",
  "total_conversations": 234,
  "total_messages": 1450,
  "unique_users": 45,
  "avg_response_time": 2.1,
  "most_asked_questions": [
    {
      "question": "¿Cuándo es la entrega del proyecto?",
      "count": 67
    }
  ],
  "period": "last_30_days"
}
```

### Integración con AWS Bedrock

**Configuración del Cliente:**
```javascript
const {BedrockRuntimeClient, InvokeModelCommand} = require("@aws-sdk/client-bedrock-runtime");

const client = new BedrockRuntimeClient({
  region: process.env.AWS_REGION,
  credentials: {
    accessKeyId: process.env.AWS_ACCESS_KEY_ID,
    secretAccessKey: process.env.AWS_SECRET_ACCESS_KEY
  }
});
```

**Ejemplo de Invocación:**
```javascript
async function generateResponse(userMessage, context) {
  const payload = {
    anthropic_version: "bedrock-2023-05-31",
    max_tokens: 1024,
    messages: [
      {
        role: "user",
        content: `Contexto del curso: ${context}\n\nPregunta del estudiante: ${userMessage}`
      }
    ]
  };

  const command = new InvokeModelCommand({
    modelId: "anthropic.claude-haiku-v1",
    contentType: "application/json",
    accept: "application/json",
    body: JSON.stringify(payload)
  });

  const response = await client.send(command);
  const result = JSON.parse(new TextDecoder().decode(response.body));
  
  return {
    text: result.content[0].text,
    tokensUsed: result.usage.output_tokens
  };
}
```

---

## ANEXO E: Esquema de Base de Datos

### Colecciones MongoDB

#### Collection: `conversations`

```javascript
{
  _id: ObjectId("..."),
  conversation_id: "conv_abc123",
  user_id: "12345",
  course_id: "67890",
  created_at: ISODate("2024-11-15T10:25:00Z"),
  updated_at: ISODate("2024-11-15T10:30:00Z"),
  messages: [
    {
      message_id: "msg_1",
      role: "user",  // "user" o "assistant"
      content: "¿Cuáles son las fechas de entrega?",
      timestamp: ISODate("2024-11-15T10:25:00Z"),
      tokens_used: null  // solo para mensajes del asistente
    },
    {
      message_id: "msg_2",
      role: "assistant",
      content: "Las fechas de entrega son...",
      timestamp: ISODate("2024-11-15T10:25:02Z"),
      tokens_used: 150,
      source: "ai"  // "ai" o "faq"
    }
  ],
  metadata: {
    total_messages: 2,
    total_tokens: 150
  }
}
```

**Índices:**
```javascript
db.conversations.createIndex({ user_id: 1, course_id: 1 });
db.conversations.createIndex({ created_at: -1 });
db.conversations.createIndex({ conversation_id: 1 }, { unique: true });
```

#### Collection: `courses`

```javascript
{
  _id: ObjectId("..."),
  course_id: "67890",
  course_name: "Programación Web I",
  faqs: [
    {
      faq_id: "faq_1",
      category: "Contenido del curso",
      question: "¿Cuál es el contenido del curso?",
      answer: "El curso cubre HTML, CSS, JavaScript...",
      created_by: "prof_123",
      created_at: ISODate("2024-09-01T00:00:00Z")
    }
  ],
  settings: {
    enabled: true,
    max_tokens_per_query: 1024,
    response_temperature: 0.7
  },
  created_at: ISODate("2024-09-01T00:00:00Z"),
  updated_at: ISODate("2024-11-15T10:00:00Z")
}
```

**Índices:**
```javascript
db.courses.createIndex({ course_id: 1 }, { unique: true });
```

#### Collection: `users`

```javascript
{
  _id: ObjectId("..."),
  user_id: "12345",
  canvas_id: "canvas_12345",
  name: "Juan Pérez",
  email: "juan.perez@iudigital.edu.co",
  role: "student",  // "student", "teacher", "admin"
  courses: ["67890", "67891"],
  preferences: {
    language: "es",
    notifications: true
  },
  created_at: ISODate("2024-09-01T00:00:00Z"),
  last_login: ISODate("2024-11-15T10:25:00Z")
}
```

**Índices:**
```javascript
db.users.createIndex({ user_id: 1 }, { unique: true });
db.users.createIndex({ canvas_id: 1 });
```

#### Collection: `usage_stats`

```javascript
{
  _id: ObjectId("..."),
  date: ISODate("2024-11-15T00:00:00Z"),
  course_id: "67890",
  metrics: {
    total_conversations: 23,
    total_messages: 145,
    unique_users: 15,
    total_tokens: 12500,
    avg_response_time: 2.1,
    peak_concurrent_users: 8
  },
  top_questions: [
    {
      question: "¿Cuándo es la entrega del proyecto?",
      count: 12
    }
  ]
}
```

**Índices:**
```javascript
db.usage_stats.createIndex({ date: -1, course_id: 1 });
```

---

## ANEXO F: Consideraciones de Seguridad

### Medidas de Seguridad Implementadas

#### 1. Autenticación y Autorización

**Autenticación LTI:**
- Validación de firma OAuth en cada request LTI
- Verificación de consumer key y secret
- Validación de timestamp para prevenir replay attacks
- Tokens de sesión JWT con expiración de 8 horas

**Autorización basada en roles:**
- Estudiantes: solo acceso a sus conversaciones
- Docentes: acceso a estadísticas y configuración de su curso
- Administradores: acceso completo al sistema

#### 2. Protección de Datos

**Encriptación:**
- HTTPS/TLS 1.2+ para todas las comunicaciones
- Encriptación de tokens JWT
- Variables de entorno para credenciales sensibles (nunca en código)

**Privacidad:**
- No se almacenan contraseñas de usuario
- Datos de conversación segregados por curso
- Cumplimiento con políticas institucionales de privacidad

#### 3. Validación de Entrada

**Sanitización de inputs:**
- Validación de longitud máxima de mensajes (5000 caracteres)
- Escapado de caracteres especiales para prevenir injection
- Validación de tipos de datos en APIs

#### 4. Rate Limiting

```javascript
// Implementado en backend
const rateLimit = require("express-rate-limit");

const apiLimiter = rateLimit({
  windowMs: 60 * 1000, // 1 minuto
  max: 30, // máximo 30 requests por minuto por IP
  message: "Demasiadas solicitudes, por favor intente más tarde"
});

app.use("/api/", apiLimiter);
```

#### 5. Monitoreo y Logging

**Logs de seguridad:**
- Intentos de autenticación fallidos
- Accesos no autorizados
- Errores de validación de tokens
- Actividad sospechosa (patrones anómalos)

**Retención de logs:**
- Logs de aplicación: 30 días
- Logs de seguridad: 90 días
- Respaldos: según política institucional

### Recomendaciones de Seguridad para Producción

1. **Cambiar todas las credenciales por defecto**
   - Generar nuevos LTI consumer key/secret
   - Rotar AWS access keys regularmente
   - Actualizar SESSION_SECRET

2. **Configurar firewall**
   - Permitir solo puertos 443 (HTTPS) y 22 (SSH)
   - Restringir acceso SSH solo a IPs institucionales

3. **Habilitar WAF (Web Application Firewall)**
   - Protección contra SQL injection
   - Protección contra XSS
   - Rate limiting adicional

4. **Implementar monitoreo continuo**
   - Alertas de disponibilidad del servicio
   - Alertas de uso anómalo de recursos
   - Alertas de intentos de acceso no autorizado

---

## ANEXO G: Plan de Contingencia y Rollback

### Escenarios de Contingencia

#### Escenario 1: Falla del Servicio AWS Bedrock

**Síntomas:**
- Errores 500 en API de conversaciones
- Timeouts en llamadas a AWS
- Logs indicando problemas de conectividad AWS

**Acciones:**
1. Activar modo fallback a respuestas predefinidas (FAQs)
2. Notificar a administradores por email
3. Contactar soporte AWS si persiste > 30 minutos
4. Revisar límites de cuota en cuenta AWS

**Tiempo estimado de recuperación:** < 1 hora

#### Escenario 2: Caída de Base de Datos MongoDB

**Síntomas:**
- Errores de conexión a MongoDB
- Imposibilidad de recuperar historial
- Logs: "MongoError: connection timeout"

**Acciones:**
1. Reiniciar servicio MongoDB: `sudo systemctl restart mongod`
2. Si persiste, restaurar desde último backup
3. Verificar espacio en disco (MongoDB requiere espacio libre)
4. Revisar logs de MongoDB: `/var/log/mongodb/mongod.log`

**Tiempo estimado de recuperación:** < 2 horas

#### Escenario 3: Falla de Integración LTI con Canvas

**Síntomas:**
- Estudiantes no pueden acceder desde Canvas
- Errores 401 en endpoint /lti/launch
- Logs: "Invalid OAuth signature"

**Acciones:**
1. Verificar que credenciales LTI no hayan cambiado
2. Revisar configuración en Canvas Admin
3. Validar que URLs de callback sean correctas
4. Regenerar credenciales LTI si es necesario

**Tiempo estimado de recuperación:** < 30 minutos

### Procedimiento de Rollback

**Cuándo hacer rollback:**
- Errores críticos en versión nueva (> 50% de usuarios afectados)
- Degradación severa de performance (> 10 segundos respuesta)
- Violación de seguridad detectada

**Pasos de Rollback:**

1. **Detener servicios actuales**
```bash
pm2 stop iudgpt-backend
pm2 stop iudgpt-frontend
```

2. **Restaurar código anterior**
```bash
cd iud-gpt-backend
git checkout tags/v1.0-stable  # o commit anterior estable
npm install
cd ../iud-gpt-front-end-nodejs
git checkout tags/v1.0-stable
npm install
```

3. **Restaurar base de datos (si es necesario)**
```bash
# Desde backup más reciente
mongorestore --db iudgpt /path/to/backup/iudgpt/
```

4. **Reiniciar servicios**
```bash
pm2 restart iudgpt-backend
pm2 restart iudgpt-frontend
```

5. **Verificar funcionamiento**
- Probar acceso desde Canvas
- Enviar consulta de prueba
- Verificar logs para errores

**Tiempo estimado de rollback completo:** < 15 minutos

### Respaldos Automáticos

**Script de backup diario:**
```bash
#!/bin/bash
# /opt/scripts/backup-iudgpt.sh

DATE=$(date +%Y%m%d_%H%M%S)
BACKUP_DIR=/opt/backups/iudgpt

# Backup MongoDB
mongodump --db iudgpt --out $BACKUP_DIR/mongodb_$DATE

# Backup configuraciones
cp -r /path/to/backend/.env $BACKUP_DIR/config_$DATE/
cp -r /path/to/frontend/.env $BACKUP_DIR/config_$DATE/

# Eliminar backups > 30 días
find $BACKUP_DIR -type d -mtime +30 -exec rm -rf {} +

# Notificar éxito
echo "Backup completado: $DATE" | mail -s "IUD GPT Backup" admin@iudigital.edu.co
```

**Configurar en crontab:**
```bash
# Ejecutar todos los días a las 2:00 AM
0 2 * * * /opt/scripts/backup-iudgpt.sh
```

---

## ANEXO H: Requerimientos de Infraestructura

### Especificaciones Mínimas de Servidor

**Ambiente de Producción:**

**Servidor de Aplicación (Backend + Frontend):**
- CPU: 4 cores mínimo (recomendado 8)
- RAM: 8 GB mínimo (recomendado 16 GB)
- Almacenamiento: 50 GB SSD
- Ancho de banda: 100 Mbps mínimo
- Sistema operativo: Ubuntu Server 20.04 LTS o superior

**Servidor de Base de Datos (MongoDB):**
- CPU: 2 cores mínimo (recomendado 4)
- RAM: 4 GB mínimo (recomendado 8 GB)
- Almacenamiento: 100 GB SSD (con capacidad de expansión)
- Recomendación: Usar MongoDB Atlas (gestionado) para reducir carga operativa

**Balanceador de Carga (Opcional pero recomendado):**
- Nginx o HAProxy
- CPU: 2 cores
- RAM: 2 GB

### Estimación de Recursos AWS

**Costos mensuales estimados (basado en uso actual):**

```
Servicio: AWS Bedrock (Claude Haiku)
Escenario: 500 estudiantes, 20 consultas/estudiante/mes
Cálculo:
- 500 estudiantes × 20 consultas = 10,000 consultas/mes
- Promedio 150 tokens de salida por consulta
- 10,000 × 150 = 1,500,000 tokens/mes de salida
- Costo por 1M tokens output: ~$1.25 USD
- Costo por 1M tokens input: ~$0.25 USD (estimado similar input)

Costo estimado: $2-3 USD/mes (uso ligero)
Costo máximo esperado: $20-30 USD/mes (uso intensivo)
```

**Recomendaciones:**
- Configurar alertas de facturación AWS en $50 USD
- Monitorear uso semanal de tokens
- Implementar caché de respuestas frecuentes para reducir llamadas a API

### Escalabilidad

**Capacidad actual soportada:**
- Usuarios concurrentes: 50-100
- Consultas por segundo: 10-15
- Almacenamiento conversaciones: ~1 GB por 10,000 conversaciones

**Plan de escalamiento (si se requiere más capacidad):**

**Fase 1: Optimización (0-500 usuarios activos)**
- Usar servidor único con recursos actuales
- Implementar caché Redis para respuestas frecuentes

**Fase 2: Escalamiento Vertical (500-2000 usuarios)**
- Aumentar RAM a 32 GB
- Migrar a CPU con 16 cores
- Implementar MongoDB con réplica set

**Fase 3: Escalamiento Horizontal (2000+ usuarios)**
- Múltiples instancias de aplicación con load balancer
- MongoDB cluster con sharding
- CDN para assets estáticos
- Considerar migrar a contenedores (Docker/Kubernetes)

---

## ANEXO I: SLA Propuestos

### Acuerdos de Nivel de Servicio Recomendados

**Disponibilidad del Sistema:**
- Objetivo: 99.5% mensual (equivale a ~3.6 horas de downtime permitido/mes)
- Horario de servicio: 24/7
- Ventanas de mantenimiento: Domingos 2:00-4:00 AM (notificadas con 48h anticipación)

**Tiempos de Respuesta:**
- Consultas simples (FAQs): < 1 segundo (95% de casos)
- Consultas con IA: < 3 segundos (90% de casos)
- Carga inicial de interfaz: < 5 segundos

**Soporte Técnico:**
- Incidentes críticos (sistema caído): Respuesta en < 1 hora
- Incidentes altos (degradación severa): Respuesta en < 4 horas
- Incidentes medios: Respuesta en < 24 horas
- Consultas generales: Respuesta en < 48 horas

**Backups y Recuperación:**
- Backups diarios automatizados
- Retención: 30 días de backups
- Tiempo de recuperación (RPO): < 24 horas
- Punto de recuperación (RTO): < 1 hora para datos críticos

---

## ANEXO J: Checklist de Entrega

### Verificación de Completitud

**Código Fuente:**
- [x] Repositorio backend accesible en GitLab institucional
- [x] Repositorio frontend accesible en GitLab institucional
- [x] Archivos .env.example incluidos (sin credenciales reales)
- [x] README.md con instrucciones básicas
- [x] Archivo package.json con dependencias

**Documentación:**
- [x] Manual de instalación completo
- [x] Manual de usuario (estudiantes)
- [x] Manual de usuario (docentes)
- [x] Manual de administrador
- [x] Documentación de API
- [x] Esquema de base de datos
- [x] Diagrama de arquitectura

**Configuraciones:**
- [x] Configuración LTI para Canvas
- [x] Variables de entorno documentadas
- [x] Scripts de respaldo incluidos
- [x] Configuración de Nginx (ejemplo)

**Pruebas:**
- [x] Casos de prueba documentados
- [x] Criterios de aceptación definidos
- [x] Resultados de pruebas funcionales
- [x] Evidencias de pruebas con usuarios

**Seguridad:**
- [x] Medidas de seguridad documentadas
- [x] Plan de contingencia definido
- [x] Procedimiento de rollback documentado
- [x] Recomendaciones de seguridad

**Infraestructura:**
- [x] Requerimientos de servidor especificados
- [x] Estimación de costos AWS
- [x] Plan de escalabilidad
- [x] SLA propuestos

### Entregables Físicos/Digitales

1. **Repositorio GitLab:**
   - URL Backend: https://gitlab.iudigital.edu.co/ds-iudigital/iud-gpt/iud-gpt-backend
   - URL Frontend: https://gitlab.iudigital.edu.co/ds-iudigital/iud-gpt/iud-gpt-front-end-nodejs
   - Acceso: Concedido a equipo de Dirección de Tecnología

2. **Documentación (este documento):**
   - Formato: PDF
   - Versión: 1.0
   - Fecha: Enero 2026

3. **Credenciales y Configuraciones:**
   - Archivo cifrado con credenciales AWS (entrega presencial)
   - Consumer Key y Secret LTI (entrega presencial)
   - Acceso administrativo MongoDB (coordinar con equipo)

4. **Capacitación:**
   - Sesión de transferencia de conocimiento (fecha a coordinar)
   - Q&A session con equipo técnico
   - Contacto para soporte post-entrega (30 días)

---

## Declaración de Entrega

El equipo investigador certifica que:

1. Todo el código fuente entregado está funcional y probado
2. La documentación técnica está completa y actualizada
3. No existen dependencias críticas no documentadas
4. El sistema cumple con todos los criterios de aceptación definidos
5. Se han proporcionado todos los manuales e instrucciones necesarias

El sistema IUD GPT está listo para implementación en ambiente productivo bajo gestión de la Dirección de Tecnología de la Institución Universitaria Digital de Antioquia.

**Equipo Investigador:**

_________________________  
Boris Alberto Salleg Royero  
Coinvestigador  

_________________________  
Jorge Armando Julio Cruz  
Coinvestigador  

**Fecha:** ____________ de Enero de 2026

---

**FIN DE DOCUMENTACIÓN TÉCNICA**
