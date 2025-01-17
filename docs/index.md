---
organization: francois2metz
category: ["internet"]
brand_color: "#0d0b30"
display_name: "Gandi"
short_name: "Gandi"
description: "Steampipe plugin for querying your domains on Gandi."
og_description: "Query Gandi with SQL! Open source CLI. No DB required."
og_image: "/images/plugins/francois2metz/gandi-social-graphic.png"
icon_url: "/images/plugins/francois2metz/gandi.svg"
---

# Gandi + Steampipe

[Gandi](https://gandi.net/) is a registrar and an hosting company.

[Steampipe](https://steampipe.io) is an open source CLI to instantly query cloud APIs using SQL.

For example:

```sql
select
  fqdn,
  tld,
  owner
from
  gandi_domain
```

```
+--------------------+------+---------------+
| fqdn               | tld  | owner         |
+--------------------+------+---------------+
| caresteouvert.fr   | fr   | francois2metz |
| 2metz.fr           | fr   | francois2metz |
+--------------------+------+---------------+
```

## Documentation

- **[Table definitions & examples →](/plugins/francois2metz/gandi/tables)**

## Get started

### Install

Download and install the latest Gandi plugin:

```bash
steampipe plugin install francois2metz/gandi
```

### Configuration

Installing the latest gandi plugin will create a config file (`~/.steampipe/config/gandi.spc`) with a single connection named `gandi`:

```hcl
connection "gandi" {
  plugin = "francois2metz/gandi"

  # The API Key (get it on your account: https://account.gandi.net/)
  key = "YOUR_GANDI_API_KEY"
}
```

You can also use environment variables:

- `GANDI_KEY`: Your Gandi API Key

## Get Involved

* Open source: https://github.com/francois2metz/steampipe-plugin-gandi
