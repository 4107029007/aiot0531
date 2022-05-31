# AIoT Github

## Lecture 15: IoT Flask Web (deploy to heroku)
#### Author: Norah Lin

### Target
1. 使用local app.py但使用遠端DB
### step 0 : Clone this github

* 註冊 Heroku, github 請下載 HeidiSQL, VS code


### step 1 : Clone this github

* git clone https://github.com/huanchen1107/aiot0530-start-no-token 到 local\aiot0531 folder
* 把local的 \aiot0531\.git 殺掉 (產生自己的git管理員) 方便建立新的git repository 
https://github.com/4107029007/aiot0531
### step 2 : install some package


```python
pip install gunicorn   
Flask==2.0.1 
Jinja2==3.0.1 
psycopg2 
sklearn 
pandas  
numpy 
```

### step 3: add an heroku postgredb

* register heroku account
* go to dashboard
* new an app
* go to resource and add-on an Heroku postgredb

### step 4: login to heroku pstgredb using HeidiSQL

* 在heidi中登入剛剛建立起的pstgredb
* 網路類型選擇PostgresSQL
* library選最新的
* user跟host等都依序填入heroku中credential的資料

```sql
myserver ="<fill-in-Heroku-Postgredb-DB-sever>"
myuser="<fill-in-Heroku-Postgredb-DB-user>"
mypassword="<fill-in-Heroku-Postgredb-DB-pwd>"
mydb="<fill-in-Heroku-Postgredb-DB-db>"

```
### step 5: import postgredb (in db/postgre.db)

* 連接至postgredb後，載入預先寫好的sql檔並執行
* 通過create table跟insert將資料寫入db中
(若不確定是否有正確上傳，可以去heruku的網站overview現有的db看是否有成功上傳)

### step 6: setting db in app.py

* 在app.py中加入db的帳密跟server
(要讓app.py可以去access剛剛建立的db)

```sql
myserver ="<fill-in-Heroku-Postgredb-DB-sever>"
myuser="<fill-in-Heroku-Postgredb-DB-user>"
mypassword="<fill-in-Heroku-Postgredb-DB-pwd>"
mydb="<fill-in-Heroku-Postgredb-DB-db>"

```
### step 7: testing locally by running python app.py

* 執行app.py並點開連結
* 點擊setRandom跟callAI按鈕看是否可以輸出相對應的highchart
### step 8: deploy to github (new public github repositoy)

delete .git and git remote add origin master github.com/xxxxx


### step 9: Heroku deploy from github

### step 10: Complete

Sample link 1:
https://awinlab-aiot.herokuapp.com/

Sample link 2: 
https://aiot0529.herokuapp.com/





