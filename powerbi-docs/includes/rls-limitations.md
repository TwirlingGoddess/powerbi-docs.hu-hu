## <a name="limitations"></a>Korlátozások
Itt találja a sorszintű biztonság felhőmodellekben érvényes aktuális korlátozásait.

* Ha korábban szerepköröket és szabályokat adott meg a Power BI szolgáltatásban, újból létre kell hoznia őket a Power BI Desktopban.
* Csak a Power BI Desktop-ügyféllel létrehozott adatkészleteken határozhat meg RLS-t. Ha az Excellel létrehozott adatkészletekhez szeretné engedélyeznie az RLS-t, először PBIX formátumba kell konvertálnia a fájlokat. [További információ](../desktop-import-excel-workbooks.md)
* Csak az ETL- és a DirectQuery-kapcsolatok támogatottak. Az Analysis Services élő kapcsolatait a helyszíni modellen lehet kezelni.
* A Q&A és a Cortana egyelőre nem támogatott az RLS-sel. Nem fog látni Q&A beviteli mezőt az irányítópultokhoz, ha mindegyik modellhez RLS van konfigurálva. Ennek az orvoslása szerepel a terveink között, de egyelőre nem tudjuk, mikorra fog megvalósulni.
* A külső megosztás jelenleg nem támogatott az RLS-t használó adatkészletekkel.
* Minden egyes modell esetén a biztonsági szerepkörökhöz rendelhető Azure AD-s rendszerbiztonsági tagok (vagyis egyéni felhasználók vagy biztonsági csoportok) maximális száma 1000. Ha sok felhasználót szeretne hozzárendelni a szerepkörökhöz, egyéni felhasználók helyett biztonsági csoportokat rendeljen hozzá.

## <a name="known-issues"></a>Ismert problémák
Az egyik ismert hiba, hogy hibaüzenet jelenik meg, amikor a Power BI Desktopból próbál közzétenni valamit, amit korábban már közzétett. A forgatókönyv a következő.

1. Anna olyan adatkészlettel rendelkezik, amely közzé van téve a Power BI szolgáltatásban, és konfigurált RLS-sel rendelkezik.
2. Anna frissíti a jelentést a Power BI Desktopban, és újból közzéteszi.
3. Anna hibaüzenetet kap.

**Áthidaló megoldás:** Tegye közzé újra a Power BI Desktop-fájlt a Power BI szolgáltatásból a probléma megoldásáig. Ehhez válassza az **Adatok lekérése** > **Fájlok** lehetőséget. 

