Этот проект может помочь спланировать путешествия тем, что подскажет вам погоду в начальной и конечной точке вашего планируемого путешествия.

   Использование:
Этот сайт максимально прост в использовании, просто введите в поля названия городов и получите ключевые характеристики погоды в них, помните, что принятие решение о поездке всё равно за вами!
При возникновении каки-либо проблем вы будете уведомлены сайтом о том, какая ошибка произошла.


  Какие ошибки были обработаны в рамках проверки работоспособности и каким образом появление ошибки влияет на общую работоспособность системы:
• 1. HTTPError
Описание: Эта ошибка возникает, когда сервер возвращает код состояния HTTP, указывающий на ошибку (например, 404 - не найдено или 500 - ошибка сервера).
Обработка: При возникновении ошибки HTTP приложение логгирует сообщение об ошибке с указанием города и детали ошибки. Пользователю возвращается сообщение о том, что данные не могут быть получены.
Влияние на систему: Это предотвращает крах приложения и помогает пользователю понять, что запрос не удался.

• 2. ConnectionError
Описание: Эта ошибка возникает, когда приложение не может установить соединение с сервером API.
Обработка: В случае возникновения этой ошибки приложение логгирует информацию о проблеме с соединением и уведомляет пользователя о недоступности сервиса.
Влияние на систему: Пользователь получает информацию о проблемах с сетью, что помогает ему понять, что проблема может быть временной.

• 3. Timeout
Описание: Тайм-аут возникает, если запрос к API занимает слишком много времени.
Обработка: При возникновении тайм-аута приложение логгирует ошибку и уведомляет пользователя о том, что запрос занял слишком много времени.
Влияние на систему: Это позволяет пользователю понять, что запрос может быть задержан, и предлагает попробовать позже.

• 4. RequestException
Описание: Это общее исключение для всех других ошибок, связанных с запросами.
Обработка: При возникновении этой ошибки приложение логгирует информацию о ней и возвращает пользователю общее сообщение об ошибке.
Влияние на систему: Это обеспечивает дополнительный уровень защиты от неожиданных сбоев и помогает поддерживать стабильность приложения.
Общая работоспособность системы
Обработка ошибок является критически важной для обеспечения стабильной работы приложения. Каждая из вышеописанных ошибок может привести к сбоям в получении данных о погоде, что непосредственно влияет на пользовательский опыт. Логирование ошибок позволяет разработчикам отслеживать проблемы и улучшать приложение в будущем.