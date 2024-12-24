<p style="text-align:center;">A set of routers under a single technical administration, using an interior gateway protocol and common metrics to route packets within the AS, and using an exterior gateway protocol to route packets to other ASes</p>

```Example
NET1 .... ASX <----> ASY .... NET2
```

ASX knows how to reach NET1, we assume it knows how to direct packets. Likewise, ASY knows how to reach NET2.

In order for traffic to reach NET1 from NET2 between ASX and ASY, ASX has to announce NET1 to ASY using an exterior routing protocol. This means that ASX is willing to accept traffic directed to NET1 from ASY. 

For traffic to flow, ASY has to accept this routing advertisement and use it. This is all up to ASY, whether it wants to receive information and reach NET1.

Ideally, the announcement and acceptance policies of ASX and ASY are symmetrical.

**NOTE** in more complex topologies than this example, traffic from NET1 to NET2 may not necessarily take the same path as NET2 to NET1. This is called **Asymmetrical routing**. It may be a requirement for mobile hosts and inherently asymmetrical situations, such as satelite donwload and a modem upload connection.

Policies are configured for groups of prefixes, known as ASes. An AS has a globally unique number (ASN) associated with it, the number is used in both the exchange of exterior routing information (between ASes), and as an identifier of the AS itself.

In routing terms, an AS will normally use one or more interior gateway protocols (IGPs) when exchanging reachability information within its own AS.