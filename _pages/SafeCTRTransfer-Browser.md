---
title: "Запуск SafeCTRTransfer, используя браузер"
permalink: /safectrtransfer-browser.html
sidebar:
  nav: "safectrtransfer-browser"
---

Если вы взламывали ваше устройство ранее и у вас установлена кастомная прошивка на основе EmuNAND, помните, что данное руководство работает только с SysNAND и вы должны выполнять вся шаги находясь в SysNAND. Помните, что RedNAND и EmuNAND - немного разные реализации [одного и того же](http://3dbrew.org/wiki/NAND_Redirection)(англ.).
{: .notice--info}

Если перед понижением прошивки до 2.1.0 на 2DS или New 3DS вы забыли включить Wi-Fi, вы можете включить его, вытащив батарею и отключив зарядное устройство на несколько секунд, затем снова включив консоль.
{: .notice--info}

Если вы использовали Управление microSD (microSD Management) для передачи данных на New 3DS, вы не сможете им воспользоваться на прошивке 2.1.0. Убедитесь, что у вас есть картридер для microSD-карт, прежде чем продолжить.
{: .notice--info}

Для использования [magnet](https://en.wikipedia.org/wiki/Magnet_URI_scheme)-ссылок в этом руководстве необходим torrent-клиент, например [Deluge](http://dev.deluge-torrent.org/wiki/Download)
{: .notice--info}

Убедитесь, что Беспроводной режим (Wireless Communication) включен и есть активное интернет-подключение. 
{: .notice--warning}

**Отключите родительский контроль (parental control) на устройстве перед тем, как перейти к 2.1.0 CTRTransfer. Если вы не знаете пароля, воспользуйтесь [генератором мастер-ключа](https://mkey.salthax.org/) (англ.). Если вы не можете отключить родительский контроль из-за того, что привязанный NNID зарегистрирован на ребенка младше 13 лет, вместо этого вам следует выставить все опции в состояние "не ограничивать" (do not restrict).**
{: .notice--warning}

**Выполнение CTRTransfer удалит все пользовательские ticket-файлы (которые дают доступ к играм) с вашего устройства до тех пор, пока не будет восстановлен бэкап.**
{: .notice--danger}

**НИКОГДА не форматируйте 2DS на прошивках ниже 6.0.0, иначе вы не сможете закончить первоначальную настройку и получите БРИК!**
{: .notice--danger}

**НИКОГДА не обновляйте New 3DS с прошивкой 2.1.0 (старая прошивка Old 3DS), это чревато БРИКОМ! Сначала ОБЯЗАТЕЛЬНО восстановите NAND из резервной копии или произведите обратный CTRTransfer на стандартную прошивку New 3DS!**
{: .notice--danger}

#### <a name="steps" />Описание шагов

В этой части мы будем прошивать [CTRNAND](https://www.3dbrew.org/wiki/Flash_Filesystem#CTR_partition) (англ.) консоли до версии 2.1.0, чтобы воспользоваться уязвимостью получения уникального для устройства [OTP](otp). OTP необходим для установки arm9loaderhax и **не может быть использован** на других устройствах.

Это достигается благодаря [установке заранее подготовленного образа CTRTransfer](https://www.reddit.com/r/3dshacks/comments/4zhe4a/) (англ.), содержащего 2.1.0, и копированию в него уникальных для каждой консоли файлов (таких как `moveable.sed` и `SecureInfo_A`), а затем восстановлением базы данных тайтлов.

#### <a name="what_need" />Что понадобится

* Свежая версия [SafeCTRTransfer](https://github.com/d0k3/SafeCTRTransfer/releases/latest)
* Образ 2.1.0 CTRTransfer для вашего устройства и региона     
*(Если вашего региона нет в списке, выберите любой)*:
  +    <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [New 3DS или Old 3DS или 2DS 2.1.0 - EUR - CTRTransfer](magnet:?xt=urn:btih:89acc9c1b488b8b38251de0ddf07975d6bd354a1&dn=2.1.0-4E%5FCTRTransfer%5Fo3ds.zip&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
  +    <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [New 3DS или Old 3DS или 2DS 2.1.0 - JPN - CTRTransfer](magnet:?xt=urn:btih:3dbb9c9c85a33c6242f424dcbaebcacdd8a5912b&dn=2.1.0-4J%5FCTRTransfer%5Fo3ds.zip&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)     
  +    <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [New 3DS или Old 3DS или 2DS 2.1.0 - USA - CTRTransfer](magnet:?xt=urn:btih:1609ce9ee7b0ed9b6dea0b3e7cca4fc52dad6ff4&dn=2.1.0-4U%5FCTRTransfer%5Fo3ds.zip&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)

#### <a name="instructions" />Инструкция

##### <a name="part1" />Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Создайте папку `CTRTransfer` в корне SD-карты, если таковой нет
1. Скопируйте 2.1.0 `.bin` и `.bin.sha` из `.zip-архива` CTRTransfer в папку `/CTRTransfer/` на SD-карте
1. Скопируйте `Launcher.dat` и `SafeCTRTransfer.dat` из `.zip-ахрива` SafeCTRTransfer в корень SD-карты
1. Вставьте SD-карту обратно в консоль
1. Включите консоль

##### <a name="part2" />Часть II - Запуск SafeCTRTransfer

1. Откройте браузер и перейдите по одно из этих ссылок:

  + `https://goo.gl/U0q0n7` или `https://dukesrg.github.io/?SafeCTRTransfer.dat`
  + `https://goo.gl/f8GbSf` или `http://go.gateway-3ds.com/`
  + `https://goo.gl/ASCLSV` или `http://www.reboot.ms/3ds/load.html?Launcher.dat`
  + `https://goo.gl/etmY59` или `http://dukesrg.dynu.net/3ds/rop?GW17567.dat&Launcher.dat`
 
* Или сосканируйте камерой QR, если QR-сканер есть в вашей версии прошивки:

Для того, чтобы попасть в QR-scanner, нажмите одновременно (L)+(R), находясь на домашнем экране, а затем нажмите пиктограмму с изображением QR-кода на нижнем экране.
{: .notice--info}

![dukesrg.github.io](images/QR/dukeGithub.png)        ![go.gateway-3ds.com](images/QR/gateway.png)<br><br>![reboot.ms](images/QR/goReboot.png)        ![dukesrg.dynu.net](images/QR/dukeDynu.png) 
  
  + В случае, если первая ссылка не сработала, попробуйте все остальные (некоторое консоли не могут использовать первую ссылку, в то время как другие не могут использовать последние три)
  + При возникновении ошибки, обратитесь к разделу [Проблемы и их решения](troubleshooting#ts_browser)

1. Если эксплойт сработал, запустится SafeCTRTransfer
{: .notice--info}

##### <a name="part3" />Часть III - CTRTransfer

1. Подождите пока SafeCTRTransfer автоматически произведет инициализацию и проверки безопасности
  + Если возникнет ошибка, убедитесь что все файлы на месте, и что на SD-карте достаточно свободного места в соответствии с разделом [Начало](get-started)
1. При появлении запроса, введите указанную комбинацию кнопок, чтобы подтвердить CTRTransfer на 2.1.0
  + Этот процесс займет некоторое время
  + Этот процесс автоматически создаст бэкап NAND вашей консоли в файле `/ctrtransfer/<serialnumber>_nand.bin`
  + При возникновении критической ошибки, обратитесь к разделу [Проблемы и их решения](troubleshooting#ts_transfer)   
1. После завершения процесса извлеките SD-карту из консоли для перезагрузки
  + Перезагрузка начнется примерно через 2 секунды
  + Консоль с прошивкой 2.1.0 при загрузке будет зависать на чёрном экране, если SD-карта будет находиться в консоли до загрузки меню HOME
  + Каждый раз при перезагрузке на 2.1.0 необходимо извлекать SD-карту и вставлять обратно после загрузки меню HOME
  + Не вставляйте SD-карту обратно в консоль. На следующей странице вы будете копировать на неё файлы
  + Это будет исправлено после восстановления бэкапа на следующей странице

___

*(Изменение цвета или искажения экрана - норма для некоторых устройств на 2.1.0, они исчезнут сразу после восстановления бэкапа)*
{: .notice--info}

{% capture notice %}
**Вы ГАРАНТИРОВАННО получите НЕВОССТАНАВЛИВАЕМЫЙ брик, если вы введете New 3DS с прошивкой 2.1.0 в режим сна!**    
**Это происходит только при закрытии крышки, _пока устройство включено_; это не касается выключения консоли.**    
**Устройство переходит в спящий режим только когда крышка закрыта. Таймера, или чего-то похожего, в системе нет.**    
**Оказавшись на 2.1.0 без промедления сделайте все необходимые шаги, чтобы избежать этого!**    
{% endcapture %}

<div class="notice--danger">{{ notice | markdownify }}</div>

Следующий шаг: [Установка arm9loaderhax](installing-arm9loaderhax)
{: .notice--primary}
