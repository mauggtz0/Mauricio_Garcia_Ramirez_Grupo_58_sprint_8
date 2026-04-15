# API Stand Tests

Proyecto de automatización de pruebas para la API de registro de usuarios.

## Descripción

Suite de pruebas automatizadas que valida el endpoint de creación de usuarios,
incluyendo casos positivos y negativos para el parámetro `firstName`.

## Tecnologías utilizadas

- Python
- Pytest
- Requests

## Instalación

1. Clona el repositorio
2. Crea un entorno virtual: `python -m venv venv`
3. Actívalo: `source venv/bin/activate` (Mac/Linux) o `venv\Scripts\activate` (Windows)
4. Instala dependencias: `pip install pytest requests`

## Cómo ejecutar las pruebas

```bash
pytest create_user_test.py
```

## Casos de prueba

| # | Descripción | Resultado esperado |
|---|-------------|-------------------|
| 1 | firstName con 2 caracteres | 201 ✅ |
| 2 | firstName con 15 caracteres | 201 ✅ |
| 3 | firstName con 1 carácter | 400 ❌ |
| 4 | firstName con 16 caracteres | 400 ❌ |
| 5 | firstName con letras latinas | 201 ✅ |
| 6 | firstName con caracteres especiales | 400 ❌ |
| 7 | firstName con dígitos | 400 ❌ |
| 8 | Sin parámetro firstName | 400 ❌ |
| 9 | firstName vacío | 400 ❌ |
| 10 | firstName tipo número | 400 ❌ |