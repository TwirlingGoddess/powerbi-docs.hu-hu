## <a name="using-the-username-or-userprincipalname-dax-function"></a>A username() és a usernameprincipal() DAX-függvény használata
A *username()* és a *usernameprincipal()* DAX-függvény felhasználható az adatkészletben. Használható a Power BI Desktopban megadott kifejezésekben is. A modell közzétételekor a Power BI szolgáltatásban lesznek felhasználva.

A Power BI Desktopban a *username()* a felhasználót adja eredményül *TARTOMÁNY\Felhasználó* formátumban, a *userprincipalname()* pedig *user@contoso.com* formátumban.

A Power BI szolgáltatásban a *username()* és a *userprincipalname()* eredménye egyaránt a felhasznál egyszerű felhasználóneve (UPN) lesz. Ez egy e-mail-címhez hasonlít.

