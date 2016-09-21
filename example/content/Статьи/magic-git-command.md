/*
Title: Спасительная git команда
Description: git filter-branch
*/

git filter-branch - команда, которая позволяет отредактировать файлы или сообщения коммитов сквозь всю историю и даже во всех ветках (при необходимости). Пример команды, которая может спасти растяпу:

<code>
	git filter-branch --msg-filter 'sed "s/of http:\/\/gitlab.simbirsoft\/NoFormat\/LegacyVault/ /g"'
</code>
 Такая команда вырежет строку "of http://gitlab.simbirsoft/NoFormat/LegacyVault/" из сообщений коммитов. В аргументах передана опция msg-gilter , указывающая что изменения будут выполняться для сообщений коммитов, следующий аргумент - bash инструкция, которая и делает основную работу

**Ссылки**<br>
[git documentation](https://git-scm.com/docs/git-filter-branch)<br>