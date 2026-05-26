# Estructura MVC - Backend de Horarios

## Descripción
Model-View-Controller clásico. El Modelo contiene las entidades y lógica de negocio, la Vista son las respuestas JSON (o vistas HTML si aplica), y el Controlador maneja peticiones HTTP.

## Ventajas
- Sencillo y ampliamente conocido
- Rápido de implementar
- Bueno para APIs REST simples o prototipos

## Desventajas
- Escalabilidad limitada
- Mezcla de responsabilidades en controladores grandes
- No ideal para backend complejo con múltiples dominios

## Estructura de Carpetas

ProyectoHorarios/
│
├── Model/                      ← TODA la lógica y datos
│   ├── Entity/                 ← Tablas DB
│   ├── IRepository/            ← Contratos DB
│   ├── Repository/             ← Implementación DB
│   ├── IService/               ← Contratos negocio
│   ├── Service/                ← Lógica negocio
│   ├── DTO/                    ← Transferencia datos
│   ├── IDTO/                   ← Contratos DTO
│   └── Utils/                  ← Helpers (JWT, procesos)
│
├── View/                       ← Presentación (JSON o HTML)
│   ├── Responses/              ← Para API
│   └── (Vistas .cshtml)        ← Para Web
│
└── Controller/                 ← Controladores HTTP
    ├── Security/
    └── Inventory/