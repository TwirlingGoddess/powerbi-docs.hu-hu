## <a name="define-roles-and-rules-within-power-bi-desktop"></a>Szerepkörök és szabályok definiálása a Power BI Desktopban
A Power BI Desktopban meghatározhat szerepköröket és szabályokat. Amikor közzéteszi a tartalmakat a Power BI-ban, a szerepkör-definíciók is közzé lesznek téve.

Amennyiben szeretné kiaknázni a dinamikus biztonság nyújtotta előnyöket, a kétirányú keresztszűrés engedélyezését be kell kapcsolnia a DirectQueryben. Így a keresztszűrés használata során a biztonsági szűrőt mindkét irányban alkalmazhatja.

![](./media/rls-desktop-define-roles/powerbi-desktop-preview-bi-directional-directquery.png)

Biztonsági szerepkörök definiálásához a következőket teheti.

1. Importálhatja az adatokat a Power BI Desktop-jelentésbe, vagy konfigurálhat egy DirectQuery-kapcsolatot.
   
   > [!NOTE]
   > A Power BI Desktopon belül nem definiálhat szerepköröket az Analysis Services élő kapcsolataihoz. Ezt az Analysis Services-modellben kell megtennie.
   > 
   > 
2. Válassza a **Modellezés** lapot.
3. Válassza a **Szerepkörök kezelése** lehetőséget.
   
   ![](./media/rls-desktop-define-roles/powerbi-desktop-security.png)
4. Kattintson a **Létrehozás** gombra.
   
   ![](./media/rls-desktop-define-roles/powerbi-desktop-security-create-role.png)
5. Adja meg a szerepkör nevét. 
6. Válassza ki a táblát, amelyen alkalmazni kívánja a DAX-szabályt.
7. Adja meg a DAX-kifejezéseket. A kifejezésnek igaz vagy hamis eredményt kell adnia. Például: [Entitásazonosító] = „Érték”.
   
   > [!NOTE]
   > A kifejezésben használhatja a *username()* függvényt. Ne feledje, hogy a Power BI Desktopban a *username()* a *TARTOMÁNY\felhasználónév* formátumot követi. A Power BI szolgáltatásban a függvény a felhasználó egyszerű felhasználónevének formátumát követi. Használhatja a *userprincipalname()* függvényt is, amely a felhasználót minden esetben az egyszerű felhasználónevével adja vissza.
   > 
   > 
   
   ![](./media/rls-desktop-define-roles/powerbi-desktop-security-create-rule.png)
8. Miután összeállította a DAX-kifejezést, a Kifejezés mező fölötti pipára kattintva ellenőrizheti azt.
   
   ![](./media/rls-desktop-define-roles/powerbi-desktop-security-validate-dax.png)
9. Kattintson a **Mentés** gombra.

A Power BI Desktopban nem rendelhet felhasználókat a szerepkörökhöz. Ez a Power BI szolgáltatásban lehetséges. A dinamikus biztonság engedélyezéséhez használja a Power BI Desktopban a *username()* vagy a *userprincipalname()* DAX-függvényt, és konfigurálja a megfelelő kapcsolatokat.

