# Examen2_Sistemas-Operativos

## Actividad 4 - Troubleshooting
# Snippet 1 corregido:
on:
  push:
    branches: [main]
  pull_request:
    branches: [main, develop]

# Snippet 2 corregido:
env:
  VERCEL_TOKEN: ${{ secrets.VERCEL_TOKEN }}

# Snippet 3 corregido:
strategy:
  matrix:
    node-version: [16, 18]

## Actividad 5 - Preguntas Conceptuales
# 1. ¿Cuál es la diferencia fundamental entre Integración Continua (CI) y Entrega Continua (CD)?
La integración continua (CI) consiste en integrar cambios de código de forma frecuente en un repositorio donde automáticamente se ejecutan pruebas y validaciones para asegurar que el código funciona correctamente.

La entrega continua (CD), se enfoca más en llevar ese código validado a un entorno de producción o despliegue de manera automatizada y así asegura que siempre esté listo para ser liberado.

# 2. ¿Qué es un GitHub self-hosted runner y cuándo sería necesario usarlo?
Es un servidor propio que se utiliza para ejecutar workflows de GitHub Actions en lugar de usar los servidores de GitHub, y se utiliza cuando se necesitan configuraciones específicas, mayor control del entorno, acceso a recursos internos o cuando los workflows requieren más capacidad o software que no está disponible en los runners estándar.

# 3. ¿Cuál es el propósito de los GitHub environments? ¿Cómo se usan en workflows?
Los GitHub environments permiten definir entornos como “development”, “staging” o “production” para gestionar despliegues de forma controlada, y se utilizan en los workflows para aplicar reglas como aprobaciones, restricciones o uso de secrets específicos según el entorno en el que se esté desplegando.

# 4. ¿Qué es una rollback strategy y cómo se implementaría en un pipeline de CD?
Una rollback strategy es un mecanismo que permite revertir una aplicación a una versión anterior en caso de que un despliegue falle.

En un pipeline de CD se puede implementar guardando versiones anteriores del sistema y configurando pasos automáticos que, al detectar un error, restauren la última versión estable.
