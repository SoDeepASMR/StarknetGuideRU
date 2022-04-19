<h1 align="center">Гайд по установке ноды Starknet<h1>

`1` Переходим на сайт [Alchemy.com](https://alchemy.com/)
<br><br>

`2` Регистрируемся или заходим через гугл акк
<br><br>

`3` Выбираем `Ethereum`

![image](https://user-images.githubusercontent.com/61911146/163990417-e52198c3-6b7c-48e0-a9d4-da428fd1b78e.png)
<br><br>

`4` Пишем любое название команды и приложения и выбираем сеть `Goerli`

   ![image](https://user-images.githubusercontent.com/61911146/163991102-cb4a00ac-cecb-4068-988c-b053fda88cd5.png)
<br><br>

`5` Прокликиваем `Continue` и пропускаем пэйменты 
<br><br>

`6` Копируем и сохраняем `HTTP` ключ, он нам ещё пригодится

![image](https://user-images.githubusercontent.com/61911146/163991842-27677192-6751-44e5-967f-cdeccb8a9624.png)
![image](https://user-images.githubusercontent.com/61911146/163992342-5f4478fd-6d0d-4719-ac20-14c618dcd560.png)
<br><br>

`7` Переходим в наш сервер и обновляем его
```{bash}
sudo apt-get update && sudo apt-get -y full-upgrade
```
<br><br>

`8` Создаем переменную с нашим `HTTP` ключом
```{bash}
ALCHEMY=СЮДА ВСТАВЛЯЕМ НАШ КЛЮЧ
echo 'export ALCHEMY='$ALCHEMY >> $HOME/.bash_profile
```
<br><br>

`9` Устанавливаем ноду одним скриптом
```{bash}
wget -O starknet.sh https://api.nodes.guru/starknet.sh && chmod +x starknet.sh && ./starknet.sh
```
-----------------------------------------------------------------------------------------------
<h1 align="center">Дополнительно<h1>

Просмотр логов ноды
```{bash}
journalctl -u starknetd -f
```

Статус демона ноды
```{bash}
systemctl status starknetd
```

Рестарт ноды
```{bash}
systemctl restart starknetd
```
