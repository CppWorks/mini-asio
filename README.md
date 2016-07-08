# xxsocket
A mini simplest cross platform posix socket API wrapper, support win32  &amp; linux  &amp; ios &amp; android &amp; wp8 &amp; wp8.1-universal &amp; win10-universal

support IPv6-only network.

Usage:

1. Only compile src\xxsocket.cpp src\xxsocket.h src\politedef.h with your project; For gcc, should add --std=c++11 compile flag<br />
2. demo code:
```
#include "xxsocket.h"
using namespace purelib::inet;
void test_connect() 
{
   xxsocket clientsock;
   // The interface xpconnect_n will detect whether localhost is IPV6 only network automatically
   // and connect the ipv4 server by V4MAPPED address.
   if(0 == clientsock.xpconnect_n("www.baidu.com", 443, 5/* connect timeout 5 seconds */))
   {
       printf("connect succeed\n");
   }
}
```
