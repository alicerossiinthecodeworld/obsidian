
  

работа expdate 

статья в конфле есть, добавить

  

Где-то ставят правило, дальше тверские проливают в 

  

  

В продакт сервис

private const int ExpirationDateDays7578 = 7578;

    private const int ExpirationDateDays8205 = 8205;

    private const int ExpirationDateDays5379 = 5379;

  

  

Менять момент в инкам джорнэл

  

  

Мы не берем скуху если ее нет в продакт сервисе

  

129341

  

  

были вопросы к максу

  

Вопросы к Максиму:

  

 1.  как запустить 

  

 **exec** dbo. ItemExpirationDateNeedsLogExemplarExpDateSet

**@id** = 33,

**@itemid** = 345,

**@expiredInterval** = 180,

**@ExemplarBatchSize** = 500

  

Как получить SQL Error [201] [S0004]: Procedure or function 'ItemExpirationDateNeedsLogExemplarExpDateSet' expects parameter '@DocNumber', which was not supplied.

  

1. Как сымитировать таймауты в проце и ошибки в процессе
2. Правильно ли я понимаю что мне достаточно проверить ItemExpirationDateNeedsSetExpDateLog, чтобы понять, какие экземпляры айтема обработались? 
3. Как отрегулировать срок годности в продукт сервис и сом, чтобы проверить, что результаты правильно получаются оттуда? Или должен ставиться текущий день?
4. Как должен определяться срок снятия с полки? 
5. Могу ли я выбрать любой айтем с экземплярами без срока годности? Есть ли запросы?


Теперь если у айтема нет заявку поставщику,  то мы берем 4 накладную/инкам джорнал


[[работа]] #инфоосервисах


Вопросы к Максиму:

  

 1.  как запустить 

  

 **exec** dbo. ItemExpirationDateNeedsLogExemplarExpDateSet

**@id** = 33,

**@itemid** = 345,

**@expiredInterval** = 180,

**@ExemplarBatchSize** = 500

  

Как получить SQL Error [201] [S0004]: Procedure or function 'ItemExpirationDateNeedsLogExemplarExpDateSet' expects parameter '@DocNumber', which was not supplied.

  

1. Как сымитировать таймауты в проце и ошибки в процессе
2. Правильно ли я понимаю что мне достаточно проверить ItemExpirationDateNeedsSetExpDateLog, чтобы понять, какие экземпляры айтема обработались? 
3. Как отрегулировать срок годности в продукт сервис и сом, чтобы проверить, что результаты правильно получаются оттуда? Или должен ставиться текущий день?
4. Как должен определяться срок снятия с полки? 
5. Могу ли я выбрать любой айтем с экземплярами без срока годности? Есть ли запросы?