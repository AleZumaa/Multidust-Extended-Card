# Multidust-Extended-Card

## Placa Extensora / Breakout de Pruebas (Test Adapter Board)

Placa de circuito impreso (PCB) diseñada como interfaz de interconexión y depuración para medición, ruteo y diagnóstico de señales. Permite derivar conectores multicable de cinta plana (IDC / HE10) hacia puntos de prueba o pines header individuales (J1 a J130), facilitando el conexionado con osciloscopios, analizadores lógicos, multímetros o protoboards.

---

## 🛠️ Herramientas de Diseño (EDA)

* **Software:** [KiCad EDA](https://www.kicad.org/)
* **Versión:** `v10.0.1`

> ℹ️ **Nota de compatibilidad:** El esquema y el layout fueron diseñados con **KiCad 10.0.1**. Para abrir y editar los archivos de proyecto sin problemas de migración de footprints o bibliotecas de símbolos, se recomienda utilizar KiCad 10.0.1 o superior.

---

## 📋 Características Principales

- **Conectores Principales:**
  - `CONN-1`: IDC / HE10 hembra/macho de **40 pines** (`HE10-40-1`).
  - `CONN-2`: IDC / HE10 hembra/macho de **40 pines** (`HE10-40-2`).
  - `CONN-3`: IDC / HE10 hembra/macho de **40 pines** (`HE10-40-3`).
  - `CONN-4`: IDC / HE10 hembra/macho de **10 pines** (`HE10-10`).
- **Puntos de Medición / Breakout:**
  - 130 terminales individuales tipo pad / pin-header paso 2.54 mm (`J1` a `J130`).
  - Distribución en doble hilera perimétrica (izquierda/derecha) con pads cuadrados/redondos para facilitar la colocación de puntas de prueba o pines macho/hembra.
- **Topología de PCB:**
  - Placa de 2 capas (*Double-sided FR4*).
  - Pistas con trazado a 45° optimizado para mantener integridad de señal básica y separación uniforme.
  - Indicadores serigrafiados de orientación (flechas triangulares en pin 1 de cada conector IDC).

---

## 📐 Especificaciones Técnicas

| Parámetro | Valor / Descripción |
| :--- | :--- |
| **Tipo de Placa** | Breakout / Adapter / Test Board |
| **Software EDA** | **KiCad v10.0.1** |
| **Capas** | 2 capas (Top / Bottom) |
| **Material sugerido** | FR-4 estándar (1.6 mm espesor) |
| **Acabado sugerido** | HASL Lead-Free o ENIG (recomendado para pads de prueba) |
| **Paso de Conectores IDC** | 2.54 mm (0.1") |
| **Paso de Headers de Prueba** | 2.54 mm (0.1") estándar |
| **Capacidad de Señal** | Señales lógicas, buses digitales (GPIO, SPI, UART, I2C, bus paralelo) y alimentación de baja corriente |

---

## 🔌 Asignación de Conectores y Ruteo

| Conector | Tipo / Descripción | Rango de Pines Breakout |
| :---: | :---: | :---: |
| **CONN-1** | HE10-40 (40 pines) | `J1` – `J40` |
| **CONN-2** | HE10-40 (40 pines) | `J41` – `J80` |
| **CONN-3** | HE10-40 (40 pines) | `J81` – `J120` |
| **CONN-4** | HE10-10 (10 pines) | `J121` – `J130` |

> ⚠️ **Nota:** Verificar siempre la correspondencia entre la serigrafía (flecha de pin 1 en `CONN-1..4`) y la muesca polarizadora del cable plano IDC antes de alimentar el circuito bajo prueba.

---

## 🛠️ Lista de Materiales (BOM)

| Designador | Cantidad | Componente / Descripción | Encapsulado / Footprint |
| :--- | :---: | :--- | :--- |
| `CONN-1`, `CONN-2`, `CONN-3` | 3 | Conector Header tipo caja IDC 40 pines (2x20) paso 2.54 mm | Through-Hole (THT) 2.54 mm |
| `CONN-4` | 1 | Conector Header tipo caja IDC 10 pines (2x5) paso 2.54 mm | Through-Hole (THT) 2.54 mm |
| `J1` - `J130` | 130 | Tiras de pines hembra o macho / Puntos de prueba (Test Points) | Pad / THT individual 2.54 mm |

---

## 📁 Estructura del Repositorio

```text
├── Hardware/
│   ├── Schematics/         # Esquemáticos en formato KiCad v10.0.1 (.kicad_sch)
│   ├── PCB/                # Archivo de PCB KiCad v10.0.1 (.kicad_pcb)
│   └── Gerbers/            # Archivos de fabricación (Gerber RS-274X, Drill files)
├── Docs/
│   ├── Pinout_Mapping.csv  # Mapeo detallado señal por señal
│   └── Dimensions.pdf      # Plano mecánico acotado
└── README.md
```

---

## 📄 Licencia

Este hardware se distribuye bajo licencia libre [CERN-OHL-P](https://ohwr.org/cern_ohl_p_v2.txt) (Open Hardware Licence Permissive) o [MIT License](LICENSE).
