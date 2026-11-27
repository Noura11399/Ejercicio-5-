# Ejercicio 5 
📊 **Motor de Segmentación de Clientes (RFM Simplificado)**

Nivel: Inicial

🔴 ***OBJETIVO DE NEGOCIO***

Clasificar automáticamente la cartera de clientes según su comportamiento de compra para que
marketing pueda enviar campañas personalizadas.

⚠️ **QUÉ DEBE HACER TU CÓDIGO (GUÍA DE TRABAJO)**

Definir reglas de negocio: 
Evaluar para cada cliente tres variables: 
  - Hace cuántos días compró (Recencia)
  - Cuántas veces compró (Frecuencia) y cuánto gastó (Valor Monetario)
  - Etiquetar perfiles: Asignar a cada cliente una categoría (VIP, Leal, En riesgo, Nuevo o Inactivo) combinando condiciones (if / elif / else) sobre sus métricas.
  - Resumir la cartera: Contar cuántos clientes cayeron en cada segmento y calcular cuánto dinero aporta cada grupo al negocio.

🟢 **DATASET SIMULADO (PYTHON PURO)**

clientes_rfm = [
    {
        "cliente_id": "CL01",
        "nombre": "Ana Silva",
        "gasto_total": 2400.0,
        "dias_ultima_compra": 5,
        "frecuencia_compras": 15
    },
    {
        "cliente_id": "CL02",
        "nombre": "Luis Gomez",
        "gasto_total": 950.0,
        "dias_ultima_compra": 20,
        "frecuencia_compras": 8
    },
    {
        "cliente_id": "CL03",
        "nombre": "Carla Ruiz",
        "gasto_total": 1850.0,
        "dias_ultima_compra": 110,
        "frecuencia_compras": 12
    },
    {
        "cliente_id": "CL04",
        "nombre": "Pedro Diaz",
        "gasto_total": 45.0,
        "dias_ultima_compra": 240,
        "frecuencia_compras": 1
    },
    {
        "cliente_id": "CL05",
        "nombre": "Elena Mora",
        "gasto_total": 180.0,
        "dias_ultima_compra": 12,
        "frecuencia_compras": 2
    },
    {
        "cliente_id": "CL06",
        "nombre": "Jorge Pino",
        "gasto_total": 1100.0,
        "dias_ultima_compra": 95,
        "frecuencia_compras": 9
    },
    {
        "cliente_id": "CL07",
        "nombre": "Sofia Lara",
        "gasto_total": 3200.0,
        "dias_ultima_compra": 3,
        "frecuencia_compras": 20
    },
    {
        "cliente_id": "CL08",
        "nombre": "Mario Soto",
        "gasto_total": 60.0,
        "dias_ultima_compra": 300,
        "frecuencia_compras": 1
    }
]

✅ **RESULTADO**

***Clasificación de clientes***

| Cliente | Segmento | Gasto ($) | Días sin comprar |
| :--- | :---: | ---: | ---: |
| Ana Silva | VIP | $2,400.00 | 5 |
| Luis Gomez | Leal | $950.00 | 20 |
| Carla Ruiz | En riesgo | $1,850.00 | 110 |
| Pedro Diaz | Inactivo | $45.00 | 240 |
| Elena Mora | Nuevo | $180.00 | 12 |
| Jorge Pino | En riesgo | $1,100.00 | 95 |
| Sofia Lara | VIP | $3,200.00 | 3 |
| Mario Soto | Inactivo | $60.00 | 300 |

***Resumen de cartera*** 

| Segmento | Clientes | Aporte total |
| :--- | :---: | ---: |
| VIP | 2 | $5,600.00 |
| Leal | 1 | $950.00 |
| En riesgo | 2 | $2,950.00 |
| Inactivo | 2 | $105.00 |
| Nuevo | 1 | $180.00 |
