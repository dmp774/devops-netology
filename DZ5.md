1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.

 git show aefea
 
 git log aefea

 aefead2207ef7e2aa5dc81a34aedf0cad4c32545

 git log aefead2207ef7e2aa5dc81a34aedf0cad4c32545

 Update CHANGELOG.md

2. 
 a. Какому тегу соответствует коммит 85024d3?

 
 git show -s --oneline 85024d3
 
 git log --oneline 85024d3
 
 85024d3100 (tag: v0.12.23) v0.12.23


 b. Сколько родителей у коммита b8d720? Напишите их хеши.

 git show --pretty b8d720 
 
 git show 56cd7859e0
 
 git show 9ea88f22fc 

 Два
 
 56cd7859e05c36c06b56d013b55a252d0bb7e158 9ea88f22fc6269854151c571162c5bcf958bee2b


 c.Перечислите хеши и комментарии всех коммитов, которые были сделаны между тегами v0.12.23 и v0.12.24.

 git log --oneline v0.12.23..v0.12.24
 
33ff1c03bb (HEAD, tag: v0.12.24) v0.12.24

b14b74c493 [Website] vmc provider links
 
3f235065b9 Update CHANGELOG.md
 
6ae64e247b registry: Fix panic when server is unreachable
 
5c619ca1ba website: Remove links to the getting started guide's old location
 
06275647e2 Update CHANGELOG.md
 
d5f9411f51 command: Fix bug when using terraform login on Windows
 
4b6d06cc5d Update CHANGELOG.md
 
dd01a35078 Update CHANGELOG.md
 
225466bc3e Cleanup after v0.12.23 release
 
 d.Найдите коммит, в котором была создана функция func providerSource, её определение в коде выглядит так: func providerSource(...) (вместо троеточия перечислены аргументы).

 git log -S"func providerSource("

 8c928e835

 e.Найдите все коммиты, в которых была изменена функция globalPluginDirs.

 git grep "globalPluginDirs"
 
 git log -s -L :globalPluginDirs:plugins.go

52dbf94834 keep .terraform.d/plugins for discovery

41ab0aef7a Add missing OS_ARCH dir to global plugin paths

66ebff90cd move some more plugin search path logic to command

8364383c35 Push plugin discovery down into command package

 f.Кто автор функции synchronizedWriters?

 git log -S "func synchronizedWriters("
 
 git show 5ac311e2a91e381e2f52234668b49ba670aa0f

Martin Atkins <mart@degeneration.co.uk>

