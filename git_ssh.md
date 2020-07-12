# PC にgitのSSHギーを設定
1. 用户的名字点击，选择"seting"，左侧的SSH key选择。
![参考](01.png)
![great](02.png)
![](03.png)
2. terminalを開ける。
3. sshを生成する、便利するため、passport を設定しない・

```
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
4. "Adding your SSH key to the ssh-agent"で、以下のコメドをコピーする
```
$ eval "$(ssh-agent -s)"
$ ssh-add ~/.ssh/id_rsa
```
5. hubgit に追加。
```
$ sudo apt-get install xclip

$ xclip -sel clip < ~/.ssh/id_rsa.pub
```
或は以下のコマンドを使用して、コーピーする。
```
$ cat ~/.ssh/id_rsa.pub
```