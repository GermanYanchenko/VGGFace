# Модель предсказания пола, расы и возраста лиц людей.
Данные для обучения модели https://susanqq.github.io/UTKFace/. Датасет состоит из 20000 фотографий лиц людей в возрасте от 0 до 116 лет. В качестве разметки имеется пол (male/female), раса (white/black/asian/indian/other) и возраст. Пример изображений: <br>
![alt text](https://github.com/GermanYanchenko/VGGFace/blob/main/images/dataset.png?raw=true)<br>
За основу была взята сеть VGGFace https://github.com/rcmalli/keras-vggface.<br>
Используя подход Multitask learning выполняем три параллельных выхода модели, для предсказания пола, расы и возраста. Оптимизатором модели
является Adam. Лосс-фукнция и метрика качества: Пол - бинарная кросс-энтропия/точность, Раса - sparse_categorical_crossentropy/ точность, Возраст - MSE/MAE.<br>
История обучения представлена ниже: <br>
![alt text](https://github.com/GermanYanchenko/VGGFace/blob/main/images/hist1.png?raw=true)<br>
![alt text](https://github.com/GermanYanchenko/VGGFace/blob/main/images/hist2.png?raw=true)<br>
![alt text](https://github.com/GermanYanchenko/VGGFace/blob/main/images/hist3.png?raw=true)<br>
Пример предсказания полученной модели на тестовом датасете: <br>
![alt text](https://github.com/GermanYanchenko/VGGFace/blob/main/images/predict.png?raw=true)<br>
И предсказание модели меня. Реальный возраст - 27 лет.<br>
![alt text](https://github.com/GermanYanchenko/VGGFace/blob/main/images/predict1.png?raw=true)
![alt text](https://github.com/GermanYanchenko/VGGFace/blob/main/images/predict2.png?raw=true)<br>
