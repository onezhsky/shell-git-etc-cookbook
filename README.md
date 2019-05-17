# shell-git-etc-cookbook

Шпаргалки по shell, git и т. д.

## Git

Шпаргалка по git - https://eax.me/git-commands/

### git clone

В текущую папку:

```git clone url .```

В другую указанную папку:

```git clone url другой/каталог```


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


