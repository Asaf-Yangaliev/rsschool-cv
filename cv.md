# Yangaliev Asaf Rustamovich
![No Image](images/asafyangaliev.jpegg)
## **Personal Information:**
  * **Date of birth**: 11-08-1995
  * **Place of birth**: Tashkent, Uzbekistan
  * **Communication:**
    *  **Phone number**: +998 (90) 178-72-80
    * **Email address**: asafyang1995@gmail.com
    * **Telegram**: Asaf_Yangaliev
## **Education:**
>The Branch of the Russian State University of Oil and Gas (National Research University) named after Ivan Mikhaylovich Gubkin in Tashkent \
Bachelor
## **Employment history:**
>**Period:** November 2018 - Jule 2019 \
>**Company:** Enter Engineering \
>**Position:** Planning and reporting specialist

>**Period:** Jule 2019 - September 2021 \
>**Company:** Learning Center Bunker Lab \
>**Position:** Math Teacher

>**Period:** September 2021 - April 2022 \
>**Company:** Fido Bizness \
>**Position:** Java Developer

>**Period:** May 2022 - Current \
>**Company:** Epam Systems \
>**Position:** Java Developer

## **Skills:**
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
  * Russian - native
  * English - B1
  * Spanish - A1
## Code Example:
> Method, which erases emoticons from the string (":-)", ":-(")\
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