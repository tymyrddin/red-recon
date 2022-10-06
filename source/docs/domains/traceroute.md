# traceroute

`traceroute` (Windows `tracert`) traces the route taken by the packets from our system to the target host. 
The console output shows the routers (hops) connecting us to the target system. Some routers do not respond to 
packets sent by traceroute, and a `*` is used to indicate such a case.

    traceroute cafe.thmredteam.com

```text
traceroute to clinic.thmredteam.com (104.21.93.169), 64 hops max
  1   *  *  * 
  2   45.83.90.145  64,469ms  73,575ms  70,986ms 
  3   *  *  * 
  4   217.138.223.188  53,067ms  52,242ms  55,242ms 
  5   89.44.212.140  52,708ms  55,677ms  53,332ms 
  6   172.71.132.4  57,544ms  52,764ms  53,005ms 
  7   104.21.93.169  52,763ms  64,055ms  53,459ms 
```
