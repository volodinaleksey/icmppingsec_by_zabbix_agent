# icmppingsec_by_zabbix_agent
icmppingsec Zabbix simple cheek but by Zabbix Agent.

```
UserParameter=icmppingsec[*], powershell -NoProfile -ExecutionPolicy bypass -Command "Test-Connection -ComputerName $1 -Count 4 | Measure-Object ResponseTime -Average | ForEach-Object { '{0:N5}' -f ($_.Average / 1000) -replace ',', '.'}"
```
