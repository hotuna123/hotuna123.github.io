**VPN Troubleshooting Guide on Xi Leap**

*Introduction*

If it was a blip or if the tunnel is down for more than 30 minutes which could be a serious issue. On-prem CVMs/PCVM communication to Xi side CVM/PCVM communication happens through the tunnel. If a tunnel is down, it will affect all the replication traffic coming from the on-prem side and our replications will not work.



Troubleshooting commands

```
nuclei remote_connection.health_check_all  
```

```
nuclei vpn_gateway.list
```

```
nuclei vpn_gateway.get <vpn gw uuid> | grep public_ip
```

```
tailf /var/log/charon.log
```

```
sudo tcpdump -nvvi eth0 udp
```

