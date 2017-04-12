***Отчет о проделанной иследовательской работе.***
-----------------------------------
Установка Docker machine через DockerToolbox.
-----------------------------------
При попытке установки Docker machine на Windows 10 встречаем ошибку сообщающую, что установить docker на window 10 home невозможно без
DockerToolbox

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_19-57-37.png)

Для установки Docker machine необхадимо скачать оффициальную программу [DockerToolbox](https://www.docker.com/products/docker-toolbox),
так же необхадимо заранее зарегестрироваться на [офффициальном сайте](https://www.docker.com/) 

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-10-10.png)

Выбрав необхадимую ОС, и дождавшийся загрузки программы, необхадимо установить ее используя следующие настройки,
если какое то ПО уже стоит можно не ставить( в моем случаее git у меня есть)

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-07-52.png)

Выбираем необхадимые настройки для создания ярлыков на рабочем столе и обнавления драйвера для VB (VirtualBox)

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-08-01.png)

Дождавшийся установки программы и настройки docker machine в VB запускаем Kitematic,
при первом входе нас попросят авторизоваться.

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-21-53.png)

Далее у нас уже есть установленный docker на VB названный default 

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-25-42.png)

Kitematic - простая программа для запуска контейнеров через, мощный графический пользовательский интерфейс.

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-05-47.png)

Следующие команды это лишь несколько способов , чтобы экспериментировать с docker на вашей системе, проверить информацию о версии, и 
убедитесь , что docker команды работают должным образом.

Запустим docker машину

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-26-32.png)

Вот вывод **docker ps**.

В этом примере, никакие контейнеры не работают.

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-59-55.png)

Ниже приведен пример вывода команды для **docker version**.

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-49-38.png)

Как видно из изображения, клиент OS - Windows 64-разрядный, а сервер linux 64- разрядный.

Ниже приведен пример вывода команды для **docker info**.

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-53-55.png)

На этом изображении приведена подробная информация о клиенте и сервере, их версии и т.п.

Выполним , **docker run hello-world**, для загрузки образа из Docker Hub и запуска контейнера.

![Image alt]()

Запустим контейнер Ubuntu с этой командой: **docker run -it ubuntu bash**

Эта команда загрузит **ubuntu** контейнер и запустит его.

![Image alt]()


