# enlightenment17
Адаптированные исходники enlightenment17 под новые ubuntu

Адаптировано под ubuntu 22.04 (24.04  пока ошибки с edje_cc при сборке пакетов), собирается и с 1.7.9 и с 1.7.10, но есть небольшие проблемы с evas_generic_loaders и enlightenment иногда запускается с чёрным экраном после первоначальной настройки (если выбран opengl).
Оригиналы в https://ppa.launchpadcontent.net/efl/trunk/ubuntu/pool/

Ключевые изменения:
- Патчи добавлены в ecore, eet, evas-generic-loaders, evas. Оставлены оригинальные патчи eina, enlightenment
- В ecore убрана жёсткая зависимость от libxp-dev
- В ethumb исправлен "Source-Version" -> "source:Version"
- Изменены compat с 6 до 7

Ссылки скачивания исходников (всё проверено):

https://distro.ibiblio.org/slitaz/sources/packages-cooking/e/evas_generic_loaders-1.7.10.tar.bz2
https://distro.ibiblio.org/slitaz/sources/packages-cooking/e/ethumb-1.7.10.tar.bz2
https://distro.ibiblio.org/slitaz/sources/packages-cooking/e/e_dbus-1.7.10.tar.bz2
https://distro.ibiblio.org/slitaz/sources/packages-cooking/e/emotion-1.7.10.tar.bz2
https://distro.ibiblio.org/slitaz/sources/packages-cooking/e/elementary-1.7.10.tar.bz2
https://distro.ibiblio.org/slitaz/sources/packages-cooking/e/eio-1.7.10.tar.bz2
https://bos.us.distfiles.macports.org/ecore/ecore-1.7.10.tar.bz2
https://bos.us.distfiles.macports.org/evas/evas-1.7.10.tar.bz2
https://bos.us.distfiles.macports.org/eet/eet-1.7.10.tar.bz2
https://bos.us.distfiles.macports.org/eina/eina-1.7.10.tar.bz2
https://bos.us.distfiles.macports.org/edje/edje-1.7.10.tar.bz2
https://bos.us.distfiles.macports.org/efreet/efreet-1.7.10.tar.bz2
https://bos.us.distfiles.macports.org/embryo/embryo-1.7.10.tar.bz2
https://distro.ibiblio.org/slitaz/sources/packages-cooking/e/eeze-1.7.10.tar.bz2

https://ppa.launchpadcontent.net/efl/trunk/ubuntu/pool/main/t/terminology/terminology_0.3.0-1ppa2~saucy.tar.gz
https://github.com/borisfaure/terminology/archive/refs/tags/v0.1.0.zip
https://github.com/borisfaure/terminology/archive/refs/tags/v0.2.0.zip

https://ppa.launchpadcontent.net/efl/trunk/ubuntu/pool/main/e/e17/e17_0.17.5-1ppa1~saucy.tar.gz
https://archive.ubuntu.com/ubuntu/pool/universe/e/e17/e17_0.17.6-1.1.debian.tar.xz
https://distro.ibiblio.org/slitaz/sources/packages-cooking/e/enlightenment-0.17.6.tar.bz2




Порядок сборки:
1. eina - нужен для сборки eet
2. eet
3. evas - нужен, чтобы сформировать ecore-evas, то есть для правильной сборки ecore
4. ecore
5. embryo
5. eio
6. edje - нужен для сборки ethumb
7. emotion - нужен для сборки ethumb и terminology
8. edbus - нужен для сборки ethumb
9. ethumb - нужен для сборки elementary
10. efreet - нужен для сборки elementary
11. elementary
12. terminology
13. eeze - нужен для сборки e17
14. evas-generic-loaders - нужен для установки e17
15. e17

