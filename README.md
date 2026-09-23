# Redes Neuronales

Repositorio de práctica con redes neuronales sobre MNIST y Fashion-MNIST (TensorFlow / Keras).

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
