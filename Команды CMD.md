## Создать файл

>[!example] Создание пустого файла
>```bash
>echo. > empty_file.txt
>```

>[!example] Создание файла с текстом
>```bash
>echo Hello, World! > filename.txt
>```
## Просмотр файла

>[!example] Просмотр файла
>```bash
>type somefile.txt
>more somefile.txt
>```
>Для копирования содержимого необходим флаг ***clip***. 
>Пример: [[Команды CMD#Копирование содержимого файла]]

## Вставка в файл

>[!example] Вставка в файл в использованием ***PowerShell***
>```bash
>Get-clipboard > file.txt
>```
>Происходит перезапись файла

## Копирование содержимого файла

>[!example] Копирование содержимого файла
>```bash
>clip < somefile.txt
>type somefile.txt | clip
>```

>[!example] Копирование содержимого команды(пример: ***ipconfig***)
>```bash
>ipconfig | clip
>```

По каким-то причинам. ***Powershell*** не копирует русские символы. Решается переходом в ***cmd***, а потом обратно в ***Powershell***

## Удаление файла
```bash
del somefile.txt
```
