#devops-netology

Student Падеев Василий  
Fops-27  

Задание:  
В клонированном репозитории:  

1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.  
Решение:  
Команда:  
```git log --pretty=oneline | grep ^aefea  
```
Полный хеш:   
```aefead2207ef7e2aa5dc81a34aedf0cad4c32545  
```
Комментарий: Update CHANGELOG.md  


2. Какому тегу соответствует коммит 85024d3?  
Решение:  
Команда:  
```git show 85024d3  
```
Тег: v0.12.23  

3. Сколько родителей у коммита b8d720? Напишите их хеши.  
Решение:  
Команды:  
```git show b8d720^  
git show b8d720^2  
git show b8d720^3  
```
Родителей: 2  
Хеши родителей:  
```56cd7859e05c36c06b56d013b55a252d0bb7e158  
9ea88f22fc6269854151c571162c5bcf958bee2b  
```

4. Перечислите хеши и комментарии всех коммитов, которые были сделаны между тегами v0.12.23 и v0.12.24.  
Решение:  
Команда:  
```git log v0.12.23^..v0.12.24 --pretty=oneline  
```
Хеши и комментарии:  
```33ff1c03bb960b332be3af2e333462dde88b279e (tag: v0.12.24) v0.12.24  
b14b74c4939dcab573326f4e3ee2a62e23e12f89 [Website] vmc provider links  
3f235065b9347a758efadc92295b540ee0a5e26e Update CHANGELOG.md  
6ae64e247b332925b872447e9ce869657281c2bf registry: Fix panic when server is unreachable  
5c619ca1baf2e21a155fcdb4c264cc9e24a2a353 website: Remove links to the getting started guide's old location  
06275647e2b53d97d4f0a19a0fec11f6d69820b5 Update CHANGELOG.md  
d5f9411f5108260320064349b757f55c09bc4b80 command: Fix bug when using terraform login on Windows  
4b6d06cc5dcb78af637bbb19c198faff37a066ed Update CHANGELOG.md  
dd01a35078f040ca984cdd349f18d0b67e486c35 Update CHANGELOG.md  
225466bc3e5f35baa5d07197bbc079345b77525e Cleanup after v0.12.23 release  
85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23) v0.12.23  
```

5. Найдите коммит, в котором была создана функция func providerSource, её определение в коде выглядит так: func providerSource(...) (вместо троеточия перечислены аргументы).  
Решение:  
Команда:  
```git log -S 'func providerSource(' --pretty=oneline --name-only
```

Хеш и комментарий:  
```8c928e83589d90a031f811fae52a81be7153e82f main: Consult local directories as potential mirrors of providers
```
Имя файла: provider_source.go  

6. Найдите все коммиты, в которых была изменена функция globalPluginDirs.  
Решение:  
Команда:  
```git log -S 'globalPluginDirs' --pretty=oneline
```

Хеши и комментарии:  
```7c4aeac5f30aed09c5ef3198141b033eea9912be stacks: load credentials from config file on startup (#35952)
65c4ba736375607b6af6c035972f7f151232b6c6 Remove terraform binary
125eb51dc40b049b38bf2ed11c32c6f594c8ef96 Remove accidentally-committed binary
22c121df8631c4499d070329c9aa7f5b291494e1 Bump compatibility version to 1.3.0 for terraform core release (#30988)
7c7e5d8f0a6a50812e6e4db3016ebfd36fa5eaef Don't show data while input if sensitive
35a058fb3ddfae9cfee0b3893822c9a95b920f4c main: configure credentials from the CLI config file
c0b17610965450a89598da491ce9b6b5cbd6393f prevent log output during init
8364383c359a6b738a436d1b7745ccdce178df47 Push plugin discovery down into command package
```
7. Кто автор функции synchronizedWriters?  
Решение:  
Команда:  
```git log -S 'synchronizedWriters' --pretty=format:'%h %an %ad %s'
```

Автор функции: Martin Atkins   

