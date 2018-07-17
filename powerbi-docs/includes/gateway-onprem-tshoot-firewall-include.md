## <a name="firewall-or-proxy"></a>Tűzfalak és proxyk
Az átjáró proxyinformációinak megadásával kapcsolatban további információt a [Proxybeállítások konfigurálása a Power BI-átjárókhoz](../service-gateway-proxy.md) leírásban talál.

A PowerShell parancssorból a [Test-NetConnection](https://docs.microsoft.com/powershell/module/nettcpip/test-netconnection) parancs futtatásával ellenőrizheti, hogy a tűzfal vagy proxy blokkolja-e a kapcsolatokat. Ez teszteli a kapcsolódást az Azure Service Bushoz. Ez csakis a hálózati kapcsolatot teszteli, és nem érinti a felhőkiszolgáló szolgáltatást vagy az átjárót. Ez a parancs segít megállapítani, hogy a gépe képes-e az internetkapcsolatra.

    Test-NetConnection -ComputerName watchdog.servicebus.windows.net -Port 9350

> [!NOTE]
> A Test-NetConnection csak a Windows Server 2012 R2 vagy újabb rendszereken érhető el. Ezenkívül a Windows 8.1 és újabb rendszereken is elérhető. A korábbi verziójú operációs rendszereken a Telnet használatával lehetett tesztelni a portkapcsolatokat.
> 
> 

Az eredményeknek a következőképpen kell kinéznie. A TcpTestSucceeded értéket érdemes figyelni. Ha a **TcpTestSucceeded** értéke nem *true*, lehet, hogy egy tűzfal blokkolja a kapcsolódást.

    ComputerName           : watchdog.servicebus.windows.net
    RemoteAddress          : 70.37.104.240
    RemotePort             : 5672
    InterfaceAlias         : vEthernet (Broadcom NetXtreme Gigabit Ethernet - Virtual Switch)
    SourceAddress          : 10.120.60.105
    PingSucceeded          : False
    PingReplyDetails (RTT) : 0 ms
    TcpTestSucceeded       : True

Ha igazán alapos szeretne lenni, helyettesítse a **ComputerName** és a **Port** értékeket a későbbiekben a [portok](../service-gateway-onprem.md#ports) alatt felsorolt értékekkel

A tűzfal blokkolhatja az Azure Service Bus és az Azure adatközpontok közötti kapcsolatokat is. Ha ez az eset áll fenn, engedélyezze (oldja fel a blokkolást) az adatközpontok régiójának IP-címeit. Az Azure IP-címek listáját [itt](https://www.microsoft.com/download/details.aspx?id=41653) érheti el.

