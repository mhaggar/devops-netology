1. команда: 
git log aefea 
ответ:
aefead2207ef7e2aa5dc81a34aedf0cad4c32545
Update CHANGELOG.md

2.
+ команда:
git log 85024d3
ответ:
тэг указан в скобках коммита 
v0.12.23
+ команда:
git log b8d720
ответ:
в коммите есть строка merge где указаны родители
2 commits 56cd7859e0 9ea88f22fc
+ команда:
git log v0.12.23..v0.12.24
ответ:
после выполнения команды получаем список коммитов: 
commit 33ff1c03bb960b332be3af2e333462dde88b279e (tag: v0.12.24)
    v0.12.24

  commit b14b74c4939dcab573326f4e3ee2a62e23e12f89
    [Website] vmc provider links

  commit 3f235065b9347a758efadc92295b540ee0a5e26e
    Update CHANGELOG.md

  commit 6ae64e247b332925b872447e9ce869657281c2bf
    registry: Fix panic when server is unreachable

    Non-HTTP errors previously resulted in a panic due to dereferencing the
    resp pointer while it was nil, as part of rendering the error message.
    This commit changes the error message formatting to cope with a nil
    response, and extends test coverage.

    Fixes #24384

  commit 5c619ca1baf2e21a155fcdb4c264cc9e24a2a353
    website: Remove links to the getting started guide's old location

    Since these links were in the soon-to-be-deprecated 0.11 language section, I
    think we can just remove them without needing to find an equivalent link.

  commit 06275647e2b53d97d4f0a19a0fec11f6d69820b5
    Update CHANGELOG.md

  commit d5f9411f5108260320064349b757f55c09bc4b80
    command: Fix bug when using terraform login on Windows

  commit 4b6d06cc5dcb78af637bbb19c198faff37a066ed
    Update CHANGELOG.md

  commit dd01a35078f040ca984cdd349f18d0b67e486c35
    Update CHANGELOG.md

  commit 225466bc3e5f35baa5d07197bbc079345b77525e
    Cleanup after v0.12.23 release
+ команда:
git log -S 'func providerSource'
ответ:
первый коммит указывает когда была создана функция, второй - когда изменена 
commit 8c928e83589d90a031f811fae52a81be7153e82f
+ команда:
git grep "globalPluginDirs"
git log -L :globalPluginDirs:plugins.go
ответ:
первой командой получаем имя файла в котором находится функция, второй ищем изменения
 commit 78b12205587fe839f10d946ea3fdc06719decb05
  commit 52dbf94834cb970b510f2fba853a5b49ad9b1a46  
  commit 41ab0aef7a0fe030e84018973a64135b11abcd70
  commit 66ebff90cdfaa6938f26f908c7ebad8d547fea17
+ команда:
git log -S "synchronizedWriters"
git checkout 5ac311e2a91e381e2f52234668b49ba670aa0fe5 
git grep "synchronizedWriters"
git blame -C -L 15,30 synchronized_writers.go
ответ:
Первой командой ищем перый коммит, где упоминается эта функция, второй переключаемся на этот коммит, третьей - ищем имя файла в которой находится эта функция, затем находим строки функции. Последней командой смотрим аннотацию кто написал эту функцию. 
5ac311e2a91 (Martin Atkins 2017-05-03 16:25:41 -0700 15)
