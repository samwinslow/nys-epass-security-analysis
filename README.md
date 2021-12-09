# nys-epass-security-analysis
Privacy &amp; security analysis of the NYS Excelsior Pass app

## Configuring mitmproxy

- Install [mitmproxy](https://github.com/mitmproxy/mitmproxy/) with either a prebuilt binary,
or download from source and follow the build instructions.
- Start mitmproxy, configure any necessary inbound and outbound firewall rules for port 8080 or your chosen port.
- Configure proxy settings on your mobile device. On iOS, Settings > Wifi > (network) > ℹ > Configure Proxy.
Use your computer's local IP as the Server, 8080 as the Port. No authentication.
- Disable "Private Address" which encrypts DNS traffic.
- Navigate to [mitm.it](http://mitm.it/) on your mobile device. Download, install, and trust the SSL certificate.

## Intercepting requests with mitmdump

- Clone [mitmproxy](https://github.com/mitmproxy/mitmproxy/) and locate the `har_dump.py` script (in `examples/contrib` as of v7.0.x)
- Run `mitmdump -s ~/path/to/har_dump.py --set hardump=./dump.har`. This will dump traffic to a [HAR file](https://en.wikipedia.org/wiki/HAR_(file_format)). 

## Parsing & understanding the results

### TODO
