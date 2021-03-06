# DjangoBlog

[//]: # (ð)

[//]: # (*[English]&#40;/docs/README-en.md&#41; â [ç®ä½ä¸­æ]&#40;README.md&#41;*)

åºäº`python3.8`å`Django3.0`çåå®¢ã   

[//]: # ([![Django CI]&#40;https://github.com/liangliangyy/DjangoBlog/actions/workflows/django.yml/badge.svg&#41;]&#40;https://github.com/liangliangyy/DjangoBlog/actions/workflows/django.yml&#41; [![CodeQL]&#40;https://github.com/liangliangyy/DjangoBlog/actions/workflows/codeql-analysis.yml/badge.svg&#41;]&#40;https://github.com/liangliangyy/DjangoBlog/actions/workflows/codeql-analysis.yml&#41; [![codecov]&#40;https://codecov.io/gh/liangliangyy/DjangoBlog/branch/master/graph/badge.svg&#41;]&#40;https://codecov.io/gh/liangliangyy/DjangoBlog&#41;  [![license]&#40;https://img.shields.io/github/license/liangliangyy/djangoblog.svg&#41;]&#40;&#41;  )

## ä¸»è¦åè½ï¼
- æç« ï¼é¡µé¢ï¼åç±»ç®å½ï¼æ ç­¾çæ·»å ï¼å é¤ï¼ç¼è¾ç­ãæç« åé¡µé¢æ¯æ`Markdown`ï¼æ¯æä»£ç é«äº®ã
- æ¯ææç« å¨ææç´¢ã
- å®æ´çè¯è®ºåè½ï¼åæ¬åè¡¨åå¤è¯è®ºï¼ä»¥åè¯è®ºçé®ä»¶æéï¼æ¯æ`Markdown`ã
- ä¾§è¾¹æ åè½ï¼ææ°æç« ï¼æå¤éè¯»ï¼æ ç­¾äºç­ã
- æ¯æOauthç»éï¼ç°å·²æGoogle,GitHub,facebook,å¾®å,QQç»å½ã
- æ¯æ`Memcache`ç¼å­ï¼æ¯æç¼å­èªå¨å·æ°ã
- ç®åçSEOåè½ï¼æ°å»ºæç« ç­ä¼èªå¨éç¥Googleåç¾åº¦ã
- éæäºç®åçå¾åºåè½ã
- éæ`django-compressor`ï¼èªå¨åç¼©`css`ï¼`js`ã
- ç½ç«å¼å¸¸é®ä»¶æéï¼è¥ææªææå°çå¼å¸¸ä¼èªå¨åéæéé®ä»¶ã
- éæäºå¾®ä¿¡å¬ä¼å·åè½ï¼ç°å¨å¯ä»¥ä½¿ç¨å¾®ä¿¡å¬ä¼å·æ¥ç®¡çä½ çvpsäºã


## å®è£
mysqlå®¢æ·ç«¯ä»`pymysql`ä¿®æ¹æäº`mysqlclient`ï¼å·ä½è¯·åè [pypi](https://pypi.org/project/mysqlclient/) æ¥çå®è£åçåå¤ã

ä½¿ç¨pipå®è£ï¼ `pip install -Ur requirements.txt`

å¦æä½ æ²¡æpipï¼ä½¿ç¨å¦ä¸æ¹å¼å®è£ï¼
- OS X / Linux çµèï¼ç»ç«¯ä¸æ§è¡: 

    ```
    curl http://peak.telecommunity.com/dist/ez_setup.py | python
    curl https://bootstrap.pypa.io/get-pip.py | python
    ```

- Windowsçµèï¼

    ä¸è½½ http://peak.telecommunity.com/dist/ez_setup.py å https://raw.github.com/pypa/pip/master/contrib/get-pip.py è¿ä¸¤ä¸ªæä»¶ï¼åå»è¿è¡ã 


## è¿è¡

 ä¿®æ¹`DjangoBlog/setting.py` ä¿®æ¹æ°æ®åºéç½®ï¼å¦ä¸æç¤ºï¼

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'djangoblog',
        'USER': 'root',
        'PASSWORD': 'password',
        'HOST': 'host',
        'PORT': 3306,
    }
}
```

### åå»ºæ°æ®åº
mysqlæ°æ®åºä¸­æ§è¡:
```sql
CREATE DATABASE `djangoblog` /*!40100 DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci */;
```

ç¶åç»ç«¯ä¸æ§è¡:
```bash
./manage.py makemigrations
./manage.py migrate
```

**æ³¨æï¼** å¨ä½¿ç¨ `./manage.py` ä¹åéè¦ç¡®å®ä½ ç³»ç»ä¸­ç `python` å½ä»¤æ¯æå `python 3.6` åä»¥ä¸çæ¬çãå¦æä¸æ¯å¦æ­¤ï¼è¯·ä½¿ç¨ä»¥ä¸ä¸¤ç§æ¹å¼ä¸­çä¸ç§ï¼

- ä¿®æ¹ `manage.py` ç¬¬ä¸è¡ `#!/usr/bin/env python` ä¸º `#!/usr/bin/env python3`
- ç´æ¥ä½¿ç¨ `python3 ./manage.py makemigrations`

### åå»ºè¶çº§ç¨æ·

 ç»ç«¯ä¸æ§è¡:
```bash
./manage.py createsuperuser
```

### åå»ºæµè¯æ°æ®
ç»ç«¯ä¸æ§è¡:
```bash
./manage.py create_testdata
```

### æ¶ééææä»¶
ç»ç«¯ä¸æ§è¡: Â 
```bash
./manage.py collectstatic --noinput
./manage.py compress --force
```

### å¼å§è¿è¡ï¼
æ§è¡ï¼ `./manage.py runserver`


æµè§å¨æå¼: http://127.0.0.1:8000/  å°±å¯ä»¥çå°ææäºã  

## æå¡å¨é¨ç½²

æ¬å°å®è£é¨ç½²è¯·åè [DjangoBlogé¨ç½²æç¨](https://www.lylinux.net/article/2019/8/5/58.html)
æè¯¦ç»çé¨ç½²ä»ç».    

æ¬é¡¹ç®å·²ç»æ¯æä½¿ç¨dockeræ¥é¨ç½²ï¼å¦æä½ ædockerç¯å¢é£ä¹å¯ä»¥ä½¿ç¨dockeræ¥é¨ç½²ï¼å·ä½è¯·åè:[dockeré¨ç½²](/docs/docker.md)



## æ´å¤éç½®:
[æ´å¤éç½®ä»ç»](/docs/config.md)
[éæelasticsearch](/docs/es.md)

## é®é¢ç¸å³

[//]: # (æä»»ä½é®é¢æ¬¢è¿æIssue,æèå°é®é¢æè¿°åéè³æé®ç®± `liangliangyy#gmail.com`.æä¼å°½å¿«è§£ç­.æ¨èæäº¤Issueæ¹å¼.  )

---
 ## è´å¤§å®¶ðââï¸ðââï¸

[//]: # ( å¦ææ¬é¡¹ç®å¸®å©å°äºä½ ï¼è¯·å¨[è¿é]&#40;https://github.com/liangliangyy/DjangoBlog/issues/214&#41;çä¸ä½ çç½åï¼è®©æ´å¤çäººçå°ã)
[//]: # (æ¨çåå¤å°ä¼æ¯æç»§ç»­æ´æ°ç»´æ¤ä¸å»çå¨åã )


## æèµ 
å¦ææ¨è§å¾æ¬é¡¹ç®å¯¹æ¨ææå¸®å©ï¼æ¬¢è¿æ¨è¯·æåæ¯åå¡ï¼æ¨çæ¯ææ¯ææå¤§çå¨åï¼æ¨å¯ä»¥æ«æä¸æ¹äºç»´ç ä¸ºæä»æ¬¾ï¼è°¢è°¢ã
### æ¯ä»å®ï¼
<div>    

[//]: # (<img src="https://resource.lylinux.net/image/2017/12/16/IMG_0207.jpg" width="150" height="150" />)
</div>  

### å¾®ä¿¡ï¼
<div>    

[//]: # (<img src="https://resource.lylinux.net/image/2017/12/16/IMG_0206.jpg" width="150" height="150" />)
</div>

---

æè°¢jetbrains
<div>    
<a href="https://www.jetbrains.com/?from=DjangoBlog"><img src="https://resource.lylinux.net/image/2020/07/01/logo.png" width="150" height="150"></a>
</div>
