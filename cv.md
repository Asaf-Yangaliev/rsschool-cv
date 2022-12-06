# Yangaliev Asaf Rustamovich
![Изображение отсуствует](images/asafyangaliev.jpeg)
## **Контакты для связи:**
**Phone number**: +998 (90) 178-72-80 \
**Email**: asafyang1995@gmail.com \
**Telegram**: Asaf_Yangaliev
## **Образование:**
>Филиал РГУ нефти и газа (НИУ) имени И.М.Губкина в г. Ташкенте
## **Опыт работы:**
>**Период:** ноябрь 2018 - июль 2019 \
>**Кампания:** Enter Engineering \
>**Должность:** Специалист по планированию и отчетности

>**Период:** июль 2019 - сентябрь 2021 \
>**Место работы:** Учебный Центр Bunker Lab \
>**Должность:** Учитель математики

>**Период:** сентябрь 2019 - апрель 2022 \
>**Кампания:** Fido Bizness \
>**Должность:** Java Developer

>**Период:** май 2019 - н.в. \
>**Кампания:** Epam Systems \
>**Должность:** Java Developer

## **Достижения:**
>2016 - Победа на Губкинской олимпиаде по математике, 4 место в финале Республиканской олимпиады по математике \
>2017 - 2 место на Губкинской олимпиаде по математике

## **Навыки:**
* Java Core
* Spring
* Spring Boot
* Rest API
* SQL
* Kafka
* AWS
* HTML/CSS/JavaScript
* Git
* Languages:
  * Russian - Native
  * English - B1
  * Spanish - A1
## Пример кода:
> Метод, который стирает смайлики в строке (":-)", ":-(")\
("ew:-)))dl:-(((dsff") -> "ewdldsff" \
("wqeqwe:-)):-((") -> "wqeqwe"
```Java
    public static String eraseString(String s) {
        if (s == null) {
            throw new IllegalArgumentException("parameter must not be null");
        }
        int begin = 0;
        StringBuilder sb = new StringBuilder();
        while (true) {
            int index = getMinIndex(s.indexOf(":-)", begin), s.indexOf(":-(", begin));
            if (index == -1) {
                sb.append(s, begin, s.length());
                break;
            }
            sb.append(s, begin, index);
            index += 2;
            char c = s.charAt(index);
            while (index < s.length() && c == s.charAt(index)) {
                index++;
            }
            begin = index;
        }
        return sb.toString();
    }

    private static int getMinIndex(int index1, int index2) {
        if (index1 == -1 && index2 == -1)
            return -1;
        else if (index1 == -1)
            return index2;
        else if (index2 == -1)
            return index1;
        else
            return Math.min(index1, index2);
    }
```