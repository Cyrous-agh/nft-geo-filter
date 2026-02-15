# nft-geo-filter
NFT Geo Filter rule for blocking IPs by location or configuration on Linux
# nft-geo-filter

A Python-based GeoIP filter for **nftables** on Linux systems.  
Blocks or allows network traffic based on country IP ranges.

---

🇬🇧 English

nft-geo-filter is a Python-based GeoIP filtering tool for nftables on Linux.
It downloads country-based IP ranges and applies them as nftables rules.

Features

Country-based GeoIP filtering

IPv4 and IPv6 support

Allow or drop policy

Automatic IP list download

Designed for servers and firewalls



Installation
sudo cp nft-geo-filter /bin/nft-geo-filter
sudo chmod +x /bin/nft-geo-filter

Usage

sage: nft-geo-filter [-h] [-v] [-l NFT_LOCATION] [-a] [--allow-established] [-c] [--provider {ipdeny.com,ipverse.net}] [-f {ip,ip6,inet,netdev}] [-n TABLE_NAME] [-i INTERFACE] [--no-ipv4] [--no-ipv6] [-e IPS] [--log-accept]
                      [--log-accept-prefix LOG_ACCEPT_PREFIX] [--log-accept-level LOG_ACCEPT_LEVEL] [--log-drop] [--log-drop-prefix LOG_DROP_PREFIX] [--log-drop-level LOG_DROP_LEVEL]
                      country [country ...]


for Update->
sudo nft-geo-filter --country US --provider ipdeny.com


sudo /bin/nft-geo-filter --table-family netdev --interface ->Interface-Name Interface Name<- --log-drop --log-drop-prefix "GEO-BLOCK-INTGRESS: " ru ch <----country 
sudo /bin/nft-geo-filter --provider ipdeny.com -f inet -n geo-filter -i eth1 --log-drop --log-drop-prefix "GEO-BLOCK-INT:" ru ch 
sudo /bin/nft-geo-filter --table-family inet --table-name geo-in --log-drop --log-drop-prefix "Counter : " --counter RU CH
sudo /bin/nft-geo-filter --table-family inet --table-name geo-out --log-drop --log-drop-prefix "Counter   : " --counter RU CH

---

## 🇩🇪 Deutsch

### Beschreibung
`nft-geo-filter` ist ein in **Python** geschriebenes Tool zur GeoIP-Filterung mit **nftables**.  
Es lädt IP-Ranges nach Ländern (IPv4 & IPv6) von öffentlichen Providern und erstellt automatisch passende nftables-Regeln.

### Funktionen
- GeoIP-Filtering nach Ländern
- IPv4 & IPv6 Unterstützung
- Allow- oder Drop-Modus
- Automatischer Download der IP-Listen
- Geeignet für Server & Firewalls

### Installation
```bash
sudo cp nft-geo-filter /bin/nft-geo-filter
sudo chmod +x /bin/nft-geo-filter
