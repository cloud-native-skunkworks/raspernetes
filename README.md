## Raspbernetes


<img src="images/IMG_4819.jpeg" width="400px" />

This is a data sheet of information required to build a high performance raspberry pi cluster with MicroK8s Kubernetes for home use. It should be sufficient for most use cases and can be extended as needed to meet your needs. 

This is more of a starting point than a complete guide.


### Bill of materials

| Item                      | Link                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Count | Price | Total (GBP) |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|-------|--------|
| Enclosure                 | [Pi hut](https://thepihut.com/collections/raspberry-pi-cluster-cases/products/ssd-cluster-case-for-raspberry-pi)                                                                                                                                                                 | 1     | 55  | 55   |
| Raspberry Pi 4 b 8gb      | [Amazon](https://www.amazon.co.uk/Raspberry-PI-4B-8GB-RAM/dp/B0899VXM8F/ref=sr_1_4?crid=1O4MJ36EG0CB9&keywords=raspberry+pi+4b&qid=1653982026&sprefix=raspberry+pi+4+b%2Caps%2C53&sr=8-4)                                                                                                                                                                                                                                                                                              | 4     | 87.2  | 348.8  |
| Patch cables              | [Amazon](https://www.amazon.co.uk/C2G-Cat5e-Ethernet-Network-Unshielded-Blue/dp/B00H8XNDTM/ref=sr_1_2_sspa?crid=1Y9FAZ9NW12WA&keywords=short%2Bethernet%2Bcable%2BPoE&qid=1653982102&sprefix=short%2Bethernet%2Bcable%2Bpoe%2Caps%2C50&sr=8-2-spons&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExNkxZMzJXTlBaVjFOJmVuY3J5cHRlZElkPUEwODAxNzQ3MUJCTExQMzFYM0o5OCZlbmNyeXB0ZWRBZElkPUEwNzY4MDk1MjhGVlhaSVIwRURBQiZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU&th=1) | 4     | 2.1   | 8.4    |
| USB to Sata cables        | [Amazon](https://www.amazon.co.uk/Benfei-SATA-Adapter-Supports-UASP/dp/B07F7WDZGT/ref=sr_1_5?crid=3UWMTIEVJWY30&keywords=usb+to+sata+raspberry+pi&qid=1653982159&sprefix=usb+to+sata+raspberry+pi+%2Caps%2C51&sr=8-5)                                                                                                                                                                                                                                                                  | 4     | 6.29  | 25.16  |
| PoE Router                | [Ebay](https://www.ebay.co.uk/itm/363019690583?epid=2213522312&hash=item5485a8e257:g:1FEAAOSwtgFij0t7)                                                                                                                                                                                                                                                                                                                                                                                | 1     | 68.36 | 68.36  |
| SSD                       | [Amazon](https://www.amazon.co.uk/Kingston-SA400S37-240G-Solid-State/dp/B01N5IB20Q/ref=sr_1_3?adgrpid=52819915083&gclid=Cj0KCQjw-daUBhCIARIsALbkjSbEQr8Xnx4L_hlkWGCtewOSNi6SnnMzRcF-OGGTNwjb9ddEvRQO5vkaAlAEEALw_wcB&hvadid=259142379046&hvdev=c&hvlocphy=1007014&hvnetw=g&hvqmt=e&hvrand=16323803481848172762&hvtargid=kwd-296614513627&hydadcr=19074_1719650&keywords=kingston+240gb+ssd&qid=1653982564&sr=8-3)                                                                      | 4     | 43.89 | 175.56 |
| Fans                      | [Amazon](https://www.amazon.co.uk/gp/product/B00HWGZT3I/ref=ppx_yo_dt_b_asin_title_o08_s00?ie=UTF8&psc=1)                                                                                                                                                                                                                                                                                                                                                                              | 2     | 7.50  | 15     |
| USB to 3/4-Pin PWM PC Fan |  [Amazon](https://www.amazon.co.uk/gp/product/B09BV9CKXJ/ref=ppx_yo_dt_b_asin_image_o03_s00?ie=UTF8&psc=1)                                                                                                                                                                                                                                                                                                                                                                             | 1     | 8.59  | 8.59   |
| PoE Hat                   | [Pi hut](https://thepihut.com/products/raspberry-pi-poe-plus-hat)                                                                                                                                                                                                                                                                                                                                                                                                                      | 4     | 19.80 | 79.20  |
| MicroSD card              | [Amazon](https://www.amazon.co.uk/Gigastone-5-Pack-Class10-Nintendo-Samsung/dp/B07P192KFQ/ref=sr_1_7_sspa?crid=2XH3DF34VXK33&keywords=raspberry%2Bpi%2Bmicro%2Bsd%2Bcard%2B32gb&qid=1653984545&sprefix=raspebrry%2Bpi%2B%2Caps%2C58&sr=8-7-spons&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUFONExXMVJLRUVMQVMmZW5jcnlwdGVkSWQ9QTA4MjQ4OTAxSk00NllHRFJDV1lEJmVuY3J5cHRlZEFkSWQ9QTAzMjk0NjUxVlpaQlk1NVFTNTFSJndpZGdldE5hbWU9c3BfbXRmJmFjdGlvbj1jbGlja1JlZGlyZWN0JmRvTm90TG9nQ2xpY2s9dHJ1ZQ&th=1)     | 1     | 24.98 | 24.98  |
|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |       |       | 809.55 |


#### Note on router vs switch

In the photo I have a tp-link 5 port switch but the BoM includes a newer PoE router which I prefer. 
This is useful if you want to transport your cluster and retain the IPAM information in the router. 
The switch is managed but the router has a few other features that make it a better option. 
If you want a switch like in the photo here are the details:
- 40.97 (GBP) [Amazon](https://www.amazon.co.uk/TP-Link-TL-SG1005P-Ethernet-Configuration-Required/dp/B0769C24T1/ref=sr_1_3?adgrpid=74825115520&gclid=Cj0KCQjw-daUBhCIARIsALbkjSabwCFEOLxEmALeaLfBSJDHGUrWdh_ifiwSxUxGodLibDOFFd-cQvcaAvgsEALw_wcB&hvadid=356644610847&hvdev=c&hvlocphy=1007014&hvnetw=g&hvqmt=e&hvrand=3002664512498092811&hvtargid=kwd-317217279028&hydadcr=25426_1819469&keywords=tp+link+5+port+poe+switch&qid=1653983657&sr=8-3)

### Software

- [Ubuntu 22.04](https://ubuntu.com/download/raspberry-pi)
- [MicroK8s](https://ubuntu.com/tutorials/how-to-kubernetes-cluster-on-raspberry-pi?&_ga=2.92060063.463304713.1653983297-30417302.1648472081#1-overview)


#### Note on installation

It is important to install `/var/snap` under the SSD rather than the micro SD card for optimal performance.
