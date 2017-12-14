## <a name="update-to-the-latest-version"></a>Frissítés a legújabb verzióra
Ha az átjáró verziója elavult, számos probléma felmerülhet.  Általában véve célszerű meggyőződnie arról, hogy a legújabb verzióval rendelkezik.  Ha az átjárót már legalább egy hónapja nem frissítette, javasoljuk, hogy telepítse az átjáró legújabb verzióját, majd nézze meg, hogy jelentkezik-e ugyanaz a probléma.

## <a name="common-issues"></a>Gyakori problémák
Az alábbiakban ismertetünk néhány gyakori problémát a megoldásával együtt. Ezek az információk már több, az internetelérést korlátozó ügyfelünkön segítettek.

<iframe width="560" height="315" src="https://www.youtube.com/embed/-t7RO6mHATI?showinfo=0" frameborder="0" allowfullscreen></iframe>

### <a name="authentication-to-proxy-server"></a>Hitelesítés a proxykiszolgálón
Előfordulhat, hogy a proxyn egy tartományi felhasználói fióknak hitelesítenie kell magát. Az átjáró alapértelmezés szerint a Windows-szolgáltatás bejelentkezési felhasználójának SID azonosítóját használja. Általában megoldja a problémát, ha a bejelentkezési felhasználót módosítja egy tartományi felhasználóra. További tájékoztatást [Az átjárószolgáltatás fiókjának módosítása egy tartományi felhasználóra](../service-gateway-proxy.md#changing-the-gateway-service-account-to-a-domain-user) című cikkben talál.

### <a name="your-proxy-only-allows-ports-80-and-443-traffic"></a>A proxy csak a 80-as és a 443-as porton engedélyez forgalmat
Vannak proxyk, amelyek a 80-as és a 443-as portra korlátozzák a forgalmat. Az Azure Service Busszal zajló kommunikáció alapértelmezés szerint a 443-astól különböző portokon történik.

Kényszerítheti az átjárót arra, hogy közvetlen TCP helyett HTTPS-en kommunikáljon az Azure Service Busszal. A *Microsoft.PowerBI.DataMovement.Pipeline.GatewayCore.dll.config* fájlt kell ehhez módosítania. Módosítsa az `AutoDetect` értéket `Https`-re. Ez a fájl alapértelmezés szerint a *C:\Program Files\On-premises data gateway* mappában található.

```
<setting name="ServiceBusSystemConnectivityModeString" serializeAs="String">
    <value>Https</value>
</setting>
```

## <a name="installation"></a>Telepítés
### <a name="error-failed-to-add-user-to-group---2147463168---pbiegwservice---performance-log-users---"></a>Hiba: Nem sikerült hozzáadni a felhasználót a csoporthoz.  (-2147463168   PBIEgwService   Teljesítménynapló felhasználói   )
Ez a hibaüzenet akkor jelenik meg, ha egy tartományvezérlőre próbálja telepíteni az átjárót. A tartományvezérlőre történő telepítés nem támogatott. Az átjárót olyan gépre kell telepítenie, amely nem tartományvezérlő.

