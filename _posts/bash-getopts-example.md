---
layout: article
title: "Как обрабатывать аргументы к bash скрипу"
categories: tips
tags:
- bash
- linux
- snippets
image:
  teaser: teaser_01.jpg
  feature: featured_01.jpg 
comments: false  
---

Я довольно часто пишу небольшие скрипты на bash. В основном, они содержат просто последовательность команд с нужными параметрами. 

Нередко такие скрипты могут принимать аргументы для подстановки (типа скриптов в /etc/init.d). 

Но иногда бывает нужно чтобы у скрипта было несколько аргументов с возможностью указания разного количества параметров (как у большинства утилит в linux). 

Конечно, это можно реализовать разными способами. Но я нашел, что использовать *getopts* _почти всегда_ лучше. И чтобы не забыть как это делается, приведу ниже пример использования:


{% highlight bash linenos=table %}

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





---