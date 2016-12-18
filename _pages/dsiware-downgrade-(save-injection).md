---
title: "Понижение прошивки при помощи DSiWare (инжект сохранения)"
permalink: /dsiware-downgrade-(save-injection).html
---

Если ваша прошивка 11.0.0, 11.1.0, или 11.2.0, то вы можете понизить версию NATIVE_FIRM, используя DSiWare и вторую 3DS с установленной кастомной прошивкой.
{: .notice}   

Этот метод использует уязвимость, которая позволяет DSiWare-приложениям писать и читать в любом месте NAND. 
{: .notice--info}

Будьте готовы ждать. Slowhax не с потолка получил такое название. Работа хака займет от 20 (New 3DS) до 60 (Old 3DS) минут.
{: .notice--info}

Это рабочая реализация "FIRM partitions known-plaintext"-эксплойта. Подробнее о нем [здесь](https://www.3dbrew.org/wiki/3DS_System_Flaws).
{: .notice--info}

Ваше DSiWare-сохранение будет скопировано перед тем, как будет заменено взломанным сохранением.
{: .notice--info}

#### Что нужно:

* Купленная игра из списка ниже. *Игра должна быть уже установлена в приставку, поскольку каждая из игр в списке уже удалена из eShop*.
  + **Fieldrunners**;
  + **Legends of Exidia**;
  + **Guitar Rock Tour**; 
  + **The Legend of Zelda: Four Swords (Anniversary Edition)**  
* Точка входа из [этого списка](homebrew-launcher-(no-browser)) или (в случае, если у вас прошивка версии 11.0.0 EUR / USA) [из этого списка](homebrew-launcher-(browser)).    
* Свежая версия [3ds_dsiwarehax_installer](https://github.com/yellows8/3ds_dsiwarehax_installer/releases)
* Свежая версия [waithax](https://github.com/Mrrraou/waithax/releases/latest)
* Свежая версия [3DSident](https://github.com/joel16/3DSident/releases/latest)
* Свежая версия [dgTool](https://github.com/Plailect/dgTool/releases/latest)
* Свежая версия [TinyFormat](https://github.com/javimadgit/TinyFormat/releases)
* The Homebrew [Starter Kit](http://smealum.github.io/ninjhax2/starter.zip)
* Архив с прошивкой, соответствующей версии **целевой 3DS**:
  + [New 3DS 11.0.0](magnet:?xt=urn:btih:2d13a5ea1570f911bd5c6423e0c30e51d548837a&dn=11.0.0%5Fto%5F10.4.0%5Fn3ds.zip&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
  + [Old 3DS 11.0.0](magnet:?xt=urn:btih:72393bbd99bc285db84a9cabf39d9b3200058d6a&dn=11.0.0%5Fto%5F10.4.0%5Fo3ds.zip&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)     
  ~    
  + [New 3DS 11.1.0](magnet:?xt=urn:btih:d7d60c27c18f53bd8508a194656a465f6448bedf&dn=11.1.0%5Fto%5F10.4.0%5Fn3ds.zip&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)     
  + [Old 3DS 11.1.0](magnet:?xt=urn:btih:0caf9a948a2d8bf23606d641f6628e2baeb983bb&dn=11.1.0%5Fto%5F10.4.0%5Fo3ds.zip&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)     

#### Что делать:

##### Часть I - Подготовка

1. Скопируйте _содержимое_ архива `starter.zip` в корень карты памяти с заменой.
  + Таким образом мы актуализируем все необходимые файлы для работы Homebrew Launcher; старые версии HBL приводят к зависанию 3ds_dsiwarehax_installer.
4. Скопируйте папку `3ds` с заменой из архива 3ds_dsiwarehax_installer в корень КП.
4. Скопируйте папку `4B51394A` из архива `4B51394A.zip` в папку `/3ds/3ds_dsiwarehax_installer/dsiware/` на карте памяти. 
5. Скопируйте папку `3ds` с заменой из архива 3DSident в корень КП.
5. Скопируйте `waithax.3dsx` в папку `/3ds/` на КП.
6. Скопируйте `boot.nds` от dgTools в корень КП.
4. Скопируйте папку `3ds` с заменой из архива TinyFormat в корень КП.
1. Создайте папку `dgTool` в корне карты памяти **целевой 3DS**, если таковой там нет.
3. Скопируйте содержимое архива с NFIRM (11.y.y_to_10.4.0_x3ds.zip) в папку `dgTool`.
3. Верните карту памяти в 3DS.

##### Часть II - Резервное копирование DsiWare

После окончания этого гайда, созданная в этой части резервная копия может быть использована для восстановления сохранения DSiWare-игры с помощью удаления DSiWare из системной памяти и восстановления игры из карты памяти.
{: .notice--info}

Сделанный бекап может быть использован только на том NAND, на котором был создан. Если вы отформатируете 3DS, или восстановите другой NAND, (особенно если `movable.sed` был изменен), резервная копия станет бесполезной.
{: .notice--info}

1. Перейдите в Системные настройки (System Settings), Управление данными (Data Management), "DSiWare".
2. Скопируйте все DSiWare-игры , которые уже есть на КП в системную память.
4. Покиньте системное меню.

##### Часть III - waithax

1. Запустите Homebrew Launcher, используя удобную вам точку входа.
2. Запустите waithax.
3. Ожидайте
  + На New 3DS, процесс хака занимает около 20 минут (хотя на некоторых системах, из-за ошибки, может пройти столько же времени, как и на Old 3DS).
  + На Old 3DS, роцесс хака занимает около часа.
4. После окончания процесса нажмите (START) для выхода.
5. Запустите 3ds_dsiwarehax_installer.
6. Выберите DSiWare-игру, в которую хотите установить эксплойт. 
4. После окончания процесса нажмите (A) для выхода.
8. Нажмите (START) для входа в меню Hombrew Launcher.
4. Нажмите (A) для выхода.

##### Часть IV - Резервное копирование NAND

3. Запустите установленную DSiWare-игру.
4. Запустите dgTool, используя установленную DSiWare-игру. 
  + **Fieldrunners**: коснитесь кнопки 'Scores' в главном меню;
  + **Legends of Exidia**: после того, как нажмете (A) или (Start) и пропустите два игровых экрана, выберите первый слот сохранения и нажмите продолжить (continue).
  + **Guitar Rock Tour**: листайте вниз и перейдите в High-Scores -> Drums -> Easy.
  + **The Legend of Zelda: Four Swords (Anniversary Edition)**: Просто начните игру.
  + Если у игры нет установленного хакнутого сохранения, начните инструкцию с начала.
5. Выберите "Dump nand", чтобы сделать бекап NAND 3DS.
  + Процесс занимает много времени.
6. Запомните путь, по которому сохраняется результат. 
7. Выйдите из dgTool.
  + При необходимости выключите приставку, удерживая кнопку питания.
8. Вставьте КП в компьютер, скопируйте `NAND_N3DS.bin` или `NAND_O3DS.bin` (зависит от вашей модели) в надежное место.
  + Сделайте копии в нескольких местах или в облачном хранилище; 
  + Этот бекап может спасти вам консоль, если что-то пойдет не так.
  + **Убедитесь, что размер вашего бекапа соответствует размеру указанному в [этом](nand-size) разделе; если это не так, удалите бекап и создайте его заново!**

##### Часть V - Прошивка целевой 3DS.

**НЕ понижайте прошивку с помощью dgTool на приставках с установленным arm9loaderhax. Это гарантированно приведет к брику!**

3. Запустите установленную DSiWare-игру.
4. Запустите dgTool, используя установленную DSiWare-игру. 
  + **Fieldrunners**: коснитесь кнопки 'Scores' в главном меню;
  + **Legends of Exidia**: после того, как нажмете (A) или (Start) и пропустите два игровых экрана, выберите первый слот сохранения и нажмите продолжить (continue).
  + **Guitar Rock Tour**: листайте вниз и перейдите в High-Scores -> Drums -> Easy.
  + **The Legend of Zelda: Four Swords (Anniversary Edition)**: Просто начните игру.
3. Выберите "Downgrade FIRM to 10.4" и подтвердите установку файлов прошивки 10.4.0 в **целевую 3DS**.
4. Закройте dgTool.
  + Для этого зажмите кнопку питания и держите до тех пор, пока приставка не выключится.
5. Перезагрузите приставку.

##### Часть VI - Проверка эксплойта

2. Вставьте КП в 3DS.
3. Запустите Homebrew launcher, используя удобную для вас точку входа.
4. Запустите 3DSident.
5. Убедитесь, что в программе следующие значения совпадают:
  + **Kernel version**: 2.50-11
  + **FIRM version**: 2.50-11
  + Если у вас отображаются другие значения, значит вы где-то допустили ошибку. Проделайте все с самого начала. 
5. Нажмите любую кнопку, чтобы вернуться в Homebrew Launcher.

##### Часть VII - Форматирование устройства
Форматирование нужно, чтобы избежать софт-брика описанного в разделе [Понижение прошивки до 9.2.0](9.2.0-downgrade). Бекап, сделанный ранее, будет использован для восстановления состояния приставки до форматированияю, когда вы дойдете до [установки arm9loaderhax](installing-arm9loaderhax).
{: .notice--info}

Вы не потеряете данных, если у вас есть бекап, который вы восстановите, когда перейдете к [установке arm9loaderhax](installing-arm9loaderhax).
{: .notice--info}

1. Запустите TinyFormat из Hombrew Launcher.
2. Нажмите (Y) для форматирования устройства.
3. Настройте устройство.

Версия прошивки, указанная в настройках **не** изменится.
{: .notice--info}

Переходите к [понижению прошивки до 9.2.0](9.2.0-downgrade)
{: .notice--primary}