---
title: "Homebrew Launcher (SoundHax)"
permalink: /homebrew-launcher-soundhax.html
---

Существует много различных точек входа в Homebrew Launcher.
{: .notice}

SoundHax совместим с версиями прошивки от 9.0.0 до 11.3.0 включительно в регионах EUR, JPN, KOR и USA.
{: .notice--info}

Убедитесь, что Беспроводной режим (Wireless Communication) включен и есть активное Интернет-подключение. 
{: .notice--info}

Заметьте, что обновление на картридже позволяет обновить только базовые функции консоли, такие как Системные настройки, меню HOME, и т. п. Приложение Звук Nintendo 3DS и сетевые функции, такие как Перенос системы, Интернет-браузер, Площадь StreetPass Mii или eShop с картриджа не обновляются.
{: .notice--info}

Это означает, что обновление картриджем с версии <9.0.0 сделает невозможным запуск [Soundhax](homebrew-launcher-(soundhax))! Вам понадобится [альтернативный метод](homebrew-launcher-(alternatives)) запуска Homebrew Launcher!
{: .notice--info}

Если версия вашего браузера от 1 до 6 (откройте Системные настройки (System Settings); обратите внимание на нижний правый угол верхнего экрана, на число вида X.X.X-Y, где Y - версия вашего браузера), следует попробовать запустить [HBL, используя браузер](https://3ds.customfw.xyz/homebrew-launcher-browser). 
{: .notice--warning}

#### <a name="what_need" />Что понадобится 

+ Homebrew [Starter Kit](http://smealum.github.io/ninjhax2/starter.zip)
+ Последняя версия [SoundHax](http://soundhax.com/) *(для вашего устройства и региона)*
+ [otherapp payload](https://smealum.github.io/3ds/#otherapp) *(для вашей версии и региона)*

#### <a name="instructions" />Инструкция

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Скопируйте _содержимое_ папки `starter` из архива `starter.zip` в корень вашей SD-карты
1. Скопируйте Soundhax `.m4a` в корень вашей SD-карты
1. Скопируйте otherapp payload в корень вашей SD-карты и переименуйте его в `otherapp.bin`
1. Вставьте SD-карту обратно в консоль
1. Включите консоль
1. Запустите приложение Звук Nintendo 3DS (Nintendo 3DS Sound)
1. Пролистайте все сообщения говорящего попугая, закройте приложение и запустите снова
  + Если запустить Soundhax сразу, без закрытия, то птичка будет появляться при каждом запуске программы, до тех пор, пока вы не выполните этот пункт
1. Перейдите в `/SDCARD`, затем начните воспроизведение "<3 nedwill 2016"
  + Может потребоваться несколько попыток
  + При зависании отключите питание консоли, зажав кнопку питания, и попробуйте снова
1. Консоль должна загрузиться в Homebrew Launcher

___

Следующий шаг: [SafeCtrTransfer (Homebrew Launcher)](safectrtransfer-homebrew-launcher)
{: .notice--primary}
