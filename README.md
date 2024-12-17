<h1 align="center"><img src="https://github.com/user-attachments/assets/2cf01d94-b9de-4bf3-bbc6-c91cf0ce532c" width="50px"> RoskomFree - HTTP Proxy на основе Tor</h1>

РоскомФри - новый проект на основе сети Tor. Новые супербыстрые мосты позволяют быстро и эффективно обходить любую цензуру для сидения Discord (Дискорд) и просмотра YouTube (Ютуб) даже если эти сервисы заблокированы в вашей стране. 

Прокси HTTP позволяет не ломать игры, а также не нарушать и не замедлять работу остальных сайтов. Что делает данный проект идеальным инструментом для обхода блокировок.

А простая установка и инструкция позволяет установить данное решение даже для полных чайников.

> [!WARNING]  
> Чтобы знать о выходах последних обновлений рекомендуем подписаться на наш Telegram канал https://t.me/roskomfree

> [!CAUTION]  
> Если у вас возникли любые вопросы Вы можете задать их в Telegram группе https://t.me/youtubenotwork

## 1. Как и почему это работает
Сеть Tor (The Onion Router) - это система, позволяющая пользователям сохранять анонимность в Интернете. Она работает, направляя интернет-трафик через серию ретрансляторов, разбросанных по всему миру, что затрудняет отслеживание действий пользователей и определение их реального местоположения.

### 1.1 Почему Tor сложно взломать и заблокировать?
Сложность взлома Tor обусловлена несколькими ключевыми факторами:
1. **Многослойное шифрование:** Tor использует многослойное шифрование, подобное луковице ("onion"). Каждый ретранслятор удаляет один слой шифрования, узнавая только адрес предыдущего и следующего узла в цепочке. Это означает, что ни один ретранслятор не обладает полной информацией о происхождении и назначении трафика.
2. **Децентрализация:** Tor - это децентрализованная сеть, не имеющая единой точки отказа или контроля. Она состоит из тысяч добровольных ретрансляторов, управляемых обычными людьми по всему миру. Это делает её крайне устойчивой к атакам и цензуре.
3. **Отсутствие центрального управления:** Никто не владеет сетью Tor и не контролирует её. Сеть управляется сообществом пользователей и разработчиков, что гарантирует её независимость и устойчивость к внешнему влиянию.
4. **Большое количество ретрансляторов:** Чем больше ретрансляторов в сети, тем сложнее отследить трафик и скомпрометировать анонимность пользователей. Тысячи ретрансляторов, находящихся в разных юрисдикциях, создают огромное количество возможных маршрутов для трафика, делая атаку практически невозможной.
5. **Ретрансляторы - обычные люди:** Большинство ретрансляторов Tor управляются добровольцами - обычными людьми, которые хотят внести свой вклад в свободу и приватность в Интернете. Это разнообразие участников затрудняет компрометацию значительной части сети.
6. **Постоянное развитие и совершенствование:** Проект Tor постоянно развивается. Разработчики регулярно улучшают протоколы и исправляют уязвимости, делая сеть ещё более безопасной.

### 1.2 Новый протокол Webtunnel
**Webtunnel** - это новый подключаемый транспорт Tor, разработанный для повышения устойчивости к блокировкам. Он маскирует трафик Tor под обычный зашифрованный веб-трафик (HTTPS), делая его практически неотличимым от обычного просмотра веб-страниц.

**Преимущества Webtunnel:**
- **Повышенная устойчивость к блокировкам:** Благодаря маскировке под обычный HTTPS, Webtunnel сложно обнаружить и заблокировать. Ваш провайдер не увидит что Вы используете Tor.
- **Простота использования:** Webtunnel легко настраивается и не требует от пользователей специальных знаний.
- **Хорошая производительность:** Webtunnel обеспечивает высокую скорость соединения, сравнимую с другими современными подключаемыми транспортами.

Подробнее о протоколе можно почитать здесь:
- https://xakep.ru/2024/03/14/webtunnel
- https://www.securitylab.ru/news/546698.php

## 2. Установка программы
### 2.1. Скачайте и запустите RoskomFree
Скачать по ссылке: https://github.com/censorliber/roskomfree/archive/refs/heads/main.zip
<br>
Для запуска окна консоли и отладки запустите - `RoskomFree.cmd`
<br>
Для запуска в фоне запустите - `RoskomFree_service.cmd`

### 2.2. Установите расширение ZeroProxy
- Для Chrome https://chromewebstore.google.com/detail/proxy-switchyomega-3-zero/pfnededegaaopdmhkdmcofjmoldfiped
- Для Firefox https://addons.mozilla.org/en-US/firefox/addon/zeroomega/

### 2.3. Настройте расширение
Откройте настройки:

![image](https://github.com/user-attachments/assets/130ae337-7c04-4dc0-a154-7011a414e77d)

Введите заданный прокси (`127.0.0.1` и порт `8228`):

![image](https://github.com/user-attachments/assets/558286db-0a12-4e3e-9fe1-e6bb2f9a2e65)

Перейдите во вкладку `auto switch`:

![image](https://github.com/user-attachments/assets/4c65a761-0c8e-422a-91b7-5d5192d21fca)

Нажмите `Edit source code`

![image](https://github.com/user-attachments/assets/f0559845-4d10-45c2-941a-33ad8d93f4ce)

```python
[SwitchyOmega Conditions]
@with result

*.instagram.com +proxy
scontent-hel3-1.cdninstagram.com +proxy
*.cdninstagram.com +proxy
*.ntc.party +proxy
*.youtube.com +proxy
*.googlevideo.com +proxy
play.google.com +proxy
yt3.ggpht.com +proxy
youtu.be +proxy
*.discord.com +proxy
*.discord.gg +proxy
*.discordapp.com +proxy
*.discordapp.net +proxy
*.discord.media +proxy
*.discord-attachments-uploads-prd.storage.googleapis.com +proxy
*.dis.gd +proxy
*.discord.co +proxy
*.discordcdn.com +proxy
*.discordstatus.com +proxy
bbc.com +proxy
*.proton.me +proxy
twitter.com +proxy
*.twimg.com +proxy
t.co +proxy
x.com +proxy
*.torproject.org +proxy
*.rutracker.org +proxy 
*.rutracker.cc +proxy
*.archive.org +proxy
*.web.archive.org +proxy
*.soundcloud.com +proxy
*.mullvad.net +proxy
*.nnmclub.to +proxy
*.roskomsvoboda.org +proxy
holod.media +proxy
news.google.com +proxy
*.medium.com +proxy
*.habr.com +proxy
*.hybrid-analysis.com +proxy
*.4pda.to +proxy
*.chatgpt.com +proxy

* +direct
```

Сохраните изменения:

![image](https://github.com/user-attachments/assets/516ff29b-842c-4ebc-8403-12a83ce7d7ab)

Выйдите из настроек. Теперь Вам следует выбрать режим `auto switch`, нажав по иконке расширения (после успешного выбора он загорится синим):

![image](https://github.com/user-attachments/assets/c57837ca-9e40-4d0b-a90c-1f544493a6f1)
