# 🌤️ Clasificación de Imágenes Climáticas usando Redes Neuronales Convolucionales

## 📋 Descripción del Proyecto
Este proyecto implementa y compara dos enfoques de deep learning para clasificación de imágenes climáticas:
- **CNN Personalizado** (arquitectura customizada)
- **ResNet-50** (arquitectura preentrenada con fine-tuning)

### 🎯 Objetivo
Desarrollar sistemas de clasificación robustos para categorizar imágenes en tres clases climáticas:
- ☀️ Amanecer (sunrise)
- ☁️ Nublado (cloudy)  
- 🌧️ Lluvia (rain)

## 📊 Resultados Destacados

### 🏆 Comparativa Final de Modelos

| Métrica | CNN Personalizado | ResNet-50 | Diferencia |
|---------|-------------------|-----------|------------|
| **Mejor Accuracy** | 96.45% | 94.38% | **+2.07%** |
| **Tiempo/Época** | 6-8 segundos | 29-46 segundos | **5.3x más rápido** |
| **Épocas Convergencia** | 43 | 69 | **37% más rápido** |
| **Estabilidad** | Alta | Media | **Más estable** |

### 📈 Tabla Comparativa Detallada

| Métrica | CNN Personalizado | ResNet-50 |
|---------|-------------------|-----------|
| Mejor Accuracy Validación | 96.45% (Época 43) | 94.38% (Época 69) |
| Accuracy Promedio (últimas 10) | 94.2% | 92.8% |
| Mejor Loss Validación | 0.0959 | 0.1361 |
| Tiempo por Época | 6-8 segundos | 29-46 segundos |
| Estabilidad | Alta (variación ±3%) | Media (variación ±8%) |

## 🏅 Conclusión y Recomendaciones

### 🥇 **GANADOR GENERAL: CNN PERSONALIZADO**
- **Accuracy:** 96.45%
- **Tiempo Total:** ~6 minutos
- **Ventajas:** Mayor velocidad, mejor rendimiento, menor consumo computacional

### 🥈 **RESNET-50** 
- **Accuracy:** 94.38% 
- **Tiempo Total:** ~58 minutos
- **Ventajas:** Arquitectura establecida, buen potencial para transfer learning

## 🗂️ Estructura del Proyecto
clasificacion_clima/
├── 📁 notebooks/
│ └── clasificacion_del_clima.ipynb # Notebook principal
├── 📁 data/
│ ├── raw/ # Datos originales
│ ├── processed/ # Datos procesados
│ └── external/ # Datos externos
├── 📁 src/ # Código fuente
├── 📁 models/ # Modelos entrenados
├── 📁 reports/ # Reportes y resultados
├── 📁 docs/ # Documentación
└── 📁 images/ # Imágenes del proyecto


## 🛠️ Instalación y Uso

### Requisitos
```bash
pip install -r requirements.txt

Ejecución

    Clonar el repositorio

    Instalar dependencias: pip install -r requirements.txt

    Ejecutar el notebook principal: notebooks/clasificacion_del_clima.ipynb

👨‍💻 Autor

Bruno Saint Martin Padilla

📄 Licencia

Este proyecto es para fines educativos y de investigación.


# 📖 Metodología del Proyecto

## 🎯 Enfoques Comparados

### 1. CNN Personalizada
- Arquitectura diseñada específicamente para el dataset climático
- Entrenamiento desde cero
- Optimizada para velocidad y eficiencia

### 2. ResNet-50 con Fine-tuning
- Arquitectura preentrenada en ImageNet
- Transfer learning aplicado al dominio climático
- Capas fully-connected adaptadas para 3 clases

## ⚙️ Configuración de Entrenamiento

### Hiperparámetros Comunes
- **Optimizador:** Adam
- **Learning Rate:** 0.001
- **Batch Size:** 32
- **Función de Loss:** CrossEntropyLoss

### Estrategias de Regularización
- Data Augmentation
- Early Stopping
- Dropout en capas fully-connected
