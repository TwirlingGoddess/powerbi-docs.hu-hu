## <a name="validating-the-role-within-power-bi-desktop"></a>Szerepkör érvényesítése a Power BI Desktopban
A szerepkör létrehozása után tesztelheti a szerepkör hatásait a Power BI Desktopban. Ehhez válassza a **Megtekintés szerepkörökként** elemet.

![](./media/rls-desktop-view-as-roles/powerbi-desktop-rls-view-as-roles.png)

A **Megtekintés szerepkörökként** párbeszédpanelen ellenőrizheti, hogy egy adott felhasználó vagy szerepkör mit láthat. Megtekintheti azokat a szerepköröket, amelyeket létrehozott.

![](./media/rls-desktop-view-as-roles/powerbi-desktop-rls-view-as-roles-dialog.png)

Jelölje ki az egyik létrehozott szerepkörét, majd kattintson az **OK** gombra, hogy alkalmazza a szerepkört arra, amit épp megtekintett. A jelentésekből csak a szerepkör számára releváns adatok jelennek meg.

Az **Egyéb felhasználó** beállítással egy adott felhasználót is kiválaszthat. Az egyszerű felhasználónevet (UPN) érdemes megadni, mivel a Power BI szolgáltatás azt használja. Kattintson az **OK** gombra, és a jelentések csak a felhasználó számára elérhető adatokat fogják megjeleníteni. 

![](./media/rls-desktop-view-as-roles/powerbi-desktop-rls-other-user.png)

> [!NOTE]
> A Power BI Desktopban csak akkor fognak megjelenni különböző eredmények, ha DAX-kifejezéseken alapuló dinamikus biztonsági megoldást alkalmaz.
> 
> 

