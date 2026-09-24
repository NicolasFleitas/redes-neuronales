# Redes Neuronales

Repositorio de práctica con redes neuronales sobre MNIST y Fashion-MNIST (TensorFlow / Keras).

## Introducción

Práctica introductoria de redes densas (MLP) para clasificación de imágenes de 28x28.

- **Objetivo:** entrenar la misma red simple (784 → 128 → 10) en dos datasets y comparar qué cambia.
- **Experimentos:** ReLU vs Sigmoid y Adam vs SGD, con los mismos hiperparámetros (5 epochs, batch 128, lr 0.001).
- **Resultado:** la ganadora es ReLU + Adam en ambos casos, con ~97% en MNIST y ~86.6% en Fashion-MNIST. La ropa cuesta más porque las clases se solapan (camisa/remera, suéter/abrigo).
- **Idea clave:** una densa de 1 capa ya resuelve dígitos, pero al aplanar píxeles pierde formas locales; por eso confunde trazos o prendas parecidas, donde una CNN rendiría mejor.

## Requisitos

- Python 3.12
- uv

## Instalación

```bash
uv sync
```

Esto instala las dependencias principales (`jupyter`, `numpy`, `matplotlib`, `tensorflow-cpu`, que incluye Keras) y el grupo `dev` (`nbstripout`).

## Uso

```bash
uv run jupyter notebook
```

Luego abrir el notebook deseado desde el navegador.

## Notebooks

- `notebooks/01-mnist.ipynb`: clasificación de dígitos manuscritos (MNIST).
- `notebooks/02-fashion-mnist.ipynb`: clasificación de prendas de vestir (Fashion-MNIST).

## Notas sobre nbstripout

Los notebooks se guardan sin salidas gracias a `nbstripout` (ver `.gitattributes`).

Esto mantiene el repositorio limpio y evita diffs innecesarios en el historial.
