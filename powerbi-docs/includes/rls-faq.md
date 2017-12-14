## <a name="faq"></a>Gyakori kérdések
**Kérdés:** Mi történik, ha korábban létrehoztam szerepköröket/szabályokat egy adatkészlethez a Power BI szolgáltatásban? Akkor is működnek, ha nem teszek semmit?  
**Válasz:** Nem. A vizualizációk nem fognak megfelelően renderelődni. Újból létre kell hoznia a szerepköröket/szabályokat a Power BI Desktopban, majd közzé kell tennie őket a Power BI szolgáltatásban.

**Kérdés:** Létrehozhatom ezeket a szerepköröket az Analysis Services-adatforrásokhoz?  
**Válasz:** Igen, ha az adatokat a Power BI Desktopba importálta. Ha élő kapcsolatot használ, nem konfigurálhatja az RLS-t a Power BI szolgáltatáson belül, mert a helyszínen van meghatározva az Analysis Services-modellben.

**Kérdés:** RLS-sel korlátozhatom a felhasználóim számára elérhető oszlopok vagy mértékek körét?  
**Válasz:** Nem. Ha egy felhasználó hozzáfér egy adott adatsorhoz, a sor összes adatoszlopát láthatja.

**Kérdés:** Lehetővé teszi az RLS, hogy elrejtsem a részletes adatokat, de hozzáférést nyújtsak a vizualizációkban összegzett adatokhoz?  
**Válasz:** Nem. Egy-egy adatsort biztosíthat, de a felhasználók mindig látják a részleteket vagy az összegzett adatokat.

