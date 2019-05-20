## Command Lines for Network
* check for the connection to certain ip<br>
ping (+ip) <br>*show the ttl, bytes, time and other detailed information when connecting to the ip, and refresh by intervals*<br>
#### $ ping --help
Usage: ping [OPTION...] HOST ...
Send ICMP ECHO_REQUEST packets to network hosts.

 *Options controlling ICMP request types:*<br>
      --address              send ICMP_ADDRESS packets (root only)
      --echo                 send ICMP_ECHO packets (default)
      --mask                 same as --address
      --timestamp            send ICMP_TIMESTAMP packets
  -t, --type=TYPE            send TYPE packets

*Options valid for all request types:*<br>
  -c, --count=NUMBER         stop after sending NUMBER packets
  -d, --debug                set the SO_DEBUG option
  -i, --interval=NUMBER      wait NUMBER seconds between sending each packet
  -n, --numeric              do not resolve host addresses
  -r, --ignore-routing       send directly to a host on an attached network
      --ttl=N                specify N as time-to-live
  -T, --tos=NUM              set type of service (TOS) to NUM
  -v, --verbose              verbose output
  -w, --timeout=N            stop after N seconds
  -W, --linger=N             number of seconds to wait for response

 *Options valid for --echo requests:*<br>
  -f, --flood                flood ping (root only)
      --ip-timestamp=FLAG    IP timestamp of type FLAG, which is one of
                             "tsonly" and "tsaddr"
  -l, --preload=NUMBER       send NUMBER packets as fast as possible before
                             falling into normal mode of behavior (root only)
  -p, --pattern=PATTERN      fill ICMP packet with given pattern (hex)
  -q, --quiet                quiet output
  -R, --route                record route
  -s, --size=NUMBER          send NUMBER data octets

  -?, --help                 give this help list
      --usage                give a short usage message
  -V, --version              print program version<br>


* check for the connection to certain DNS<br>
traceroute (+dns address)<br>
*show the detailed router ips between source ip and destination ip, as well as connecting time*<br>

#### $ traceroute --help
Usage: traceroute [OPTION...] HOST
Print the route packets trace to network host.

  -f, --first-hop=NUM        set initial hop distance, i.e., time-to-live
  -g, --gateways=GATES       list of gateways for loose source routing
  -I, --icmp                 use ICMP ECHO as probe
  -m, --max-hop=NUM          set maximal hop count (default: 64)
  -M, --type=METHOD          use METHOD (`icmp' or `udp') for traceroute
                             operations, defaulting to `udp'
  -p, --port=PORT            use destination PORT port (default: 33434)
  -q, --tries=NUM            send NUM probe packets per hop (default: 3)
      --resolve-hostnames    resolve hostnames
  -t, --tos=NUM              set type of service (TOS) to NUM
  -w, --wait=NUM             wait NUM seconds for response (default: 3)
  -?, --help                 give this help list
      --usage                give a short usage message
  -V, --version              print program version<br>


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQyMzEyNDAzMV19
-->