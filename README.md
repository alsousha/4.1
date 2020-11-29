# java4.1-Мили (модернизация)


Авиаперевозчики предлагают различные бонусные программы, начисляющие бесплатные мили за перелёты.

Формула следующая: за каждые 20 рублей, потраченные на билет, начисляется 1 миля.

Проект рассчитывает **количество начисленных мили** за купленный билет и содержит:

1. Класс **BonusMilesService** с методом calculate, который:

    * принимает на вход один параметр: cost типа int
  
    * возвращает рассчитанное количество миль (тип - int)
    
    * код программы:
    
```java

public class BonusMilesService {
    public int calculate(int cost){
        int bonus = 20;
        return cost/bonus;
    }
}

```

2. Класс **Main**, который содержит следующий код:

```java
public class Main {
    public static void main(String[] args) {
        BonusMilesService service = new BonusMilesService();
        int price = 10_000;
        int miles = service.calculate(price);
        System.out.println(miles);
    }
}
```
