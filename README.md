<h1 align="center"><img src="https://github.com/user-attachments/assets/2cf01d94-b9de-4bf3-bbc6-c91cf0ce532c" width="50px"> RoskomFree - HTTP Proxy на основе Tor</h1>

### 1. Скачайте и запустите RoskomFree
Для запуска окна консоли и отладки запустите - `RoskomFree.cmd`
<br>
Для запуска в фоне запустите - `RoskomFree_service.cmd`

### 2. Установите расширение ZeroProxy
- Для Chrome https://chromewebstore.google.com/detail/proxy-switchyomega-3-zero/pfnededegaaopdmhkdmcofjmoldfiped
- Для Firefox https://addons.mozilla.org/en-US/firefox/addon/zeroomega/

### 3. Настройте расширение
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
