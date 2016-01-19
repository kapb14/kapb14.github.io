---
layout: article
title: "PowerShell Tips раунд 1"
categories: old
tags:
- powershell
- basics
teaser: teaser_02.jpg
---

Для  начала, PowerShell 3.0 в powershell_ise.exe  из под админа на своей workstation. 

___

> Рекомендую также поставить [Microsoft Script Explorer for Windows PowerShell](http://www.microsoft.com/en-us/download/details.aspx?displaylang=en&id=29101)


Обновить наш "Get-Help":

    Update-Help


Увидеть варианты коммандлетов начинающихся с "Test-":

    Get-Command Test-*


Открыть в дефолтном браузере msdn по запрашиваемому коммандлету:

    Get-Help New-Alias -Online


Позырить **man** по запрашиваемому коммандлету:

    Get-Help New-Alias

Или просто:

    man New-Alias

> Дело в том, что в powershell уже есть несколько Alias'ов и **man** - как раз один из них. 


Посмотреть имеющиеся алиасы (сокращения):

    Get-Alias


Открыть профиль в блокноте:

    notepad $profile



Разрешить запуск скриптов скачанных из сети и имеющих валидный сертификат:

    Set-ExecutionPolicy RemoteSigned



Смотреть текстовый лог в реальном времени (вроде "tail -f"):

    Get-Content -Path .\ЛогФайл.log -Wait

___

> Быстро запустить консольную команду из "Win+R" так, чтобы окно "cmd.exe" не закрылось сразу после выполнения. (Не совсем по теме PowerShell`а, но захотелось сохранить заметку):

    [Win+R]
    cmd /c ipconfig&&pause

---


