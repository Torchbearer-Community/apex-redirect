# torchbearer.community → www redirect

The Torchbearer Community website lives on Cloudflare Pages at
**www.torchbearer.community**. Cloudflare Pages can only be reached through a
CNAME record, and DNS does not allow a CNAME at the root of a domain, so the
bare domain needs a server of its own that holds an HTTPS certificate and
forwards visitors to www.

This repository is that server. GitHub Pages serves it at
`torchbearer.community` (see `CNAME`) with a certificate it manages, and both
`index.html` and `404.html` send every request to the same path on www.

DNS (Namecheap, host `@`): four A records `185.199.108.153`,
`185.199.109.153`, `185.199.110.153`, `185.199.111.153` and four AAAA records
`2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`,
`2606:50c0:8003::153`. Nothing here needs to change unless GitHub changes
those addresses.
