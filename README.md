# Clasificador de productos para inventario

Web que usa la cámara para reconocer productos de supermercado, indica su **sección** y **producto**, y permite ir llenando un inventario (descargable en CSV).

- `index.html`: cámara (o subir foto) + inventario por secciones guardado en el navegador.
- `prueba.html`: prueba del modelo con fotos de ejemplo (`muestras/`).
- `model.json` + `group1-shard*.bin` + `clases.json`: modelo TensorFlow.js (MobileNetV2 + capa de clasificación, 63 productos en 7 secciones).
- `Clasificador_de_productos_inventario.ipynb`: notebook de entrenamiento (descarga los datasets, entrena, evalúa y exporta a TensorFlow.js).
- `requirements.txt`: librerías para ejecutar el notebook en local.

Secciones: Frutas, Verduras, Lácteos, Bebidas, Snacks y dulces, Despensa, Conservas.

Datasets: [Freiburg Groceries](http://aisdatasets.informatik.uni-freiburg.de/freiburg_groceries_dataset/) y [Grocery Store Dataset](https://github.com/marcusklasson/GroceryStoreDataset).
Precisión en imágenes de prueba: 85% en producto, 92% en sección.
