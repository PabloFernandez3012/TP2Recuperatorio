# TP2Recuperatorio

DIAGRAMA DEL MODELO ESTRELLA (Relaciones)
                 ┌─────────────────────┐
                 │     DIM_Producto    │
                 │ id_producto (1)     │
                 └──────────┬──────────┘
                            │
                            │ (Muchos)
┌────────────────────┐      ▼
│     FACT_Ventas    │───────────────┐
│ id_producto (*)    │               │
│ id_cliente (*)     │               │
│ id_ciudad (*)      │               │
│ fecha (*)          │               │
└───────┬────────────┘               │
        │                            │
        │                            │
        ▼                            ▼
┌───────────────┐           ┌──────────────────┐
│  DIM_Cliente   │           │   DIM_Ciudad     │
│ id_cliente (1) │           │ id_ciudad (1)    │
└────────────────┘           └──────────────────┘

                 ▲
                 │ (1)
        ┌───────────────────┐
        │   DIM_Calendario  │
        │ fecha (date) (1)  │
        └───────────────────┘

