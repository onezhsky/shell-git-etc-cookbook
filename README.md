# shell-git-etc-cookbook

Шпаргалки по shell, git и т. д.

## Shell 

Шпаргалка tproger - https://eax.me/git-commands/

### Скачать сайт с помощью wget

```wget --mirror --convert-links --page-requisites --no-parent -P . https://example-domain.com```

Источник с пояснениями и другими полезными командами - https://andreyex.ru/ubuntu/10-primerov-komandy-wget/

```wget -r -k -l 7 -p -E -nc -erobots=off --user-agent="Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/5З7.З6 (KHTML, like Gecko) Chrome/60.0.З112.11З Safari/5З7.36" www.bartek.wojtyca.pl```

Из комментов отсюда: - https://toster.ru/q/202277

### Работа с zip

Архивация: 

```zip -r www.zip . ```

Архивация с исключением определенных расширений: 

```zip -x *.jpg *.JPG *.zip -r www.zip .```

Архивация и исключеним поддиректорий:

```zip -r myarchive.zip dir1 -x "dir1/ignoreDir1/*" "dir1/ignoreDir2/*"```

Разархивация: 

```unzip www.zip```


### Работа с tar.gz

Архивация: 

```tar -cvzf www.tar.gz .```

Разархивация: 

```tar -xvzf www.tar.gz```

Разархивация

```tar: tar -xvf file.tar```


### Многотомные архив с 7zip 

1. Создание многотомного архива arch.7z, положив в него содержимое папки soft:

```7za a -v100m arch.7z soft/```

в результате будут созданы файлы arch.7z.001 arch.7z.002 arch.7z.003 ..., размер каждого 100 Мб (опция -v100m).

2. Чтобы распаковать многотомный архив arch.7z.001, достаточно поместить все части архива в текущую папку и дать команду:

```7za x arch.7z.001```

Источник - https://webhamster.ru/mytetrashare/index/mtb0/1369989626iqfs7i9vi5

### mysqldump

```mysqldump -u root -h localhost -p database > db.sql```


### Рекурсивный CHMOD

Файлы: 

```find . -type f -exec chmod 755 {} \;```

Папки: 

```find . -type d -exec chmod 755 {} \;```

Или: 

```chmod -R 755 ./*```

### Размер директории в мб

```du -sh <название папки>```

### Размер поддиректорий 

```du -hs * | sort -hr```

### Использование пространства на диске

```df```

###  Удалить директорию

```rm -rf letters/```

### Перезагрузка Apache

```apachectl restart```

### Удаление файла с кривой кодировкой в названии

Удаление по номеру inode

``` 
$ ls -1 -i
144368 ???.txt
144363 ??.txt
$ find . -inum 144368 -delete
```


### Мониторинг системы

Текущее состояние системы: 

```top```

Список процессов: 

```ps aux```

Состояние памяти:

```free -m```

Состояние системы: 

```nmon```

Статья о мониторинге и производительности в документации UMI.CMS - http://dev.docs.umi-cms.ru/nastrojka_sistemy/proizvoditelnost/

### Мониторинг

Внутри команды MySQL


```show processlist;
show status;
```

А также закладка “Состояние” и “Процессы” в phpMyadmin.

## Git

Шпаргалка по git - https://eax.me/git-commands/

### git clone

В текущую папку:

```git clone url .```

В другую указанную папку:

```git clone url другой/каталог```

### Добавить в репозиторий все файлы директории с поддиректориями

```
git add --all
git commit -am "<commit message>"
git push
```










