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

## Estructura del proyecto
- `configuration.py` - URLs y endpoints de la API
- `data.py` - Datos de prueba (cuerpos de solicitudes)
- `sender_stand_request.py` - Funciones para enviar solicitudes HTTP
- `create_kit_name_kit_test.py` - Casos de prueba automatizados

## Lista de pruebas
| # | Descripción | Resultado esperado |
|---|-------------|-------------------|
| 1 | 1 carácter | 201 |
| 2 | 511 caracteres | 201 |
| 3 | 0 caracteres | 400 |
| 4 | 512 caracteres | 400 |
| 5 | Caracteres especiales | 201 |
| 6 | Espacios | 201 |
| 7 | Números | 201 |
| 8 | Sin parámetro name | 400 |
| 9 | Tipo número | 400 |

## Cómo ejecutar las pruebas
```bash
pytest create_kit_name_kit_test.py -v
