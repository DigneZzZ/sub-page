<p align="center">
  <a href="[https://github.com/MuhammadAshouri/marzban-templates](https://github.com/DigneZzZ/sub-page.git)" target="_blank" rel="noopener noreferrer" >
    <img src="https://github.com/MuhammadAshouri/marzban-templates/blob/dca23a0ecbee84839686a1b928a2dc7e8aba4089/template-01/screenshot.jpg" alt="SubPage screenshots" width="800" height="auto">
  </a>
</p>

# Usage

## Этот репозиторий является русской версией : https://github.com/DigneZzZ/sub-page.git

```bash
cd /opt/marzban
apt install git
git clone https://github.com/DigneZzZ/sub-page.git
```

Then you have to map it to your docker container. Add this line to volume section of `docker-compose.yml`:

(DO NOT REPLACE WHOLE FILE, Just the last line)
```docker
services:
    marzban:
        ...
        volumes:
            ...
      - /opt/marzban/sub-page/config.py:/code/config.py
      - /opt/marzban/sub-page/subscription.py:/code/app/views/subscription.py
      - /opt/marzban/sub-page/subscription:/code/app/templates/subscription
```

Now you can restart your marzban's docker:
```
marzban restart
```


---

