1.Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.
	git log aefead2207ef7e2aa5dc81a34aedf0cad4c32545 или git show aefea
	commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545
	Update CHANGELOG.md


2.Какому тегу соответствует коммит 85024d3?
	git show 85024d3
	v0.12.23

3.	Сколько родителей у коммита b8d720? Напишите их хеши.
	git show b8d720 или git log b8d720 или нагляднее git log --graph b8d720
	2 (56cd7859e, 9ea88f22f)

4.	Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами v0.12.23 и v0.12.24.
	git show v0.12.24
	commit 33ff1c03bb (узнал хэш v0.12.24)
	
	git log 33ff1c03bb --oneline
	33ff1c03b (tag: v0.12.24) v0.12.24
	b14b74c49 [Website] vmc provider links
	3f235065b Update CHANGELOG.md
	6ae64e247 registry: Fix panic when server is unreachable
	5c619ca1b website: Remove links to the getting started guide's 	old location
	06275647e Update CHANGELOG.md
	d5f9411f5 command: Fix bug when using terraform login on Windows
	4b6d06cc5 Update CHANGELOG.md
	dd01a3507 Update CHANGELOG.md
	225466bc3 Cleanup after v0.12.23 release
	85024d310 (tag: v0.12.23) v0.12.23

5.	Найдите коммит в котором была создана функция func providerSource, ее определение в коде выглядит так func providerSource(...) (вместо троеточего перечислены аргументы).
	git log -S "func providerSource"
	commit 5af1e6234ab6da412fb8637393c5a17a1b293663
	Author: Martin Atkins <mart@degeneration.co.uk>
	Date:   Tue Apr 21 16:28:59 2020 -0700

6.	Найдите все коммиты в которых была изменена функция globalPluginDirs.
	git log -S "globalPluginDirs" --oneline
	35a058fb3 main: configure credentials from the CLI config file
	c0b176109 prevent log output during init
	8364383c3 Push plugin discovery down into command package

7.	Кто автор функции synchronizedWriters?
	git log -S"synchronizedWriters"
	git show 5ac311e2a91e3
	Author: Martin Atkins <mart@degeneration.co.uk>
	Date:   Wed May 3 16:25:41 2017 -0700
