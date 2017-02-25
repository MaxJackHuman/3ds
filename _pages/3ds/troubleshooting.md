---
title: "Проблемы и их решения"
permalink: /troubleshooting.html
sidebar:
  nav: "troubleshooting"
---

Если Ваша приставка не загружается, найдите раздел, соответствующий вашей проблеме и следуйте его инструкциям. После решения возникшей проблемы, вернитесь к основному руководству (этот раздел весьма обширный, воспользуйтесь Ctrl+F для поиска своей проблемы)
{: .notice--primary}

**Если вы всё ещё не в состоянии решить проблему и нуждаетесь в помощи, скопируйте содержимое .log-файлов из корня SD-карты на [Gist](https://gist.github.com/) и подготовьте детальное описание проблемы и ваших попыток по её устранению для получения помощи.**
{: .notice--info}

## <a name="twl_broken" />DSi / DS игры не работают после завершения руководства

#### Что нам понадобится

* TWL_FIRM `.cia`, соответствующие вашему устройству
    + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`New_3DS TWL_FIRM - v9936.cia`](magnet:?xt=urn:btih:eab8558c97b18b1f329a2bfcc3c899b84c082a27&dn=New%5F3DS%20TWL%5FFIRM%20-%20v9936.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
    + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`Old_3DS TWL_FIRM - v8817.cia`](magnet:?xt=urn:btih:17511eadb6e6f3ff22d04f90644e37bd2d96ca43&dn=Old%5F3DS%20TWL%5FFIRM%20-%20v8817.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`TWL Version Data - v0.cia`](magnet:?xt=urn:btih:4a106681407fede5de95cc8bda635432481f6b5d&dn=TWL%20Version%20Data%20-%20v0.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`DS Internet - v2048.cia`](magnet:?xt=urn:btih:2b9df8496922f2546dfb0b01220068ce53c19d3d&dn=DS%20Internet%20-%20v2048.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`DS Download Play - v1024.cia`](magnet:?xt=urn:btih:b581d3c5d98f5e621fddfc1ce5704bb45bf05a8c&dn=DS%20Download%20Play%20-%20v1024.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`Nintendo DS Cart Whitelist - v11264.cia`](magnet:?xt=urn:btih:7b90d506ad032a581a00035616eaa17a68c48eff&dn=Nintendo%20DS%20Cart%20Whitelist%20-%20v11264.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
 
#### Инструкция

##### Часть I - Подготовительные работы

1. Создайте папку `cias` в корне SD-карты, если таковой нет
2. Скопируйте `TWL Version Data - v0.cia` в папку `/cias/` на SD-карте
3. Скопируйте `DS Download Play - v1024.cia` в папку `/cias/` на SD-карте
4. Скопируйте `DS Internet - v2048.cia` в папку `/cias/` на SD-карте
5. Скопируйте `Nintendo DS Cart Whitelist - v11264.cia` в папку `/cias/` на SD-карте
6. Скопируйте `New_3DS TWL_FIRM - v9936.cia`  или `Old_3DS TWL_FIRM - v8817.cia` в папку `/cias/` на SD-карте

##### Часть II - Установка

1. Запустите FBI
2. Выберите "SD"
3. Перейдите в папку "cias"
4. Выберите "\<current directory>"
5. Выберите "Install and delete all CIAs"
6. Выйдите из FBI нажатием кнопки (HOME)

## <a name="rm_nnid" />Удаление NNID без форматирования устройства

#### Что нам понадобится

* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest)

#### Инструкция

1. Скопируйте `GodMode9.bin` из архива GodMode9 в папку `/luma/payloads/` на вашей карте памяти и переименуйте `GodMode9.bin` в `up_GodMode9.bin`.
12. Перезагрузите приставку, удерживая (ВВЕРХ), чтобы запустить GodMode9.
14. Перейдите в `SYSNAND CTRNAND` -> `data` -> (32-х-значный ID) -> `sysdata` -> `00010038`
15. Нажмите (X), удерживая (R) на файле `00000000`, чтобы переименовать его. 
16. Нажмите (ВВЕРХ), чтобы переименовать файл в `10000000`.
17. Нажмите (A), чтобы сохранить изменения.
18. Нажмите (A), чтобы разблокировать SysNAND для записи, а затем введите указанную клавишную комбинацию для подтверждения.
18. Вернитесь в главное меню.
16. Нажмите (START) для перезагрузки.

## <a name="gw_fbi" />Не выходит сделать интеграцию в Health & Safety на устройстве с пониженной прошивкой с помощью Gateway

Это вызвано крайне некорректной процедурой понижения прошивки Gateway, которая дублирует каждое приложение в системе. Одно из них не используется, но это сбивает с толку Decrypt9, из-за чего он интегрирует FBI в отключенный дубликат.

#### Что понадобится

* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest)

#### Инструкция

1. Скопируйте `GodMode9.bin` из `.zip-архива` GodMode9 в директорию `/luma/payloads/` на SD-карте и переименуйте `GodMode9.bin` в `up_GodMode9.bin`
2. Вставьте SD-карту обратно в 3DS
5. Открыть GodMode9 из arm9loaderhax. Для этого нужно зажать кнопку (ВВЕРХ), а затем, не отпуская кнопку, включить консоль.      
2. Перейдите в `SYSNAND CTRNAND` -> `title` -> `00040010`.
7. Перейдите в папку, соответствующую вашему регион и типу приставки:
  + **Old 3DS EUR**: `00022300` -> `content`;
  + **Old 3DS JPN**: `00020300` -> `content`;
  + **Old 3DS USA**: `00021300` -> `content`;
  + **New 3DS EUR**: `20022300` -> `content`;
  + **New 3DS JPN**: `20020300` -> `content`;
  + **New 3DS USA**: `20021300` -> `content`;
8. Видите, здесь два типа *.app и *.tmd файлов? Первые написаны в капсе (`.TMD` и `.APP`), а вторые - нет (`.tmd` и `.app`).
11. Удерживая (R), нажмите (Y), чтобы создать новую папку.
10. Нажмите (А), чтобы подтвердить название новой папки - `newdir` (нам без разницы как она будет называться). 
6. Нажмите (А), чтобы разблокировать SysNAND для записи и введите указанную комбинацию кнопок.
9. На каждом файле, разрешение которого написано в капсе (`.TMD` и `.APP`), нажмите (L), чтобы отметить его.
10. Нажмите (Y), чтобы скопировать эти файлы.
11. Перейдите в `newdir`.
12. Нажмите (Y), чтобы переместить выбранные ранее файлы.
13. Выберите "Move path(s)".
14. Теперь файлы с капсом переместились в папку `newdir`.
15. Нажмите (START) для перезагрузки. 
16. Вернитесь к [установке A9LH](installing-arm9loaderhax) и попробуйте инжект FBI еще раз. 
17. Если снова не получилось, то верните капснутые файлы назад в папку `content` и повторите операцию перемещения файлов в папку `newdir`, уже с файлами без капса (`.tmd` и `.app`), а затем вернитесь к [установке A9LH](installing-arm9loaderhax) и попробуйте инжект FBI еще раз. 

## <a name="ts_browser" />Почему не работает эксплойт, использующий браузер?

Эксплойты, базирующиеся на браузере (browserhax или 2xrsa, например) очень нестабильные и частенько крашатся, но иногда всего этого можно избежать, следуя рекомендациям, описанным ниже:

1. Откройте браузер, затем настройки браузера (settings):
    1. Пролистайте в самый низ и выберите "Удалить сохр. данные" (Initialize Savedata/Clear All Save Data).
    2. Попробуй запустить эксплойт еще раз.

## <a name="ts_safe_a9lh" />Приставка грузится в SafeA9LHInstaller

Вы просто скопировали не верный `arm9loaderhax.bin` на SD-карту

1. Используйте верный `arm9loaderhax.bin`:
    1. Скопируйте `arm9loaderhax.bin` из архива Luma3DS в корень своей карты памяти;
    2. Выключите приставку, зажмите (SELECT) и включите.

## <a name="ts_safe_a9lh_screen" />Изображение после запуска SafeA9LHInstaller некорректно

Такое часто бывает непонятно почему. Кнопки все равно работают, поэтому нажимайте (SELECT) до тех пор, пока консоль не выключится (если приставка не выключается, секунд через 10 просто отключите долгим нажатием кнопки включения).

1. Просто следуйте инструкции как ни в чем не бывало
2. Нажимайте (SELECT) до тех пор, пока консоль не выключится
3. Подождите несколько секунд
4. Нажмите любую кнопку, чтобы выключить консоль

## <a name="ts_d9_backup" />Decrypt9 или Hourglass9 не восстанавливают / не видят мой NAND-бекап

1. Убедитесь, что в **корне** КП нет папки "Decrypt9".
3. Попробуйте сделать проверку файловой системы карточки с помощью [H2testw (Windows)](h2testw-windows), [F3 (Linux)](f3-linux), или [F3X (Mac)](f3x-mac).
4. Сделайте бекап карты памяти и переформатируйте ее, затем верните все файлы на место.
5. Попробуйте другую карту памяти.

## <a name="ts_sys_down" />Черный экран при загрузке SysNAND 

1. Попробуйте загрузиться без SD-карты, а затем верните ее в консоль.
    1. Отключите приставку, зажав кнопку выключения.
    2. Вытащите SD-карту.
    3. Включите 3DS. 
    4. Когда появится меню Home, вставьте назад SD-карту.
    5. Если сработало, то следует отчистить данные Домашнего экрана. Для этого удалите в папке `/Nintendo 3DS/(32-значный ID)/(32-значный ID)/extdata/00000000/`, папку, соответствующую вашей системе и региону
        + EUR регион: Удалите `00000098`;
        + JPN регион: Удалите `00000082`;
        + USA регион: Удалите `0000008f`;
        + KOR регион: Удалите `000000A9`;
1. Попробуйте загрузиться без картриджа (совсем).
2. Если есть хардмод - восстановите бекап наверняка рабочего NAND в SysNAND.
3. Загрузитесь в режим восстановления и обновите систему.
    *Почти наверняка не сработает на 3DS с прошивкой 2.1.0*    
    **НЕЛЬЗЯ делать на New 3DS с прошивкой 2.1.0 - гарантированный брик**
    1. Отключите приставку, зажав кнопку выключения
    2. Удерживайте  (L)+(R)+(A)+(ВВЕРХ)
    3. Включите 3DS
    4. Зайдя в режим восстановления, обновите свою 3DS.
4. Может быть брик. Для поддержки обращайтесь на [#3dshacks on Rizon IRC](https://www.reddit.com/r/3dshacks/wiki/irc) или в [3DS Hacking on Discord](https://discord.gg/MWxPgEp) (*для русскоязычных - группа [3DS_cfw](http://vk.com/3ds_cfw) - прим. пер.*).

## <a name="ts_sys_a9lh" />Черный экран при загрузке SysNAND после установки a9lh

1. Убедитесь, что у вас установлен рабочий загрузчик
    1. Проверьте, есть ли в корне SD-карты файл `arm9loaderhax.bin`.
2. Попробуйте сбросить настройки Luma 
    1. Удалите файл `/luma/config.bin` с SD-карты
    2. Заново настройте Luma после запуска. 
3. Проверьте, грузится ли Hourglass9
    1. Выключите приставку, зажмите (START) и включите.
4. Попробуйте отчистить данные Домашнего экрана
    1. Удалите в папке `/Nintendo 3DS/(32-значный ID)/(32-значный ID)/extdata/00000000/`, папку, соответствующую вашей системе и региону: 
        + EUR регион: Удалите `00000098`
        + JPN регион: Удалите `00000082`
        + USA регион: Удалите `0000008f`
        + KOR регион: Удалите `000000A9`
1. Попробуйте загрузиться без картриджа (совсем).
8. Если вы даунгрейдились через Gateway, то убедитесь, что у вас установлена самая последняя версия Luma3DS (не ниже, чем 6.2.3).
9. Если версия вашего NAND между 3.0.0 и 4.5.0, проделайте следующие действия:
    + Убедитесь, что используете самую свежую версию [Luma 3DS](https://github.com/AuroraWright/Luma3DS/releases)
    + Скачайте [этот файл](http://nus.cdn.c.shop.nintendowifi.net/ccs/download/0004013800000002/00000056) и переименуйте в `firmware.bin`.
    + Скачайте [этот файл](http://nus.cdn.c.shop.nintendowifi.net/ccs/download/0004013800000002/cetk).
    + Скопируйте `firmware.bin` и `cetk` в папку `/luma/` на SD-карте
    + После обновления системы удалите эти файлы. 
9. Попробуйте выполнить [9.2.0 ctrtransfer](9.2.0-ctrtransfer).
10. Попросите помощи на [#3dshacks on Rizon IRC](https://www.reddit.com/r/3dshacks/wiki/irc) или в [3DS Hacking on Discord](https://discord.gg/MWxPgEp) (*для русскоязычных - группа [3DS_cfw](http://vk.com/3ds_cfw) - прим. пер.*).

## <a name="ts_sys_blue" />Голубой экран при загрузке (bootrom error)

1. У вас брик.
2. Восстановиться может помочь [хардмод](https://gbatemp.net/threads/414498/) или ремонт / замена устройства.