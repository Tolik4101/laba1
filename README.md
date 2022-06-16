Задание 1 
Скачаем библиотеку *boost*:
`wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`
![screen 1](screen 1.png)

Задание 2
Разархивируем скачанный архив:
`tar -xvf boost_1_69_0.tar.gz`
![screen 2](screen 2.png)

Задание 3 
Подчитаем количество файлов в директории, не включая вложенные:
`tree -L 1`
![screen 3](screen 3.png)

Задание 4
Подсчитаем вложенные файлы:
`tree`
![screen 4](screen 4.png)

Задание 5
Подсчитаем количество звголовочных файлов с расширениями: cpp, h, hpp и остальные
`find ~/laba1/boost_1_69_0 -name "*.cpp" | wc -l && find ~/laba1/boost_1_69_0 -name "*.h" | wc -l && find ~/laba1/boost_1_69_0 -name "*.hpp" | wc -l`
![screen 6](screen 6.png)
![screen 7](screen 7.png)

Задание 6 
Найдем полный путь до файлов с названием any.hpp
`find ~/laba1/boost_1_69_0 -name "any.hpp"`
![screen 8](screen 8.png)

Задание 7
Выведем в консоль все файлы, где упоминается boost::asio
`find ~/laba1/boost_1_69_0 -type f | xargs grep -i boost::asio`
![screen 9](screen 9.png)

Задание 8
Скомпилируем boost
![screen 10](screen 10.png)

Задание 9 
Перенесем все скомпилированные в предыдущем шаге библиотеки
`mv boost ~/boost-libs`
![screen 11](screen 11.png)

Задание 10
Подсчитаем сколько дискового простанства занимает каждый файл
`ncdu ~/boost-libs/share`
![screen 12](screen 12.png)

Задание 11
Найдем 10 самых тяжелых файлов
`find ~/boost-libs/share/boost-build/src/tools -type f -exec du -h {} +|sort -rh | head -n 10`
![screen 13](screen 13.png)
![screen 14](screen 14.png)
