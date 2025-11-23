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

## 📊 Resultados Obtenidos
- **CNN Personalizado:** 96.45% accuracy
- **ResNet-50:** 94.38% accuracy
- **CNN es 5.3x más rápido** en entrenamiento
