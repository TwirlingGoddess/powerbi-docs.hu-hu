A Power BI-ban kapcsolatokat alakíthat ki egyszerre több táblázat között is, beleértve a teljesen eltérő adatforrásból származókat. Az adatmodellek kapcsolatait a Power BI Desktop **Kapcsolatok** nézetében tekintheti meg.

![](media/7-5-table-relationships-and-dax/dax-relationships_1.png)

## <a name="dax-relational-functions"></a>A DAX relációs függvényei
A DAX **relációs függvényei** lehetővé teszik a létesített kapcsolatokkal rendelkező táblák kezelését.

A DAX-függvények segítségével eredményként visszaadhatja egy adott oszlop értékét, vagy akár egy kapcsolat összes sorát.

Például a **TABLE** (táblázat) függvény a kapcsolódásokat követve visszaadja egy oszlop értékét, míg a **RELATEDTABLE** (kapcsolódó táblázat) követi a kapcsolódást, és egy kapcsolódó sorokra szűrt teljes táblázatot ad vissza eredményként.

![](media/7-5-table-relationships-and-dax/dax-relationships_2.png)

A **RELATED** (kapcsolódó) függvény *több-az-egyhez* típusú kapcsolatoknál használható, a **RELATEDTABLE** pedig *egy-a-többhöz* típusúaknál.

A relációs függvények használatával olyan kifejezéseket hozhat létre, amelyek több különböző táblázat értékeit tartalmazzák. A DAX a kapcsolati lánc hosszától függetlenül mindig visszaadja ezeknek a függvényeknek az eredményét.

> A videótartalomért köszönet illeti [Alberto Ferrarit az SQLBI-tól](http://www.sqlbi.com/learning-dax)
> 
> 

