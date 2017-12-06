Ebben a témában közelebbről is szemügyre vesszük, hogyan illeszkedik egymáshoz a Power BI első két része.

* Jelentés létrehozása a **Power BI Desktopban**
* Jelentés közzététele a **Power BI szolgáltatásban**

Először indítsa el a Power BI Desktopot, majd válassza az **Adatok beolvasása** lehetőséget. Megjelenik az adatforrások gyűjteménye, ahonnan kiválaszthat egy adatforrást. Az alábbi képen egy weblap forrásként történő kiválasztása látható. A fenti videóban Will egy **Excel**-munkafüzetet választott ki.

![](media/0-2-get-started-power-bi-desktop/c0a2_1.png)

Függetlenül attól, hogy melyik adatforrást választja, a Power BI ahhoz az adatforráshoz fog kapcsolódni, és az abból az adatforrásból elérhető adatokat fogja mutatni. Az alábbi képen egy másik példa látható: egy különböző államokat és nyugdíjazási statisztikákat elemző weblap.

![](media/0-2-get-started-power-bi-desktop/c0a2_2.png)

A Power BI Desktop **Jelentés** nézetében elkezdhet jelentéseket létrehozni.

A **Jelentés** nézetnek öt fő területe van:

1. A menüszalag, ahol a jelentésekkel és vizualizációs elemekkel kapcsolatos gyakori feladatok láthatók
2. A **Jelentés** nézet vagy vászon, ahol vizualizációs elemeket lehet létrehozni és elrendezni
3. A **Lapok** fülterület alul, amely lehetővé teszi egy jelentéslap kiválasztását vagy hozzáadását
4. A **Vizualizációk** ablaktábla, ahol megváltoztathatja a vizualizációs elemeket, testre szabhatja a színeket és tengelyeket, szűrőket alkalmazhat, áthúzhatja a mezőket stb.
5. A **Mezők** ablaktábla, ahonnan a lekérdezési elemeket és szűrőket át lehet húzni a **Jelentés** nézetre vagy a **Vizualizációk** ablaktábla **Szűrők** területére

![](media/0-2-get-started-power-bi-desktop/c0a2_3.png)

A **Vizualizációk** és **Mezők** ablaktáblák a szélükön látható kis nyilakkal összecsukhatók, hogy a **Jelentés** nézetben nagyobb hely legyen a vizualizációs elemek létrehozásához. Ezek a nyilak felfelé vagy lefelé mutatva a vizualizációs elemek változtatása közben is láthatók, és nyíl irányának megfelelően az adott szakasz kinyitható, illetve összecsukható.

![](media/0-2-get-started-power-bi-desktop/c0a2_4.png)

Vizualizációs elem létrehozásához egyszerűen húzzon egy mezőt a **Mezők** listáról a **Jelentés** nézetre. Ebben a példában húzza át a *RetirementStats* (Nyugdíjstatisztikák) State (Állam) mezőjét, és nézze meg, mi történik.

![](media/0-2-get-started-power-bi-desktop/c0a2_5.png)

Nézze... A Power BI Desktop automatikusan létrehozott egy térkép-alapú vizualizációs elemet, mert felismerte, hogy a State (Állam) mező földrajzi helyadatokat tartalmaz.

Most lépjünk előre egy kicsit: néhány vizualizációs elem hozzáadása után a jelentés közzétehető a Power BI szolgáltatásban. A Power BI Desktop **Kezdőlap** menüszalagjáról válassza ki a **Közzététel** lehetőséget.

![](media/0-2-get-started-power-bi-desktop/c0a2_6.png)

A rendszer kérni fogja, hogy jelentkezzen be a Power BI-ba.

![](media/0-2-get-started-power-bi-desktop/c0a2_7.png)

Amikor bejelentkezik, és befejeződik a közzétételi folyamat, az alábbi párbeszédablak jelenik meg. A **Sikeres!** felirat alatt rákattinthat a Power BI szolgáltatásra mutató hivatkozásra, ahol megtekintheti az éppen most közzétett jelentést.

![](media/0-2-get-started-power-bi-desktop/c0a2_8.png)

Amikor bejelentkezik a Power BI szolgáltatásba, látni fogja a szolgáltatásban éppen most közzétett Power BI Desktop-fájlt. Az alábbi képen a Power BI Desktopban létrehozott jelentés a **Jelentések** szakaszban látható.

![](media/0-2-get-started-power-bi-desktop/c0a2_9.png)

Ha a jelentésben rákattint a **Rögzítés** ikonra, a vizualizációs elemet rögzítheti az egyik irányítópulton. A következő képen a rögzítés ikon bekeretezve látható, egy rá mutató nyíllal.

![](media/0-2-get-started-power-bi-desktop/c0a2_10.png)

Az ikon kiválasztásakor az alábbi párbeszédablak jelenik meg, lehetővé téve, hogy a vizualizációs elemet egy már létező irányítópultra rögzítse, vagy létrehozzon egy új irányítópultot.

![](media/0-2-get-started-power-bi-desktop/c0a2_11.png)

Amikor a jelentésből rögzít néhány vizualizációs elemet, azok láthatóvá válnak az irányítópulton.

![](media/0-2-get-started-power-bi-desktop/c0a2_12.png)

A fentieken túl természetesen még sok minden másra használhatja a Power BI-t, például a létrehozott irányítópultok megosztására. A megosztásra a képzés során később még visszatérünk.

Most nézzük meg azt a szolgáltatást, amely automatikusan tud irányítópultokat létrehozni már akkor is, ha egyszerűen csatlakozik egy olyan felhőalapú szolgáltatáshoz, mint amilyen például Facebook vagy a Salesforce.

