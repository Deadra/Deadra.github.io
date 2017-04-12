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

Kitematic - простая программа для запуска контейнеров через, мощный графический пользовательский интерфейс.

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-05-47.png)

У нас уже есть установленный docker на VB названный default 

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-25-42.png)

Следующие команды это лишь несколько способов , чтобы экспериментировать с docker на вашей системе, проверить информацию о версии, и 
убедитесь , что docker команды работают должным образом.

Запустим docker машину

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-26-32.png)

Введем команду **docker ps** и посмотрим результат:

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-59-55.png)

Видно, что в этом примере, никакие контейнеры не работают.

Ниже приведен пример вывода команды для **docker version**.

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-49-38.png)

Как видно из изображения, клиент OS - Windows 64-разрядный, а сервер linux 64- разрядный.

Ниже приведен пример вывода команды для **docker info**.

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_20-53-55.png)

На этом изображении приведена подробная информация о клиенте и сервере, их версии и т.п.

Выполним , **docker run hello-world**, для загрузки образа из Docker Hub и запуска контейнера.

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_21-13-36.png)

Запустим контейнер Ubuntu с этой командой: **docker run -it ubuntu bash**

Эта команда загрузит **ubuntu** контейнер и запустит его. 

(таким же образом можно устанавливать и другие версии Linux)

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_21-20-50.png)

Предлагаю поэксперементировать с установленой версией ubuntu и проделать пару шагов для выявления возможностей установленной ubuntu

Для начала определим в каком мы сейчас находимся каталоге командой **ls**

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_21-21-35.png)

Перейдем в каталог etc следующей командой: **cd /etc/** и определим содержимое каталога etc с помощью команды **ls**

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_21-23-09.png)

Посмотрим что есть в каталоге init.d, передем в него и определим его содержимое **cd /etc/init.d && ls**

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_21-25-51.png)

Откроем файл README с помощью команды **nano**, тут первая трудность, такой команды не существует.

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_21-50-16.png)

Но мы не будем отступать и установим данный текстовый редактор. 

Заметим что с начала надо обнавить индекс пакетов APT. По существу это база данных доступных пакетов, определенных в файле
/etc/apt/sources.list и каталоге /etc/apt/sources.list.d . Для обновления локального индекса пакетов до последних изменений необхадимо
набрать следующую команду: **apt-get update** или с правами Sudo **sudo apt-get update** 

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_21-26-36.png)

Затем установим текстовый редактор - nano

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_21-26-51.png)

Как видно текстовый редактор успешно установлен.

Откроем текстовый файл в каталоге **init.d** - Skeleton с помощью следующей команды: **nano /etc/init.d/skeleton**

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_21-30-56.png)

Успешно!!!

Продолжим выполнение иследовательской работы.



Проверим командой **docker ps**, что сейчас действительно запущщен docker.

Для этого запустим еще 1 консоль и исполним команду **docker ps**.

![Image alt](https://github.com/Deadra/Deadra.github.io/blob/master/Scr/2017-04-12_21-44-38.png)

Как видно сейчас действительно запущен docker с образом ubuntu.

На этом предлогаю закончить с ubuntu

![Image alt]()
