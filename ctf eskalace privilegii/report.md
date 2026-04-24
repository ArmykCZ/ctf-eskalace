Kterou zranitelnost jste využili?
zjistili jsme, že suid bit má /usr/bin/syscheck
ze strings /usr/bin/syscheck jsme zjistili. že program volá funkci system(date)
s tím, že když se podíváme do toho stringu, který nám byl vypsán, tak nevidíme absolutní cestu našeho date 

poté jsme dali do path náš /tmp a vytvořili soubor date, kam jsme dali příkaz na spawnutí root shellu, kdy path bere první první soubor se jménem date co existuje, syscheck ho spustí v system(date) s root právy

Jaký je rozdíl mezi UID a EUID při spuštění takového programu

uid = kdo to spustil
euid jaká práva má proces

Jak byste jako administrátor zajistili systém, aby tento útok nebyl možný.

dát absolutní cestu k date :D
