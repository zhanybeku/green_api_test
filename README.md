# green_api_test

### Russian:

Страница на языке HTML, позволяющая отправлять текстовые сообщения и файлы через URL с помощью инстанса Green API.  
Для работы со страницей необходимо:

1. Установить приложение WhatsApp.
2. Зарегистрироваться на сервисе Green API.
3. Создать инстанс через консоль Green API.
4. Открыть страницу и ввести необходимые данные.
5. Получить вывод ответа HTTP методов.

Использованные методы Green API, помещенные в соответствующие JavaScript функции в `<script>` элементе HTML страницы:
- **getSettings** - GET
- **getStateInstance** - GET
- **sendMessage** - POST
    - ```javascript
        const payload = {
          chatId: `${phoneNumber}@c.us`,
          message: message,
        };
      ```
      - Данные `payload` получаются через соответствующие поля, заполняемые пользователем.
- **sendFileByUrl** - POST
    - ```javascript
        const payload = {
          chatId: `${phoneNumber}@c.us`,
          urlFile: mediaUrl,
          fileName: fileName,
          caption: "",
        };
      ```
      - Данные `payload` получаются через соответствующие поля, заполняемые пользователем.
      - `fileName` формируется посредством разделения URL по символу `/` и выбора последнего полученного элемента.
      - `caption` оставлен пустым ввиду отсутствия отведенного на него поля в предоставленном макете.

### English:
