# Laboratorio 2 – Continuous Integration

Este proyecto implementa una librería de **matemática básica** en Python con un conjunto de funciones simples, pruebas unitarias y un flujo de integración continua mediante **GitHub Actions**.

## 📌 Objetivos

- Desarrollar una librería pequeña con funciones matemáticas básicas.
- Implementar pruebas unitarias con casos exitosos y casos borde/error.
- Gestionar el proyecto con control de versiones en Git y GitHub.
- Configurar un workflow de **CI con GitHub Actions** que ejecute automáticamente los tests en cada Pull Request hacia la rama `main`.

## 📂 Estructura del proyecto

```
lab-ci/
├── src/
│   └── mathlib.py          # Librería con las funciones matemáticas
├── tests/
│   └── test_mathlib.py     # Pruebas unitarias con pytest
├── .github/
│   └── workflows/
│       └── ci.yml          # Configuración de GitHub Actions
├── requirements.txt        # Dependencias del proyecto
└── README.md              # Documentación del proyecto
```

## ⚙️ Funciones implementadas

- `square(n)` → Retorna el cuadrado de un número.
- `factorial(n)` → Retorna el factorial de un número entero no negativo.
- `is_prime(n)` → Retorna si un número es primo o no.
- `gcd(a, b)` → Retorna el máximo común divisor entre dos números.
- `lcm(a, b)` → Retorna el mínimo común múltiplo entre dos números.

## 🧪 Pruebas unitarias

Las pruebas fueron desarrolladas con **pytest** y cubren:
- Dos casos de "happy path" por cada función.
- Un caso borde o de error en cada función.
- Validación de que los tests fallan si la lógica es modificada incorrectamente.

Para ejecutar las pruebas localmente:

```bash
pytest
```

## 🔄 Integración Continua

Se configuró un workflow con GitHub Actions que:
- Se ejecuta en cada Pull Request hacia `main`.
- Instala dependencias y corre los tests con pytest.
- Bloquea el merge si las pruebas no pasan.

Archivo del workflow: `.github/workflows/ci.yml`

## ✅ Rúbrica cumplida

- ✅ Funciones implementadas correctamente con casos borde.
- ✅ Control de versiones en GitHub.
- ✅ Pruebas unitarias con escenarios exitosos y de error.
- ✅ Workflow en GitHub Actions activo en cada Pull Request.

## 🚀 Instalación y uso

1. Clona el repositorio:
```bash
git clone <url-del-repositorio>
cd lab-ci
```

2. Instala las dependencias:
```bash
pip install -r requirements.txt
```

3. Ejecuta las pruebas:
```bash
pytest
```

## 📝 Contribuir

1. Crea un fork del proyecto
2. Crea una nueva rama (`git checkout -b feature/nueva-funcion`)
3. Realiza tus cambios y commitea (`git commit -am 'Añadir nueva función'`)
4. Push a la rama (`git push origin feature/nueva-funcion`)
5. Abre un Pull Request

El workflow de CI se ejecutará automáticamente y validará que todas las pruebas pasen antes de permitir el merge.