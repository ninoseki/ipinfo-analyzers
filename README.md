# ipinfo-analyzers

Cortex Analyzer for IPinfo.

## Supported API endpoints

### Details (ipinfo.io/{IP})

```bash
$ echo '{ "data": "66.87.125.72", "dataType":"ip", "config":{ "api_key":"YOUR_API_KEY", "service":"details" }}' | python ipinfo_analyzer.py | jq .
{
  "success": true,
  "summary": {
    "taxonomies": [
      {
        "level": "info",
        "namespace": "IPinfo",
        "predicate": "Country",
        "value": "US"
      },
      {
        "level": "info",
        "namespace": "IPinfo",
        "predicate": "ASN",
        "value": "AS10507"
      }
    ]
  },
  "artifacts": [
    {
      "type": "fqdn",
      "value": "ip-66-87-125-72.spfdma.spcsdns.net"
    },
    {
      "type": "domain",
      "value": "spcsdns.net"
    },
    {
      "type": "ip",
      "value": "66.87.125.0/24"
    },
    {
      "type": "domain",
      "value": "sprint.com"
    }
  ],
  "full": {
    "ip": "66.87.125.72",
    "hostname": "ip-66-87-125-72.spfdma.spcsdns.net",
    "city": "Springfield",
    "region": "Massachusetts",
    "country": "US",
    "loc": "42.1210,-72.4896",
    "postal": "01129",
    "phone": "413",
    "asn": {
      "asn": "AS10507",
      "name": "Sprint Personal Communications Systems",
      "domain": "spcsdns.net",
      "route": "66.87.125.0/24",
      "type": "isp"
    },
    "company": {
      "name": "Sprint Springfield POP",
      "domain": "sprint.com",
      "type": "isp"
    },
    "carrier": {
      "name": "Sprint Corporation",
      "mcc": "310",
      "mnc": "120"
    }
  }
}
```

### Hosted domains (ipinfo.io/domains/{IP})

```bash
$ echo '{ "data": "216.239.34.21", "dataType":"ip", "config":{ "api_key":"YOUR_API_KEY", "service":"hosted_domains" }}' | python ipinfo_analyzer.py | jq .
{
  "success": true,
  "summary": {
    "taxonomies": [
      {
        "level": "info",
        "namespace": "IPinfo",
        "predicate": "HostedDomains",
        "value": "25 records"
      }
    ]
  },
  "artifacts": [
    {
      "type": "ip",
      "value": "216.239.32.0/19"
    },
    {
      "type": "domain",
      "value": "lezhin.com"
    },
    {
      "type": "domain",
      "value": "ingress.com"
    },
    {
      "type": "domain",
      "value": "sscadda.com"
    },
    {
      "type": "domain",
      "value": "humaliwalayazadar.com"
    },
    {
      "type": "fqdn",
      "value": "businesslive.co.za"
    },
    {
      "type": "domain",
      "value": "padpadblog.com"
    },
    {
      "type": "domain",
      "value": "seleniumhq.org"
    },
    {
      "type": "domain",
      "value": "lowongankerja15.com"
    },
    {
      "type": "domain",
      "value": "screencastify.com"
    },
    {
      "type": "domain",
      "value": "chinagfw.org"
    },
    {
      "type": "domain",
      "value": "royallepage.ca"
    },
    {
      "type": "domain",
      "value": "fanpagekarma.com"
    },
    {
      "type": "domain",
      "value": "operatorsekolah.com"
    },
    {
      "type": "domain",
      "value": "sarkarinaukricareer.in"
    },
    {
      "type": "domain",
      "value": "swap.com"
    },
    {
      "type": "domain",
      "value": "layanjer.com"
    },
    {
      "type": "domain",
      "value": "gurusd.net"
    },
    {
      "type": "domain",
      "value": "mostajad.com"
    },
    {
      "type": "domain",
      "value": "thinkwave.com"
    },
    {
      "type": "domain",
      "value": "rejinpaul.com"
    },
    {
      "type": "domain",
      "value": "polymer-project.org"
    },
    {
      "type": "domain",
      "value": "kalvisolai.com"
    },
    {
      "type": "domain",
      "value": "social-dog.net"
    },
    {
      "type": "domain",
      "value": "gsmhelpful.com"
    },
    {
      "type": "domain",
      "value": "webupd8.org"
    }
  ],
  "full": {
    "ip": "216.239.34.21",
    "asn": "AS15169",
    "count": 152151,
    "range": "216.239.32.0/19",
    "domains": [
      "lezhin.com",
      "ingress.com",
      "sscadda.com",
      "humaliwalayazadar.com",
      "businesslive.co.za",
      "padpadblog.com",
      "seleniumhq.org",
      "lowongankerja15.com",
      "screencastify.com",
      "chinagfw.org",
      "royallepage.ca",
      "fanpagekarma.com",
      "operatorsekolah.com",
      "sarkarinaukricareer.in",
      "swap.com",
      "layanjer.com",
      "gurusd.net",
      "mostajad.com",
      "thinkwave.com",
      "rejinpaul.com",
      "polymer-project.org",
      "kalvisolai.com",
      "social-dog.net",
      "gsmhelpful.com",
      "webupd8.org"
    ]
  }
}
```
