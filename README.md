# 🛠️ Prueba de Automatización QA - Registro y Compra Simulada
## 🎯 Objetivo
Implementar una prueba automatizada utilizando Playwright con TypeScript, que simule el flujo de registro y compra en una página de e-commerce ficticia, asegurando robustez y mantenibilidad.

## 🧠 Requisitos del Proyecto
- **Framework:** Playwright con TypeScript.
- **Arquitectura:** Implementación del patrón Page Object Model (POM).
- **Configuración:** Sistema adaptable para cambiar entre entornos (staging, production).
- **Reporte:** Generación de reportes detallados con trazas y diagnóstico de fallos.

## 🔥 Escenario de Prueba Automatizado
1. **Acceso a la página:** http://localhost:3000 (basado en el proyecto Node creado previamente).
2. **Registro de usuario:**
    * Llenar el formulario con datos ficticios válidos.
    * Validar mensajes de error al dejar campos vacíos o con formato incorrecto.
3. **Agregar productos al carrito:**
* Añadir el primer y último producto de la lista.
* Incluir un producto personalizado (por ejemplo, seleccionando color/tamaño).
4. **Proceso de compra:**
* Completar los datos de pago (simulados).
* Validar que aparezca la página de confirmación.
5. **Validación de la orden:**
* Enviar un POST a un endpoint ficticio para verificar el registro de la orden.

## 🧪 Datos de Prueba Usados
* **Usuario:** Nombre generado aleatoriamente.
* **Email:** qa_tester+<timestamp>@mail.com (para asegurar unicidad).
* **Contraseña:** Password123

**Tarjeta de prueba:**
* **Número:** 4111 1111 1111 1111
* **Expiración:** 12/25
* **CVV:** 123

## ⚙️ Requisitos Técnicos Avanzados
**🎯 Estrategia de selectores**
* Implementación de selectores robustos y fallback para mantener estabilidad.
* Documentación de las decisiones clave sobre los selectores.
**⏳ Manejo de esperas**
* Uso de esperas dinámicas: waitForResponse, waitForLoadState.
* Prohibido: waitForTimeout (para evitar ralentización innecesaria).
**🛠️ Manejo de errores y recuperación**
* Captura de screenshots y trazas en caso de fallos.
* Control de errores de red y caídas inesperadas.
**🔒 Gestión de datos de prueba**
* Separación de datos sensibles y configurables (.env).
* Generación dinámica de datos (emails únicos y nombres aleatorios).

## 📝 Criterios de Evaluación
* Estructura del código: Claridad, organización y legibilidad.
* Robustez: La prueba debe resistir cambios pequeños en la UI.
* Manejo de errores: Resiliencia ante fallos de red o tiempos de carga lentos.
* Uso efectivo de TypeScript: Tipado fuerte y control de errores.
* Reporte final: Generación de informes detallados y visuales.

## 📦 Entrega Esperada
* Repositorio GitHub con instrucciones claras (README.md).
* Historial de commits bien estructurado para reflejar la evolución del proyecto.
* Explicación breve sobre las decisiones arquitectónicas tomadas.

