## Laboratory work III

Данная лабораторная работа посвещена изучению систем автоматизации сборки проекта на примере **CMake**



## Homework

Представьте, что вы стажер в компании "Formatter Inc.".
### Задание 1
Вам поручили перейти на систему автоматизированной сборки **CMake**.
Исходные файлы находятся в директории [formatter_lib](formatter_lib).
В этой директории находятся файлы для статической библиотеки *formatter*.
Создайте `CMakeList.txt` в директории [formatter_lib](formatter_lib),
с помощью которого можно будет собирать статическую библиотеку *formatter*.

1)
![изображение](https://user-images.githubusercontent.com/92674699/159633563-79059ea2-732f-4a3b-8ebb-732ec7ea4186.png)

2)
![изображение](https://user-images.githubusercontent.com/92674699/159633295-0cd3036f-5c2c-4c3c-8d63-c544bc61d280.png)

3)
![изображение](https://user-images.githubusercontent.com/92674699/159633378-5211ebd1-e250-41e4-b55c-dd8d6276d76f.png)

4)
![изображение](https://user-images.githubusercontent.com/92674699/159634004-a730d317-1c5d-482b-a7eb-f7cf34f3903b.png)


### Задание 2
У компании "Formatter Inc." есть перспективная библиотека,
которая является расширением предыдущей библиотеки. Т.к. вы уже овладели
навыком созданием `CMakeList.txt` для статической библиотеки *formatter*, ваш 
руководитель поручает заняться созданием `CMakeList.txt` для библиотеки 
*formatter_ex*, которая в свою очередь использует библиотеку *formatter*.

1)
file:///home/dmitry/%D0%98%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202022-03-23%2009-05-03.png![изображение](https://user-images.githubusercontent.com/92674699/159634348-20d547cb-95c2-4a0e-be3f-3a490df935a3.png)


2)
![изображение](https://user-images.githubusercontent.com/92674699/159635390-072197d0-319b-4c76-b13b-e8dd6d5f9e39.png)


### Задание 3
Конечно же ваша компания предоставляет примеры использования своих библиотек.
Чтобы продемонстрировать как работать с библиотекой *formatter_ex*,
вам необходимо создать два `CMakeList.txt` для двух простых приложений:
* *hello_world*, которое использует библиотеку *formatter_ex*;
* *solver*, приложение которое испольует статические библиотеки *formatter_ex* и *solver_lib*.

