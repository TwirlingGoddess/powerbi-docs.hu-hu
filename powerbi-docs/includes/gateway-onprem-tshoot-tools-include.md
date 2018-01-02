## <a name="tools-for-troubleshooting"></a>Hibaelhárítási eszközök
<a name="logs" />

### <a name="collecting-logs-from-the-gateway-configurator"></a>A naplók összegyűjtése az átjárókonfigurálóról
Számos naplót lekérdezhet az átjáróhoz, és mindig a naplók lekérdezésével érdemes kezdenie a hibaelhárítást. Az átjáró telepítése után a felhasználói felületen keresztül kérdezheti le a legegyszerűbben a naplókat. A **Helyszíni adatátjáró** felhasználói felületen válassza a **Diagnosztika** lehetőséget, majd a **Naplók exportálása** hivatkozást az oldal alján (az alábbi ábrán látható módon).

![Helyszíni adatátjáró naplói a felhasználói felületen](./media/gateway-onprem-tshoot-tools-include/gateway-onprem-UI-logs.png)

**Telepítőnaplók**

    %localappdata%\Temp\On-premises_data_gateway_*.log

**Konfigurációs naplók**

    %localappdata%\Microsoft\On-premises Data Gateway\GatewayConfigurator*.log

**Helyszíni adatátjáró szolgáltatás naplói**

    C:\Users\PBIEgwService\AppData\Local\Microsoft\On-premises Data Gateway\Gateway*.log

### <a name="event-logs"></a>Eseménynaplók
A **helyszíni adatátjáró szolgáltatás** eseménynaplói az **Alkalmazás- és szolgáltatásnaplók** területen találhatók.

![Helyszíni adatátjáró eseménynaplói](./media/gateway-onprem-tshoot-tools-include/on-prem-data-gateway-event-logs.png)

<a name="fiddler" />

### <a name="fiddler-trace"></a>Fiddler-nyomkövetés
A [Fiddler](http://www.telerik.com/fiddler) a Telerik ingyenes eszköze, amely a HTTP-adatforgalom figyelésére használható.  Nyomon követheti a Power BI szolgáltatás és az ügyfélszámítógép közötti adatforgalmat. Az eszköz hibaüzenetek és egyéb, kapcsolódó információk megjelenítésére is képes.

![](media/gateway-onprem-tshoot-tools-include/fiddler.png)

