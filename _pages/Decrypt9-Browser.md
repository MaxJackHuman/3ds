---
title: "Запуск Decrypt9 используя браузер"
permalink: /decrypt9-browser.html
sidebar:
  nav: "decrypt9-browser"
---

Первую вещь, которую необходимо сделать - запустить Decrypt9, многоцелевую утилиту, которая позволит нам установить прошивку версии 2.1.0. В этой прошивке содержится уязвимость, которая необходима для дальнейшего взлома консоли.
{: .notice}

Если вы взламывали 3DS ранее и у вас установлена кастомная прошивка на основе EmuNAND, помните, что данное руководство работает только с SysNAND и вы должны выполнять все шаги находясь в SysNAND. Помните, что RedNAND и EmuNAND - немного разные реализации [одного и того же](http://3dbrew.org/wiki/NAND_Redirection) (англ.).
{: .notice--info}

#### <a name="what_need" />Что понадобится

* Свежая версия [Decrypt9WIP](https://github.com/d0k3/Decrypt9WIP/releases/latest)

#### <a name="instructions" />Инструкция

1. Создайте папку `files9` в корне вашей SD-карты, если таковой нет
2. Скопируйте `Launcher.dat` и `Decrypt9WIP.dat` из Decrypt9WIP `.zip` в корень SD-карты
3. Вставьте SD-карту обратно в 3DS
4. Откройте браузер и перейдите по одно из этих ссылок:

  + `https://goo.gl/XGez65` или `https://dukesrg.github.io/?Decrypt9WIP.dat`
  + `https://goo.gl/f8GbSf` или `http://go.gateway-3ds.com/`
  + `https://goo.gl/ASCLSV` или `http://www.reboot.ms/3ds/load.html?Launcher.dat`
  + `https://goo.gl/etmY59` или `http://dukesrg.dynu.net/3ds/rop?GW17567.dat&Launcher.dat`
 
* Или сосканируйте камерой QR, если QR-сканер есть в вашей версии прошивки:

Для того, чтобы попасть в QR-scanner, нажмите одновременно (L)+(R), находясь на домашнем экране, а затем нажмите пиктограмму с изображением QR-кода на нижнем экране.
{: .notice--info}

![dukesrg.github.io](images/QR/dukeGithub.png)        ![go.gateway-3ds.com](images/QR/gateway.png)<br><br>![reboot.ms](images/QR/goReboot.png)        ![dukesrg.dynu.net](images/QR/dukeDynu.png) 
  
  + В случае, если первая ссылка не сработала, попробуйте все остальные (некоторое консоли не могут использовать первую ссылку, в то время как другие не могут использовать последние три)
  + При возникновении ошибки, обратитесь к разделу [Проблемы и их решения](troubleshooting#ts_browser)

5. Если эксплойт сработал, запустится Decrypt9

Следующий шаг: [2.1.0 ctrtransfer](2.1.0-ctrtransfer).
{: .notice--primary}