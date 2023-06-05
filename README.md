# Word Embedding   

<p align="justify">
Будем работать с англоязычным датасетом, составленным из рецептов 
</p>

## Модель     

* word2vec (SkipGram)     
* Softmax (с аппроксимацией Negative Sampling)

В моделе SkipGram для каждого слова у нас есть два вектора — первый вектор используется, когда слово находится в центре скользящего окна, и второй вектор используется, когда это слово описывает контекст (т.о. есть две матрицы). Настраивать значения этих матриц методу максимального правдоподобия


##  Универсальные компоненты     

* Токенизация   
* Построение словаря   
* pytorch Dataset    
* Паддинги
* Метод максимального правдоподобия

## Основные функции и классы   

* PaddedSequenceDataset - класс c 2-мя методами:    
    1-ый метод определения сколько предложений в нём есть;    
    2-ой метод возвращения предложение по номеру, так что если предложение короче некоторой заданной длины, то он добавляет нули в конец этого предложения, если предложение длиннее установленного порога, то он его обрезает. Эта функция возвращает пары — а именно "текст" и "какая-то метка", которую по этому тексту нужно предсказывать (если задача классификации).



## Технологии
* [PyTorch](https://pytorch.org/)   
* [pandas](https://pandas.pydata.org/)
* [numpy](https://numpy.org/)
* [matplotlib](https://matplotlib.org/)
