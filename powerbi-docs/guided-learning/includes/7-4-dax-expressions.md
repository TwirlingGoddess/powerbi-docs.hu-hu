A **változók** a DAX-kifejezések rendkívül hatékonyan használható részei.

![](media/7-4-dax-expressions/dax-variables_1.png)

A DAX-kifejezésen belül bárhol definiálhat változót a következő szintaxis segítségével:

    VARNAME = RETURNEDVALUE

Bármilyen adattípus lehet változó, akár teljes táblázatok is.

Ne feledje, hogy valahányszor változóra hivatkozik a DAX-kifejezésen belül, a Power BI-nak a megadott definíció szerint újra kell számítania az értéket. Emiatt tanácsos kerülni a változók ismétlését a függvényben.

> A videótartalomért köszönet illeti [Alberto Ferrarit az SQLBI-tól](http://www.sqlbi.com/learning-dax/?utm_source=powerbi&utm_medium=marketing&utm_campaign=after-summit)
> 
> 

