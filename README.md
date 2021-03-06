# Курсовая работа. Потоки в сетях. Вариант 2

## Потоки в сетях

Сетью называется орграф без петель с помеченными вершинами и дугами. Числа, которыми
помечаются дуги сети, называются пропускными способностями дуг.

Примеры вершин сети:
перекрёстки дорог, телефонные узлы, железнодорожные узлы, аэропорты, склады и т.д.
Примеры дуг сети:
дороги, трубы, телефонные и железнодорожные линии и т.д.

Сеть, у которой существует ровно один исток (`s`) и один сток (`t`), называется [транспортной сетью][1].

### Пример:

Максимальный поток в транспортной сети с источником `s` и стоком `t`.
Числа обозначают потоки и пропускные способности.
Первое число означает величину потока, второе — пропускную способность ребра.

![Пример транспортной сети](assets/example.png "Пример транспортной сети")

В теории оптимизации и теории графов, [задача о максимальном потоке][2] заключается в
нахождении такого потока по транспортной сети, что сумма потоков из истока, или, что то же
самое, сумма потоков в сток максимальна.

## Задание.

Входные данные: текстовый файлы со строками в формате `V1`, `V1`, `P`,
где `V1`, `V2` направленная дуга транспортной сети, а
`P` – ее пропускная способность.
Исток всегда обозначен как `S`, сток – как `T`

Пример файла для сети с изображения выше:

```
S O 3
S P 3
O Q 3
O P 2
P R 2
Q R 4
Q T 2
R T 3
```

Найти максимальный поток в сети используя алгоритм:

Вариант 1. [Форда — Фалкерсона][3]

Вариант 2. [Эдмондса — Карпа][4]


[//]: # (Links)

[1]: https://ru.wikipedia.org/wiki/%D0%A2%D1%80%D0%B0%D0%BD%D1%81%D0%BF%D0%BE%D1%80%D1%82%D0%BD%D0%B0%D1%8F_%D1%81%D0%B5%D1%82%D1%8C
[2]: https://ru.wikipedia.org/wiki/%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0_%D0%BE_%D0%BC%D0%B0%D0%BA%D1%81%D0%B8%D0%BC%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%BC_%D0%BF%D0%BE%D1%82%D0%BE%D0%BA%D0%B5
[3]: https://ru.wikipedia.org/wiki/%D0%90%D0%BB%D0%B3%D0%BE%D1%80%D0%B8%D1%82%D0%BC_%D0%A4%D0%BE%D1%80%D0%B4%D0%B0_%E2%80%94_%D0%A4%D0%B0%D0%BB%D0%BA%D0%B5%D1%80%D1%81%D0%BE%D0%BD%D0%B0
[4]: https://ru.wikipedia.org/wiki/%D0%90%D0%BB%D0%B3%D0%BE%D1%80%D0%B8%D1%82%D0%BC_%D0%AD%D0%B4%D0%BC%D0%BE%D0%BD%D0%B4%D1%81%D0%B0_%E2%80%94_%D0%9A%D0%B0%D1%80%D0%BF%D0%B0