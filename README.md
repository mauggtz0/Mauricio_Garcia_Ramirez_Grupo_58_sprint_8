# Proyecto Urban Grocers

## Descripción
Proyecto de automatización de pruebas para la API de Urban Grocers.
Se prueban los valores límite del campo `name` en la solicitud de creación de un kit de productos.

## Tecnologías y técnicas utilizadas
- **Python** — lenguaje de programación
- **pytest** — framework de pruebas automatizadas
- **requests** — librería para enviar solicitudes HTTP
- **Análisis de Valores Límite (BVA)** — técnica de pruebas para validar los límites de los campos

## Fuente de documentación
La documentación del API fue consultada en apiDoc (documentación interna del servidor de Urban Grocers).

## Cómo ejecutar las pruebas
pytest create_kit_name_kit_test.py -v
