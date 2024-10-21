# Flag

**185.101.34.119**
# Prompt

>Use Censys to find a computer in Oslo that runs Ubuntu 20.04 and tcp port 2233 and 8069 are open. What is the IP?

# Solution

Using the website and tool **search.censys.io** to find and monitor every server on the Internet.

Search for hosts with search-prompt:
> ((location.city= "Oslo") and services.software.vendor=`Ubuntu`) and (services.port=`2233` and services.port=`8069`)

![[censys_solution1.png]]