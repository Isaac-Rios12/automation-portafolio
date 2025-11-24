# automation-portafolio
# 🏥 Asistente de Gestión de Citas Médicas con IA  
Agente inteligente diseñado para gestionar citas médicas utilizando Google Calendar y Firestore, con reglas empresariales estrictas, validación de horarios, uso de fechas reales y flujo conversacional seguro.

Este proyecto fue creado como demostración de capacidades avanzadas en ingeniería de prompts, diseño de agentes y flujos conversacionales profesionales.

![alt text](image.png)

---

## 🚀 Características principales

### ✔️ Integración real con:
- **Google Calendar** (creación de eventos)
- **Firestore** (registro estructurado de citas)
- **API de Doctores**
- **API de Citas por fecha/hora**

### ✔️ Inteligencia de calendario avanzada
- Obtiene automáticamente la fecha/hora actual mediante `{{ $now }}`
- Calcula día de la semana, fecha interpretada y validaciones temporales
- Detecta si la hora solicitada ya pasó
- Valida disponibilidad en tiempo real
- Sugiere horarios alternativos sin inventarlos

### ✔️ Flujo conversacional empresarial
1. Motivo y nombre del paciente  
2. Selección de doctor  
3. Validación de fecha y hora  
4. Confirmación final  
5. Creación de cita en Calendar  
6. Registro en Firestore  

Con reglas estrictas para evitar errores, duplicados y violaciones de privacidad.

---

## 🧠 Prompt del agente

El agente se rige por un **sistema de reglas estrictas**, incluyendo:

- Confidencialidad absoluta  
- No revelar eventos existentes  
- No inventar doctores, horarios ni datos  
- Validar todo con herramientas externas  
- No crear una cita sin confirmación explícita  
- Una sola cita por conversación  

El prompt completo se encuentra en:  
`/prompt/main_prompt.md`

---

## 📂 Estructura del proyecto

/medical-scheduler-agent
│
├── prompt/
│ └── main_prompt.md # Prompt completo del agente
│
├── src/
│ ├── agent.json # Configuración del agente
│ ├── tools/ # Definición de herramientas externas
│ └── examples/ # Ejemplos de uso
│
├── README.md
└── LICENSE (opcional)