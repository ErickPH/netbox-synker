# netbox-synker
# 🔧 Proxmox Inventory to NetBox Plugin

Este repositorio contiene un plugin en desarrollo para obtener el inventario de objetos desde una instancia de **Proxmox VE** utilizando su **API REST** en modo **readonly**, y luego integrarlos de forma automatizada en **NetBox** como fuente de verdad para infraestructura.

## 🚀 Objetivo

El propósito principal de este plugin es facilitar la sincronización de datos entre Proxmox y NetBox, permitiendo que los objetos virtuales (VMs, contenedores, nodos, etc.) sean consultados y representados en NetBox sin intervención manual.

## 🔒 Seguridad y alcance

- El plugin **solo realiza consultas (GET)** al API de Proxmox.
- No modifica, elimina ni crea objetos en Proxmox.
- Utiliza credenciales con permisos **readonly**, minimizando cualquier riesgo operativo.
- La integración con NetBox se realiza mediante su API, respetando los modelos y relaciones definidos en dicha plataforma.

## ⚠️ Estado del proyecto

Este código está en fase de desarrollo y **no está diseñado para entornos de producción**. Se recomienda su uso únicamente para pruebas, validación de conceptos o entornos controlados.

## 📦 Funcionalidades previstas

- Consulta de inventario de:
  - Máquinas virtuales (QEMU)
  - Contenedores (LXC)
  - Nodos físicos
- Mapeo básico de atributos relevantes (nombre, estado, recursos, etiquetas)
- Inserción automatizada en NetBox como dispositivos virtuales o instancias personalizadas
- Registro de logs para auditoría y trazabilidad

## 🛠️ Requisitos

- Proxmox VE con acceso API habilitado
- Usuario o token con permisos readonly
- Instancia de NetBox accesible vía API
- Python 3.8+ (dependencias detalladas en `requirements.txt`)

## 📌 Nota legal y técnica

Este proyecto no está afiliado oficialmente con Proxmox ni NetBox. Su uso queda bajo responsabilidad del usuario. Se recomienda revisar y adaptar el código antes de cualquier implementación institucional.

---

¿Te gustaría que lo traduzca al inglés para una versión bilingüe, o que incluya ejemplos de configuración y ejecución? También puedo ayudarte a redactar una sección de licencia o contribuciones si decides abrirlo a colaboradores selectos.
