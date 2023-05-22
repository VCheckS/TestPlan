# 1. Перечень сценарий навигации к форме

## 2.1 Загрузка страницы https://netology.ru/#/ с формой записи.

## 2.2 Переход к форме записи одним из способов

### 2.2.1 Переход с главной странице через ячейку "Програмирование"

#### - Кликаем на ячейку "Программирование"

#### - Находим в списке курс "Тестировщик ПО", выполнияем клик по данной ячейке

#### - Выполняем клик по ячейке "Записаться" в самом начале стриници

#### - Либо Прокручиваем странице до самого конце и заполняем форму записи внизу

### 2.2.2 Переход с главной страници через каталог курсов

#### - Кликаем на кнопку "Каталог курсов"

#### - Кликаем по ячейке "Все курсы"

#### - Прокручиваем страницу, находим курс "Тестировщик ПО"

#### - Выполняем клик по ячейке "Тестировщик ПО"

#### - Выполняем клик по ячейке "Записаться" в самом начале стриници

#### - Либо Прокручиваем странице до самого конце и заполняем форму записи внизу

# 2. Перечень автоматизируемых сценариев:

### 2.1 Позитивные тестовые сценарии:

#### 2.1.1 Заполнение формы валидными значениями и проверка функциональности кнопок:

    -Ввести валидные данные в поле "Имя", например "Василий";
    -Ввести валидные значения в поле "Телефон", например "+79849652590";
    -Ввести валидные данные в поле "Email", например mailbox@mail.com;
    -Кликаем на кнопку "Записаться"/ кликаем на кнопку "Получить консальтацию".

##### <i>-Ожидаемый результат :  Форма успешно отправляется, и пользователь переходит на страницу оплаты курса / пользователь получает оповещение о том что с ним свяжется специалист

### 2.2 Негативные тестовые сценарии:

#### 2.2.1 Отправка формы с незаполненными обязательными полями:

    Оставлем все или некоторые поля пустыми поочередно, нажимаем на кнопку "Записаться"

##### <i>-Ожидаемый результат :Система выдает сообщения об ошибках для незаполненных обязательных полей и не позволяет отправить форму до их заполнения.

#### 2.2.2 Ввод не валиданых значений:

    -Ввод в поле "Имя" специальные знаки и цифры, например #3424##@
    -В поле "телефон" ввести валидные данные например "+79999999999"
    -В поле "email" ввести валидные данные, например mailbox@mail.ru

##### <i>-Ожидаемый результат : система оповещает об не корректном заполнении поля "Имя" и не дает отправить заявку до исправления поля

    -Ввод в поле "Телефон" буквы и специальные знаки, либо неверный формат телефона, например #2324fgdgt, или +2314118687766
    -Ввести валидные данные в поле "Имя", например "Василий";
    -В поле "email" ввести валидные данные, например mailbox@mail.ru

##### <i>-Ожидаемый результат : система оповещает об не корректном заполнении поля "Телефон" и не дает отправить заявку до исправления поля

    -В поле "телефон" ввести валидные данные например "+79999999999"
    -Ввести валидные данные в поле "Имя", например "Василий";
    -Ввод в поле "Email" строку без знака "@", например mailbox.ru

##### <i>-Ожидаемый результат : система оповещает об не корректном заполнении поля "Email" и не дает отправить заявку до исправления поля

### 2.2.3 Проверка защиты от нежелательного ввода:

    Пример:  ввести специальные символы "<script>alert('Hello!');</script>" в поле "Имя".

#### <i>-Ожидаемый результат: Система экранирует или отфильтровывает специальные символы и принимает только допустимый текст в поле "Имя".

### 2.2.4 Проверка ограничений на поля:

    Пример: ввести текст длиннее максимально допустимой длины в поле "Имя".

##### <i>-Ожидаемый результат: Система выдает сообщение об ошибке для поля "Имя" (например, "Превышена максимальная длина Имени") и не позволяет отправить форму до исправления ошибки.

### 2.2.5 Обработка ошибок:

##### <i>Ожидаемый результат: При возникновении ошибок при отправке формы, например, проблем с соединением или сервером, система выдает соответствующее сообщение об ошибке и предоставляет пользователю информацию о проблеме или возможность повторной отправки формы.

# 3. Перечень используемых инструментов с обоснованием выбора:

## 3.1 Selenide: для автоматизации веб-интерфейса и выполнения действий на странице.

## 3.2 JUnit: для создания и организации тестовых сценариев и управления тестовыми данными.

## 3.3 Gragle: для управления зависимостями и сборки проекта.

## 3.4 Git: для управления версиями и совместной работы над кодом.

## 3.5 IntelliJ IDEA: для разработки и отладки автоматизированных тестов.

# 4. Перечень необходимых разрешений, данных и доступов:

## 4.1 Разрешение для тестирования сайта.

## 4.2 Доступ к базе данных для получения подтверждения верности отправленных в форме данных.

## 4.3 Доступ к исходному коду приложения или веб-страницы для идентификации элементов и взаимодействия с ними.

## 4.4 Тестовые данные для заполнения формы (например, тестовые учетные записи, данные пользователя).

# 5. Перечень и описание возможных рисков при автоматизации:

## 5.1 Изменение структуры или идентификаторов элементов на странице, что может привести к нарушению работы автоматизированных тестов.

## 5.2 Необходимость обновления тестовых данных при изменении требований или логики формы.

## 5.3 Проблемы совместимости с браузерами или устройствами, которые могут привести к непредсказуемому поведению тестов.

# 6. Перечень необходимых специалистов для автоматизации:

## 6.1 QA-инженер с опытом автоматизации тестирования и знанием выбранных инструментов.

7. Интервальная оценка с учетом рисков в часах:

## 7.1 Загрузка страницы с формой записи: 1 час.

## 7.2 Переход к форме записи: 1 час.

## 7.3 Заполнение обязательных полей формы: 4 часа.

## 7.4 Проверка валидации введенных данных: 2 часа.