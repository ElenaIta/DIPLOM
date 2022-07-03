#**План автоматизации**

####Исходные данные:
* APPROVED - 4444 4444 4444 4441;
* DECLINED - 4444 4444 4444 4442.



##Перечень автоматизируемых сценариев:
###**Позитивные сценарии:**

  **1. Оплата картой:**

  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - в появившихся полях ввести валидные данные
  - кликнуть кнопку "Продолжить"
  
    **Ожидаемый результат:**
    - данные успешно отправлены и могут быть просмотрены в соответствующей базе данных;
    - появится всплывающее окно об одобрении операции банком.

  **2. Покупка в кредит:**

  - открыть страницу покупки тура
  - кликнуть кнопку "Купить в кредит"
  - в появившихся полях ввести валидные данные
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** данные успешно отправлены; появится всплывающее окно об одобрении операции банком.


###**Негативные сценарии:**
  **1. Пустая форма:**

  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - кликнуть кнопку "Продолжить"
   
    **Ожидаемый результат:**
  - данные не отправлены;
  - под полем "Номер карты" появится сообщение Неверный формат;
  - под полем "Месяц" появится сообщение Неверный формат;
  - под полем "Год" появится сообщение Неверный формат;
  - под полем "Владелец" появится сообщение Поле обязательно для заполнения;
  - под полем "CVC/CVV" появится сообщение Неверный формат.
***
**2. Поле "Номер карты":**

**2.1.**
  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - поле "Номер карты" оставить пустым, остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"
   
    **Ожидаемый результат:** данные не отправлены; под полем "Номер карты" появится сообщение Неверный формат.

**2.2.**
  - открыть страницу покупки тура 
  - кликнуть кнопку "Купить" (оплата картой)
  - в поле "Номер карты" ввести не полный номер (4444 4444 4444 444), остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить";

    **Ожидаемый результат:** - данные не отправлены; под полем "Номер карты" появится сообщение Неверный формат.


**2.3.**
  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - в поле "Номер карты" ввести не валидный номер, остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** данные успешно отправлены; появится всплывающее окно об отказе в проведении операции банком.
***
**3. Поле "Месяц":**

**3.1.**
  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - поле "Месяц" оставить пустым, остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** данные не отправлены; под полем "Месяц" появится сообщение Неверный формат.

**3.2.**
  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - в поле "Месяц" ввести не валидный месяц (в пределах 01-12), остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** - данные не отправлены; под полем "Месяц" появится сообщение Неверно указан срок действия карты.

**3.3.**
  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - в поле "Месяц" ввести не валидный месяц (нижнее граничное значение 00), остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** данные не отправлены; под полем "Месяц" появится сообщение Неверно указан срок действия карты.

**3.4.**
  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - в поле "Месяц" ввести не валидный месяц (верхнее граничное значение 13), остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** данные не отправлены; под полем "Месяц" появится сообщение Неверно указан срок действия карты.
    
***
**4. Поле "Год":**

**4.1.**
  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - поле "Год" оставить пустым, остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** данные не отправлены; под полем "Год" появится сообщение Неверный формат.

**4.2.**
  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой) 
  - в поле "Год" ввести не валидный год (текущий год - 1), остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** данные не отправлены; под полем "Год" появится сообщение Истёк срок действия карты.

**4.3.**
  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой) 
  - в поле "Год" ввести не валидный год (текущий год + 6), остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** данные не отправлены; под полем "Год" появится сообщение Неверно указан срок действия карты.
    
***
**5. Поле "Владелец":**

**5.1.**
  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - поле "Владелец" оставить пустым, остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** данные не отправлены; под полем "Владелец" появится сообщение Поле обязательно для заполнения.

**5.2.**
  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой) 
  - в поле "Владелец" ввести " "(пробел), остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"
 
    **Ожидаемый результат:** данные не отправлены; под полем "Владелец" появится сообщение Поле обязательно для заполнения.

**5.3.**

  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - в поле "Владелец" ввести #&(два любых спецсимвола), остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожижаемый результат:** данные не отправлены; под полем "Владелец" появится сообщение Неверный формат имени владельца.

**5.4.**

  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой) 
  - в поле "Владелец" ввести двузначное число(10-99), остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** данные не отправлены; под полем "Владелец" появится сообщение Неверный формат имени владельца.
***
**6. Поле "CVC/CVV":**

**6.1.**

  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - поле "CVC/CVV" оставить пустым, остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

     **Ожидаемый результат:** данные не отправлены; под полем "CVC/CVV" появится сообщение Неверный формат.

**6.2.**

  - открыть страницу покупки тура
  - кликнуть кнопку "Купить" (оплата картой)
  - в поле "CVC/CVV" ввести двузначное число(10-99), остальные поля заполнить валидными данными
  - кликнуть кнопку "Продолжить"

    **Ожидаемый результат:** данные не отправлены; под полем "CVC/CVV" появится сообщение Неверный формат.
***
  
**7. Аналогичные негативные сценарии для покупки в кредит.**

***
##Перечень используемых инструментов с обоснованием выбора:

- JDK 11 - т.к. будет использоваться Java;
- IntelliJ IDEA - удобная среда подготовки авто-тестов;
- Gradle - инструмент управления зависимостями;
- DBeaver - для просмотра базы данных; 
- JUnit Jupiter - инструмент тестирования, более превычен нежели JUnit4 или TestNG;
- Selenide - удобен при тестировании веб-интерфейса;
- MySQL connector Java, PostgreSQL и Commons DBUtils - для доступа к базе данным из кода авто-тестов;
- Lombok - для упрощения написания кода;
- Faker - для генерации данных при отправке формы;
- Github - в качестве хранилища SUT и авто-тестов;
- Allure - для создания отчетов о выполнении авто-тестов;
- Allure-Selenide - для интеграции одного инструмента с другим.
***

##Перечень и описание возможных рисков при автоматизации:

- своеобразная настройка SUT при запуске (заявлена поддержка двух СУБД);
- отсутствие как таковой спецификации на приложение;
- необходимость добавления новых тестов для заказчика, при отсутствии документации и спецификации на приложение;
- зависимость авто-тестов от текущей реализации веб-элементов, даже не значительное их изменение может привести к падению авто-тестов;
- авто-тесты не проверяют графическую составляющую, а именно едет ли верстка при тех или иных действиях, комфортна ли выбранная цветовая схема оформления и тд.
***

##Интервальная оценка с учётом рисков (в часах):
Ориентировочно, 120 рабочих часов.

***

##План сдачи работ

- Написание тестов до 25 июля 2022;
- Предоставление отчетов до 05 августа 2022: