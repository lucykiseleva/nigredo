# Полезные функции JavaScript

[Ссылка на оригинал](http://artemdemo.me/blog/%D0%BF%D0%BE%D0%BB%D0%B5%D0%B7%D0%BD%D1%8B%D0%B5-%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%B8-%D0%B2-javascript/)

## Debounce
устранение дребезга

В JS есть много функций которые вызываются с большой частотой, например scroll, resize. Каждый раз прогонять в них сложную логику не правильно – это ведет к замедлению работы браузере, да и вообще портит карму :] Я уже не говорю о тех случаях, когда на часто вызываемой функции лежит еще и обращение к серверу. Это вообще отдельный ад.

## Poll – пробуем достучаться

В связи с асинхронностью JS бывают случаи когда требуемый функционал не готов к использованию и мы не можем точно определить временной промежуток требуемый для этого. В этом случае хотелось бы провести несколько проверок с интервалом для того, что бы точно знать когда все готово.

## Once – только однажды

Не все функции должны вызываться несколько раз. Давайте рассмотрим как сделать функцию, которая будет вызвана только один раз, после чего прекратит свое существование

## Микропаттерны оптимизации в Javascript
декораторы функций [debouncing и throttling](http://m.habrahabr.ru/post/60957/)


# Семь полезных техник JavaScript

[Оригинал статьи](http://designformasters.info/posts/seven-javascript-techniques/)

1. Разделяйте если это возможно.

Если важна производительность, очень полезно разделять ваши функции таким образом, чтобы действия, сильно загружающие процессор или требующие много памяти, не повторялись часто. Одна из распространенных ситуаций, когда возникает такая необходимость, это обработка различий браузеров


2. Используйте флаги

Использование флагов это еще один способ ускорения детекции объектов. Если в нескольких функциях проверяется наличие, какого либо объекта, просто используйте соответствующий флаг. Например, если проверяется поддержка браузером наиболее распространенные операции DOM, стоит использовать флаг отражающий этот факт:

var w3 = !!(document.getElementById && document.createElement);

3. Используйте «мосты»

Мост2 это паттерн, используемый в разработке программного обеспечения для «разделения абстракции и ее реализации так чтобы они могли изменяться независимо». Мосты особенно полезны в управляемом событиями программировании. 


4. Попробуйте делегацию событий
Делегация событий это простой способ сэкономить на назначении обработчиков событий. Она работает с помощью назначения обработчика событий к элементу контейнеру, и уточнения элемента с которым произошло событие в обработчике, вместо назначения нескольких обработчиков к каждому дочернему элементу и доступа к элементам через объект thi

5. Используйте callback функции

Одно из наиболее примечательных упущений всех JavaScript библиотек, это отсутствие возможности использовать callback, для функций коллекторов элементов. Будь то getElementsByClassName, getElementsByAttribute, или даже функции, использующие CSS селекторы, логично иметь возможность задать callback функцию.

Делегация событий это простой способ сэкономить на назначении обработчиков событий. Она работает с помощью назначения обработчика событий к элементу контейнеру, и уточнения элемента с которым произошло событие в обработчике, вместо назначения нескольких обработчиков к каждому дочернему элементу и доступа к элементам через объект this

6. Используйте инкапсуляцию

Это старая, но редко используемая практика. Если вы разрабатываете JavaScript, который становиться большим и неуправляемым (а это случается с каждым, поверьте мне), самый надежный способ защитить ваш код и сохранить его совместимым с другими библиотеками, это использовать замыкание. 



7. Изобретайте колесо.

Последнее, но не менее важное, изобретайте колесо

Часто когда я проектирую код или делаю элемент управления, я почти уверен, что кто-то уже сделал это, тем не менее, я стараюсь проверить могу ли я сделать лучше. Не каждое колесо круглое, и не каждое круглое колесо имеет двадцати дюймовые блестящие диски. Воображение и такой гибкий язык может далеко вас увести.