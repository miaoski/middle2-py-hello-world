如何 deploy Hello World 到 Middle2 上面
=======================================
Middle 2 使用的是 Python 2 ，必須有一個 HTTP service，最容易的方式是寫一個 flask 程式。

```bash
virtualenv venv
source venv/bin/activate
pip install flask
pip freeze > requirements.txt
```

然後把需要的三個檔案都放進 git 後 push 上 Middle 2:

```bash
git add hello.py Procfile requirements.txt
git commit -a -m 'draft'
git push
```

一陣 build 之後，就可以用囉!


或是你可以...
=============
直接下載 middle2-py-hello-world :

```bash
git clone https://github.com/miaoski/middle2-py-hello-world.git
git remote add middle2 git@middle2.com:host-name-123456
git push middle2 master
```


版權
====
MIT 宣告，請詳見 LICENSE 。
