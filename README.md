## RoskomFree - HTTP Proxy на основе Tor 
### 2. Скачайте ZeroProxy
- Для Chrome https://chromewebstore.google.com/detail/proxy-switchyomega-3-zero/pfnededegaaopdmhkdmcofjmoldfiped?hl=en
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

