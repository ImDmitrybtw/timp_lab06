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

cmake_minimum_required указывает минимальную версию Cmake

set(CMAKE_CXX_STANDARD 11),set(CMAKE_CXX_STANDARD_REQUIRED ON) устанавливают значения стандартных переменных в Cmake(в данном случае CMAKE_CXX_STANDARD и CMAKE_CXX_STANDARD_REQUIRED)

project(formatter) создает проект formatter, к которому можно подключать исполняемы файлы и библиотеки

add_library(formatter STATIC formatter.cpp) создает статическую библиотеку из указываемых файлов.

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
![изображение](https://user-images.githubusercontent.com/92674699/159644341-f11c51bb-cbb6-41ca-a577-487aba8e4d3a.png)

2)
![изображение](https://user-images.githubusercontent.com/92674699/159635390-072197d0-319b-4c76-b13b-e8dd6d5f9e39.png)


### Задание 3
Конечно же ваша компания предоставляет примеры использования своих библиотек.
Чтобы продемонстрировать как работать с библиотекой *formatter_ex*,
вам необходимо создать два `CMakeList.txt` для двух простых приложений:
* *hello_world*, которое использует библиотеку *formatter_ex*;
* *solver*, приложение которое испольует статические библиотеки *formatter_ex* и *solver_lib*.

