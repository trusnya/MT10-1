## Поведение объектов при различных действиях пользователя:

Сайт: https://web.telegram.org/

Созданные обЪекты: 

localStorage.setItem("telegramData", JSON.stringify({username: "exampleUser", chatId: "123456789"}));

sessionStorage.setItem("telegramData2", JSON.stringify({username: "exampleUser2", chatId: "123456789"}));

| Действие | Local Storage | Session Storage |
|-----|----------|---------|
|Обновление страницы| + | + |
|Дублирование вкладки браузера| + | + |
|Восстановление страницы| + | + |
|Закрытии и открытии браузера| + | - |