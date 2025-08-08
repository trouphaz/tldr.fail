# tldr.fail
Site for [tldr.fail](https://tldr.fail)

This modification allows you to use this same test on services that use proxy protocol.  [Here is some info explaining proxy protocol.](https://akmatori.com/blog/understanding-proxy-protocol).  If your service has proxy protocol enabled, the original tldr script will fail because the service will expect the Proxy Protocol headers before the TLS client hello.  The changes to the script allow you to send either V1 or V2 headers, depending on what your service uses.

usage: tldr_fail_test.py [-h] [--addr ADDR] [--port PORT] [--proxy-protocol {v1,v2}] host
