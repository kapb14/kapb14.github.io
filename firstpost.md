---
layout: article
title:  FirstPost
date: 2016-01-16
description: Проба пера на новом блоговом движке с проверкой синтаксической разметки и основных фитч.
categories: tests
tags:
- jekyll
image:
  teaser: teaser_01.jpg
  feature: featured_01.jpg 
permalink: /firstpost/  
---

Решил перенести свой блог с blogspot на github.io (он же Github Pages) с использованием Jekyll. 
Выбрал первый понравившийся шаблон - **gaya**.\\
И вуа-ля! 

___

Ну и пользуясь правом <del>первой ночи</del> первого поста - поупражняюсь в использовании markdown разметки.

> Как применить "зачеркивание" текста (strikethrough) нашел на [stackexchange](http://webapps.stackexchange.com/questions/14986/strikethrough-with-github-markdown) не знаю прокатит или нет, но попробывать стоит ;) 


* * *


## Привет!

### Заголовок 3

#### Заголовок 4

##### Заголовок 5

###### Заголовок 6




#### Пример кода на bash:

{% highlight bash %}
getopts_lookup(){
  while getopts "ha:u:m:" OPTION "$@"; do
    case "$OPTION" in
      m)  has_MSG=true; MSG="$OPTARG"; echo "MSG: $MSG" ;;
      a)  has_APP=true; APP="$OPTARG"; echo -e "APP: $APP \t OPTIND: $OPTIND" ;;
      u)  has_URL=true; URL="$OPTARG"; echo -e "URL: $URL \t OPTIND: $OPTIND" ;;
      h)  show_help ;;
      :)  echo "Option -$OPTARG requires an argument." >&2; exit 1 ;;
    esac
  done
  test ${has_PRI} && shift $((OPTIND-1))
  test ${has_URL} && shift $((OPTIND-1))
  test ${has_EVE} && shift $((OPTIND-1))
  test ${has_APP} && shift $((OPTIND-1))
}
getopts_lookup "$@ "
{% endhighlight %}



#### В дальнейшем, я планирую перенести несколько старых постов из своего старого блога [unixdojo.blogspot.ru](http://unixdojo.blogspot.ru) :

- Powershell Tips
- Бэкап ezjail-archive
- SMART под FreeBSD
- Бэкап конфигов cisco
- gmirror FreeBSD
- Средства мониторинга во FreeBSD
- Win7 WiFi AP
- Tacacs+
- EE sources
- FreeBSD usbflash install
- Марш отцов
- Lazy Linux вырезки
- iptables simples
- Bash hotkeys
- Сборка FreeBSD
- Про Samba 




   * * * 


#### Конечно, пост не обойдётся без парочки картинок:

![placeholder](http://placehold.it/400x200 "Medium example image")
![placeholder](http://placehold.it/200x200 "Small example image")


---


### Какая-то табличка:

|---
| Первая колока | Вторая колонка | Еще одна колонка
|:-|:-:|-:
| слева | по центру | справа
| текст в первой колонке | _текст во второй колонке_ | текст в третьей колонке
| *исчо раз* | исчо два | исчо три
| крекс | пекс| фекс
|---
| Second body
| 2 line
|===
| Footer row


---


#### Ну и не обойдётся без "рыбы" [сгенерил тут](http://fishtext.ru) :

Повседневная практика показывает, что постоянное информационно-пропагандистское обеспечение нашей деятельности в значительной степени обуславливает создание дальнейших направлений развития. Товарищи! постоянный количественный рост и сфера нашей активности требуют определения и уточнения модели развития.


:smile:


___


##### [и еще один cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

##### [оригинальный док по kramdown](http://kramdown.gettalong.org/syntax.html)

##### For more markdown features please look on [markdown styles](https://guides.github.com/features/mastering-markdown/). %


---



