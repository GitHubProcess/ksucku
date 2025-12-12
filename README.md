{
  "log": {
    "level": "warn",
    "timestamp": true
  },
  "dns": {
    "servers": [
      {
        "tag": "dns-remote",
        "address": "udp://1.1.1.1",
        "address_resolver": "dns-direct"
      },
      {
        "tag": "dns-trick-direct",
        "address": "https://sky.rethinkdns.com/",
        "detour": "direct-fragment"
      },
      {
        "tag": "dns-direct",
        "address": "1.1.1.1",
        "address_resolver": "dns-local",
        "detour": "direct"
      },
      {
        "tag": "dns-local",
        "address": "local",
        "detour": "direct"
      },
      {
        "tag": "dns-block",
        "address": "rcode://success"
      }
    ],
    "rules": [
      {
        "domain": "cp.cloudflare.com",
        "server": "dns-remote",
        "rewrite_ttl": 3000
      },
      {
        "domain_suffix": ".ru",
        "server": "dns-direct"
      },
      {
        "rule_set": [
          "geoip-ru",
          "geosite-ru"
        ],
        "server": "dns-direct"
      }
    ],
    "final": "dns-remote",
    "static_ips": {
      "sky.rethinkdns.com": [
        "104.17.147.22",
        "104.17.148.22",
        "104.18.0.48",
        "104.18.1.48",
        "2606:4700::6812:130",
        "2606:4700::6812:30"
      ]
    },
    "independent_cache": true
  },
  "inbounds": [
    {
      "type": "tun",
      "tag": "tun-in",
      "mtu": 9000,
      "inet4_address": "172.19.0.1/28",
      "auto_route": true,
      "strict_route": true,
      "endpoint_independent_nat": true,
      "stack": "gvisor",
      "sniff": true
    },
    {
      "type": "mixed",
      "tag": "mixed-in",
      "listen": "127.0.0.1",
      "listen_port": 12334,
      "sniff": true,
      "sniff_override_destination": true
    },
    {
      "type": "direct",
      "tag": "dns-in",
      "listen": "127.0.0.1",
      "listen_port": 16450
    }
  ],
  "outbounds": [
    {
      "type": "selector",
      "tag": "select",
      "outbounds": [
        "auto",
        "1🇳🇱@FREE2CONFIG   § 0",
        "2🇵🇱@FREE2CONFIG   § 1",
        "3🇷🇺@FREE2CONFIG  § 2",
        "4🇩🇪@FREE2CONFIG     § 3",
        "5🇩🇪@FREE2CONFIG     § 4",
        "6🇩🇪@FREE2CONFIG     § 5",
        "7🇩🇪@FREE2CONFIG     § 6",
        "8🇷🇺@FREE2CONFIG    § 7",
        "9🇩🇪@FREE2CONFIG    § 8",
        "10🇩🇪@FREE2CONFIG  § 9",
        "11🇩🇪@FREE2CONFIG     § 10",
        "12🇩🇪@FREE2CONFIG     § 11",
        "13🇩🇪@FREE2CONFIG     § 12",
        "14🇩🇪@FREE2CONFIG    § 13",
        "15🇩🇪@FREE2CONFIG     § 14",
        "16🇫🇷@FREE2CONFIG    § 15",
        "17🇩🇪@FREE2CONFIG    § 16",
        "18🇪🇪@FREE2CONFIG   § 17",
        "19🇩🇪@FREE2CONFIG     § 18",
        "20🇩🇪@FREE2CONFIG    § 19",
        "21🇦🇪@FREE2CONFIG   § 20",
        "22🇷🇺@FREE2CONFIG    § 21",
        "23🇩🇪@FREE2CONFIG     § 22",
        "24🇩🇪@FREE2CONFIG    § 23",
        "25🇩🇪@FREE2CONFIG     § 24",
        "26🇩🇪@FREE2CONFIG     § 25",
        "27🇩🇪@FREE2CONFIG     § 26",
        "28🇩🇪@FREE2CONFIG     § 27",
        "29🇩🇪@FREE2CONFIG     § 28",
        "30🇩🇪@FREE2CONFIG    § 29",
        "🇩🇪@FREE2CONFIG     § 30",
        "🇩🇪@FREE2CONFIG     § 31",
        "🇩🇰@FREE2CONFIG   § 32",
        "🇩🇪@FREE2CONFIG     § 33",
        "🇩🇪@FREE2CONFIG     § 34",
        "🇺🇸@FREE2CONFIG   § 35",
        "🇷🇺@FREE2CONFIG    § 36",
        "🇹🇷@FREE2CONFIG   § 37",
        "🇩🇪@FREE2CONFIG   § 38",
        "🇩🇪@FREE2CONFIG   § 39",
        "🇩🇪@FREE2CONFIG   § 40",
        "🇩🇪@FREE2CONFIG   § 41",
        "🇳🇱@FREE2CONFIG   § 42",
        "🇩🇪@FREE2CONFIG   § 43",
        "🇩🇪@FREE2CONFIG   § 44",
        "🇩🇪@FREE2CONFIG   § 45",
        "🇩🇪@FREE2CONFIG   § 46",
        "🇩🇪@FREE2CONFIG   § 47",
        "🇩🇪@FREE2CONFIG   § 48",
        "🇷🇺@FREE2CONFIG   § 49",
        "🇩🇪@FREE2CONFIG   § 50",
        "🇩🇪@FREE2CONFIG   § 51",
        "🇩🇪@FREE2CONFIG   § 52",
        "🇩🇪@FREE2CONFIG   § 53",
        "🇩🇪@FREE2CONFIG   § 54",
        "🇩🇪@FREE2CONFIG   § 55",
        "🇩🇪@FREE2CONFIG   § 56",
        "🇩🇪@FREE2CONFIG   § 57",
        "🇦🇲@FREE2CONFIG   § 58",
        "🇩🇪@FREE2CONFIG   § 59",
        "🇵🇱@FREE2CONFIG   § 60",
        "🇫🇮@FREE2CONFIG   § 61",
        "🇷🇺@FREE2CONFIG   § 62",
        "🇪🇸@FREE2CONFIG   § 63",
        "🇩🇪@FREE2CONFIG   § 64",
        "🇩🇪@FREE2CONFIG   § 65",
        "🇩🇪@FREE2CONFIG   § 66",
        "🇩🇪@FREE2CONFIG   § 67",
        "🇫🇷@FREE2CONFIG   § 68",
        "🇩🇪@FREE2CONFIG   § 69",
        "🇩🇪@FREE2CONFIG   § 70",
        "🇩🇪@FREE2CONFIG   § 71",
        "🇺🇸@FREE2CONFIG   § 72",
        "🇸🇪@FREE2CONFIG   § 73",
        "🇩🇪@FREE2CONFIG   § 74",
        "🇩🇪@FREE2CONFIG   § 75",
        "🇦🇪@FREE2CONFIG   § 76",
        "🇺🇸@FREE2CONFIG   § 77",
        "🇦🇲@FREE2CONFIG   § 78",
        "🇫🇷@FREE2CONFIG   § 79",
        "🇺🇸@FREE2CONFIG   § 80",
        "🇵🇱@FREE2CONFIG   § 81",
        "🇨🇦@FREE2CONFIG   § 82",
        "🇺🇸@FREE2CONFIG   § 83",
        "🇦🇺@FREE2CONFIG   § 84",
        "🇰🇿@FREE2CONFIG   § 85",
        "🇫🇷@FREE2CONFIG   § 86",
        "🇩🇪@FREE2CONFIG   § 87",
        "🇳🇱@FREE2CONFIG   § 88",
        "🇷🇺@FREE2CONFIG   § 89",
        "🇷🇺@FREE2CONFIG   § 90",
        "🇷🇺@FREE2CONFIG   § 91",
        "🇷🇺@FREE2CONFIG   § 92",
        "🇷🇺@FREE2CONFIG   § 93",
        "🇩🇰@FREE2CONFIG   § 94",
        "🇫🇷@FREE2CONFIG   § 95",
        "🇹🇷@FREE2CONFIG   § 96",
        "🇫🇷@FREE2CONFIG   § 97",
        "🇷🇺@FREE2CONFIG   § 98",
        "🇷🇺@FREE2CONFIG   § 99",
        "🇷🇺@FREE2CONFIG   § 100",
        "🇷🇺@FREE2CONFIG   § 101",
        "🇷🇺@FREE2CONFIG   § 102",
        "🇩🇪@FREE2CONFIG   § 103",
        "🇫🇮@FREE2CONFIG   § 104",
        "🇵🇱@FREE2CONFIG   § 105",
        "🇷🇺@FREE2CONFIG   § 106",
        "🇸🇪@FREE2CONFIG   § 107",
        "🇷🇺@FREE2CONFIG   § 108",
        "🇵🇱@FREE2CONFIG   § 109",
        "🇩🇪@FREE2CONFIG   § 110",
        "🇵🇱@FREE2CONFIG   § 111",
        "🇱🇹@FREE2CONFIG   § 112",
        "🇩🇪@FREE2CONFIG   § 113",
        "🇳🇱@FREE2CONFIG   § 114",
        "🇩🇪@FREE2CONFIG  § 115",
        "🇳🇱@FREE2CONFIG   § 116",
        "🇵🇱@FREE2CONFIG   § 117",
        "🇷🇺@FREE2CONFIG  § 118",
        "🇩🇪@FREE2CONFIG     § 119",
        "🇩🇪@FREE2CONFIG     § 120",
        "🇩🇪@FREE2CONFIG     § 121",
        "🇩🇪@FREE2CONFIG     § 122",
        "🇷🇺@FREE2CONFIG    § 123",
        "🇩🇪@FREE2CONFIG    § 124",
        "🇩🇪@FREE2CONFIG  § 125",
        "🇩🇪@FREE2CONFIG     § 126",
        "🇩🇪@FREE2CONFIG     § 127",
        "🇩🇪@FREE2CONFIG     § 128",
        "🇩🇪@FREE2CONFIG    § 129",
        "🇩🇪@FREE2CONFIG     § 130",
        "🇫🇷@FREE2CONFIG    § 131",
        "🇩🇪@FREE2CONFIG    § 132",
        "🇪🇪@FREE2CONFIG   § 133",
        "🇩🇪@FREE2CONFIG     § 134",
        "🇩🇪@FREE2CONFIG    § 135",
        "🇦🇪@FREE2CONFIG   § 136",
        "🇷🇺@FREE2CONFIG    § 137",
        "🇩🇪@FREE2CONFIG     § 138",
        "🇩🇪@FREE2CONFIG    § 139",
        "🇩🇪@FREE2CONFIG     § 140",
        "🇩🇪@FREE2CONFIG     § 141",
        "🇩🇪@FREE2CONFIG     § 142",
        "🇩🇪@FREE2CONFIG     § 143",
        "🇩🇪@FREE2CONFIG     § 144",
        "🇩🇪@FREE2CONFIG    § 145",
        "🇩🇪@FREE2CONFIG     § 146",
        "🇩🇪@FREE2CONFIG     § 147",
        "🇩🇰@FREE2CONFIG   § 148",
        "🇩🇪@FREE2CONFIG     § 149",
        "🇩🇪@FREE2CONFIG     § 150",
        "🇺🇸@FREE2CONFIG   § 151",
        "🇷🇺@FREE2CONFIG    § 152",
        "🇹🇷@FREE2CONFIG   § 153",
        "🇩🇪@FREE2CONFIG   § 154",
        "🇩🇪@FREE2CONFIG   § 155",
        "🇩🇪@FREE2CONFIG   § 156",
        "🇩🇪@FREE2CONFIG   § 157",
        "🇳🇱@FREE2CONFIG   § 158",
        "🇩🇪@FREE2CONFIG   § 159",
        "🇩🇪@FREE2CONFIG   § 160",
        "🇩🇪@FREE2CONFIG   § 161",
        "🇩🇪@FREE2CONFIG   § 162",
        "🇩🇪@FREE2CONFIG   § 163",
        "🇩🇪@FREE2CONFIG   § 164",
        "🇷🇺@FREE2CONFIG   § 165",
        "🇩🇪@FREE2CONFIG   § 166",
        "🇩🇪@FREE2CONFIG   § 167",
        "🇩🇪@FREE2CONFIG   § 168",
        "🇩🇪@FREE2CONFIG   § 169",
        "🇩🇪@FREE2CONFIG   § 170",
        "🇩🇪@FREE2CONFIG   § 171",
        "🇩🇪@FREE2CONFIG   § 172",
        "🇩🇪@FREE2CONFIG   § 173",
        "🇦🇲@FREE2CONFIG   § 174",
        "🇩🇪@FREE2CONFIG   § 175",
        "🇵🇱@FREE2CONFIG   § 176",
        "🇫🇮@FREE2CONFIG   § 177",
        "🇷🇺@FREE2CONFIG   § 178",
        "🇪🇸@FREE2CONFIG   § 179",
        "🇩🇪@FREE2CONFIG   § 180",
        "🇩🇪@FREE2CONFIG   § 181",
        "🇩🇪@FREE2CONFIG   § 182",
        "🇩🇪@FREE2CONFIG   § 183",
        "🇫🇷@FREE2CONFIG   § 184",
        "🇩🇪@FREE2CONFIG   § 185",
        "🇩🇪@FREE2CONFIG   § 186",
        "🇩🇪@FREE2CONFIG   § 187",
        "🇺🇸@FREE2CONFIG   § 188",
        "🇸🇪@FREE2CONFIG   § 189",
        "🇩🇪@FREE2CONFIG   § 190",
        "🇩🇪@FREE2CONFIG   § 191",
        "🇦🇪@FREE2CONFIG   § 192",
        "🇺🇸@FREE2CONFIG   § 193",
        "🇦🇲@FREE2CONFIG   § 194",
        "🇫🇷@FREE2CONFIG   § 195",
        "🇺🇸@FREE2CONFIG   § 196",
        "🇵🇱@FREE2CONFIG   § 197",
        "🇨🇦@FREE2CONFIG   § 198",
        "🇺🇸@FREE2CONFIG   § 199",
        "🇦🇺@FREE2CONFIG   § 200",
        "🇰🇿@FREE2CONFIG   § 201",
        "🇫🇷@FREE2CONFIG   § 202",
        "🇩🇪@FREE2CONFIG   § 203",
        "🇳🇱@FREE2CONFIG   § 204",
        "🇷🇺@FREE2CONFIG   § 205",
        "🇷🇺@FREE2CONFIG   § 206",
        "🇷🇺@FREE2CONFIG   § 207",
        "🇷🇺@FREE2CONFIG   § 208",
        "🇷🇺@FREE2CONFIG   § 209",
        "🇩🇰@FREE2CONFIG   § 210",
        "🇫🇷@FREE2CONFIG   § 211",
        "🇹🇷@FREE2CONFIG   § 212",
        "🇫🇷@FREE2CONFIG   § 213",
        "🇷🇺@FREE2CONFIG   § 214",
        "🇷🇺@FREE2CONFIG   § 215",
        "🇷🇺@FREE2CONFIG   § 216",
        "🇷🇺@FREE2CONFIG   § 217",
        "🇷🇺@FREE2CONFIG   § 218",
        "🇩🇪@FREE2CONFIG   § 219",
        "🇫🇮@FREE2CONFIG   § 220",
        "🇵🇱@FREE2CONFIG   § 221",
        "🇷🇺@FREE2CONFIG   § 222",
        "🇸🇪@FREE2CONFIG   § 223",
        "🇷🇺@FREE2CONFIG   § 224",
        "🇵🇱@FREE2CONFIG   § 225",
        "🇩🇪@FREE2CONFIG   § 226",
        "🇵🇱@FREE2CONFIG   § 227",
        "🇱🇹@FREE2CONFIG   § 228",
        "🇩🇪@FREE2CONFIG   § 229",
        "🇳🇱@FREE2CONFIG   § 230",
        "🇩🇪@FREE2CONFIG  § 231"
      ],
      "default": "auto",
      "interrupt_exist_connections": true
    },
    {
      "type": "urltest",
      "tag": "auto",
      "outbounds": [
        "1🇳🇱@FREE2CONFIG   § 0",
        "2🇵🇱@FREE2CONFIG   § 1",
        "3🇷🇺@FREE2CONFIG  § 2",
        "4🇩🇪@FREE2CONFIG     § 3",
        "5🇩🇪@FREE2CONFIG     § 4",
        "6🇩🇪@FREE2CONFIG     § 5",
        "7🇩🇪@FREE2CONFIG     § 6",
        "8🇷🇺@FREE2CONFIG    § 7",
        "9🇩🇪@FREE2CONFIG    § 8",
        "10🇩🇪@FREE2CONFIG  § 9",
        "11🇩🇪@FREE2CONFIG     § 10",
        "12🇩🇪@FREE2CONFIG     § 11",
        "13🇩🇪@FREE2CONFIG     § 12",
        "14🇩🇪@FREE2CONFIG    § 13",
        "15🇩🇪@FREE2CONFIG     § 14",
        "16🇫🇷@FREE2CONFIG    § 15",
        "17🇩🇪@FREE2CONFIG    § 16",
        "18🇪🇪@FREE2CONFIG   § 17",
        "19🇩🇪@FREE2CONFIG     § 18",
        "20🇩🇪@FREE2CONFIG    § 19",
        "21🇦🇪@FREE2CONFIG   § 20",
        "22🇷🇺@FREE2CONFIG    § 21",
        "23🇩🇪@FREE2CONFIG     § 22",
        "24🇩🇪@FREE2CONFIG    § 23",
        "25🇩🇪@FREE2CONFIG     § 24",
        "26🇩🇪@FREE2CONFIG     § 25",
        "27🇩🇪@FREE2CONFIG     § 26",
        "28🇩🇪@FREE2CONFIG     § 27",
        "29🇩🇪@FREE2CONFIG     § 28",
        "30🇩🇪@FREE2CONFIG    § 29",
        "🇩🇪@FREE2CONFIG     § 30",
        "🇩🇪@FREE2CONFIG     § 31",
        "🇩🇰@FREE2CONFIG   § 32",
        "🇩🇪@FREE2CONFIG     § 33",
        "🇩🇪@FREE2CONFIG     § 34",
        "🇺🇸@FREE2CONFIG   § 35",
        "🇷🇺@FREE2CONFIG    § 36",
        "🇹🇷@FREE2CONFIG   § 37",
        "🇩🇪@FREE2CONFIG   § 38",
        "🇩🇪@FREE2CONFIG   § 39",
        "🇩🇪@FREE2CONFIG   § 40",
        "🇩🇪@FREE2CONFIG   § 41",
        "🇳🇱@FREE2CONFIG   § 42",
        "🇩🇪@FREE2CONFIG   § 43",
        "🇩🇪@FREE2CONFIG   § 44",
        "🇩🇪@FREE2CONFIG   § 45",
        "🇩🇪@FREE2CONFIG   § 46",
        "🇩🇪@FREE2CONFIG   § 47",
        "🇩🇪@FREE2CONFIG   § 48",
        "🇷🇺@FREE2CONFIG   § 49",
        "🇩🇪@FREE2CONFIG   § 50",
        "🇩🇪@FREE2CONFIG   § 51",
        "🇩🇪@FREE2CONFIG   § 52",
        "🇩🇪@FREE2CONFIG   § 53",
        "🇩🇪@FREE2CONFIG   § 54",
        "🇩🇪@FREE2CONFIG   § 55",
        "🇩🇪@FREE2CONFIG   § 56",
        "🇩🇪@FREE2CONFIG   § 57",
        "🇦🇲@FREE2CONFIG   § 58",
        "🇩🇪@FREE2CONFIG   § 59",
        "🇵🇱@FREE2CONFIG   § 60",
        "🇫🇮@FREE2CONFIG   § 61",
        "🇷🇺@FREE2CONFIG   § 62",
        "🇪🇸@FREE2CONFIG   § 63",
        "🇩🇪@FREE2CONFIG   § 64",
        "🇩🇪@FREE2CONFIG   § 65",
        "🇩🇪@FREE2CONFIG   § 66",
        "🇩🇪@FREE2CONFIG   § 67",
        "🇫🇷@FREE2CONFIG   § 68",
        "🇩🇪@FREE2CONFIG   § 69",
        "🇩🇪@FREE2CONFIG   § 70",
        "🇩🇪@FREE2CONFIG   § 71",
        "🇺🇸@FREE2CONFIG   § 72",
        "🇸🇪@FREE2CONFIG   § 73",
        "🇩🇪@FREE2CONFIG   § 74",
        "🇩🇪@FREE2CONFIG   § 75",
        "🇦🇪@FREE2CONFIG   § 76",
        "🇺🇸@FREE2CONFIG   § 77",
        "🇦🇲@FREE2CONFIG   § 78",
        "🇫🇷@FREE2CONFIG   § 79",
        "🇺🇸@FREE2CONFIG   § 80",
        "🇵🇱@FREE2CONFIG   § 81",
        "🇨🇦@FREE2CONFIG   § 82",
        "🇺🇸@FREE2CONFIG   § 83",
        "🇦🇺@FREE2CONFIG   § 84",
        "🇰🇿@FREE2CONFIG   § 85",
        "🇫🇷@FREE2CONFIG   § 86",
        "🇩🇪@FREE2CONFIG   § 87",
        "🇳🇱@FREE2CONFIG   § 88",
        "🇷🇺@FREE2CONFIG   § 89",
        "🇷🇺@FREE2CONFIG   § 90",
        "🇷🇺@FREE2CONFIG   § 91",
        "🇷🇺@FREE2CONFIG   § 92",
        "🇷🇺@FREE2CONFIG   § 93",
        "🇩🇰@FREE2CONFIG   § 94",
        "🇫🇷@FREE2CONFIG   § 95",
        "🇹🇷@FREE2CONFIG   § 96",
        "🇫🇷@FREE2CONFIG   § 97",
        "🇷🇺@FREE2CONFIG   § 98",
        "🇷🇺@FREE2CONFIG   § 99",
        "🇷🇺@FREE2CONFIG   § 100",
        "🇷🇺@FREE2CONFIG   § 101",
        "🇷🇺@FREE2CONFIG   § 102",
        "🇩🇪@FREE2CONFIG   § 103",
        "🇫🇮@FREE2CONFIG   § 104",
        "🇵🇱@FREE2CONFIG   § 105",
        "🇷🇺@FREE2CONFIG   § 106",
        "🇸🇪@FREE2CONFIG   § 107",
        "🇷🇺@FREE2CONFIG   § 108",
        "🇵🇱@FREE2CONFIG   § 109",
        "🇩🇪@FREE2CONFIG   § 110",
        "🇵🇱@FREE2CONFIG   § 111",
        "🇱🇹@FREE2CONFIG   § 112",
        "🇩🇪@FREE2CONFIG   § 113",
        "🇳🇱@FREE2CONFIG   § 114",
        "🇩🇪@FREE2CONFIG  § 115",
        "🇳🇱@FREE2CONFIG   § 116",
        "🇵🇱@FREE2CONFIG   § 117",
        "🇷🇺@FREE2CONFIG  § 118",
        "🇩🇪@FREE2CONFIG     § 119",
        "🇩🇪@FREE2CONFIG     § 120",
        "🇩🇪@FREE2CONFIG     § 121",
        "🇩🇪@FREE2CONFIG     § 122",
        "🇷🇺@FREE2CONFIG    § 123",
        "🇩🇪@FREE2CONFIG    § 124",
        "🇩🇪@FREE2CONFIG  § 125",
        "🇩🇪@FREE2CONFIG     § 126",
        "🇩🇪@FREE2CONFIG     § 127",
        "🇩🇪@FREE2CONFIG     § 128",
        "🇩🇪@FREE2CONFIG    § 129",
        "🇩🇪@FREE2CONFIG     § 130",
        "🇫🇷@FREE2CONFIG    § 131",
        "🇩🇪@FREE2CONFIG    § 132",
        "🇪🇪@FREE2CONFIG   § 133",
        "🇩🇪@FREE2CONFIG     § 134",
        "🇩🇪@FREE2CONFIG    § 135",
        "🇦🇪@FREE2CONFIG   § 136",
        "🇷🇺@FREE2CONFIG    § 137",
        "🇩🇪@FREE2CONFIG     § 138",
        "🇩🇪@FREE2CONFIG    § 139",
        "🇩🇪@FREE2CONFIG     § 140",
        "🇩🇪@FREE2CONFIG     § 141",
        "🇩🇪@FREE2CONFIG     § 142",
        "🇩🇪@FREE2CONFIG     § 143",
        "🇩🇪@FREE2CONFIG     § 144",
        "🇩🇪@FREE2CONFIG    § 145",
        "🇩🇪@FREE2CONFIG     § 146",
        "🇩🇪@FREE2CONFIG     § 147",
        "🇩🇰@FREE2CONFIG   § 148",
        "🇩🇪@FREE2CONFIG     § 149",
        "🇩🇪@FREE2CONFIG     § 150",
        "🇺🇸@FREE2CONFIG   § 151",
        "🇷🇺@FREE2CONFIG    § 152",
        "🇹🇷@FREE2CONFIG   § 153",
        "🇩🇪@FREE2CONFIG   § 154",
        "🇩🇪@FREE2CONFIG   § 155",
        "🇩🇪@FREE2CONFIG   § 156",
        "🇩🇪@FREE2CONFIG   § 157",
        "🇳🇱@FREE2CONFIG   § 158",
        "🇩🇪@FREE2CONFIG   § 159",
        "🇩🇪@FREE2CONFIG   § 160",
        "🇩🇪@FREE2CONFIG   § 161",
        "🇩🇪@FREE2CONFIG   § 162",
        "🇩🇪@FREE2CONFIG   § 163",
        "🇩🇪@FREE2CONFIG   § 164",
        "🇷🇺@FREE2CONFIG   § 165",
        "🇩🇪@FREE2CONFIG   § 166",
        "🇩🇪@FREE2CONFIG   § 167",
        "🇩🇪@FREE2CONFIG   § 168",
        "🇩🇪@FREE2CONFIG   § 169",
        "🇩🇪@FREE2CONFIG   § 170",
        "🇩🇪@FREE2CONFIG   § 171",
        "🇩🇪@FREE2CONFIG   § 172",
        "🇩🇪@FREE2CONFIG   § 173",
        "🇦🇲@FREE2CONFIG   § 174",
        "🇩🇪@FREE2CONFIG   § 175",
        "🇵🇱@FREE2CONFIG   § 176",
        "🇫🇮@FREE2CONFIG   § 177",
        "🇷🇺@FREE2CONFIG   § 178",
        "🇪🇸@FREE2CONFIG   § 179",
        "🇩🇪@FREE2CONFIG   § 180",
        "🇩🇪@FREE2CONFIG   § 181",
        "🇩🇪@FREE2CONFIG   § 182",
        "🇩🇪@FREE2CONFIG   § 183",
        "🇫🇷@FREE2CONFIG   § 184",
        "🇩🇪@FREE2CONFIG   § 185",
        "🇩🇪@FREE2CONFIG   § 186",
        "🇩🇪@FREE2CONFIG   § 187",
        "🇺🇸@FREE2CONFIG   § 188",
        "🇸🇪@FREE2CONFIG   § 189",
        "🇩🇪@FREE2CONFIG   § 190",
        "🇩🇪@FREE2CONFIG   § 191",
        "🇦🇪@FREE2CONFIG   § 192",
        "🇺🇸@FREE2CONFIG   § 193",
        "🇦🇲@FREE2CONFIG   § 194",
        "🇫🇷@FREE2CONFIG   § 195",
        "🇺🇸@FREE2CONFIG   § 196",
        "🇵🇱@FREE2CONFIG   § 197",
        "🇨🇦@FREE2CONFIG   § 198",
        "🇺🇸@FREE2CONFIG   § 199",
        "🇦🇺@FREE2CONFIG   § 200",
        "🇰🇿@FREE2CONFIG   § 201",
        "🇫🇷@FREE2CONFIG   § 202",
        "🇩🇪@FREE2CONFIG   § 203",
        "🇳🇱@FREE2CONFIG   § 204",
        "🇷🇺@FREE2CONFIG   § 205",
        "🇷🇺@FREE2CONFIG   § 206",
        "🇷🇺@FREE2CONFIG   § 207",
        "🇷🇺@FREE2CONFIG   § 208",
        "🇷🇺@FREE2CONFIG   § 209",
        "🇩🇰@FREE2CONFIG   § 210",
        "🇫🇷@FREE2CONFIG   § 211",
        "🇹🇷@FREE2CONFIG   § 212",
        "🇫🇷@FREE2CONFIG   § 213",
        "🇷🇺@FREE2CONFIG   § 214",
        "🇷🇺@FREE2CONFIG   § 215",
        "🇷🇺@FREE2CONFIG   § 216",
        "🇷🇺@FREE2CONFIG   § 217",
        "🇷🇺@FREE2CONFIG   § 218",
        "🇩🇪@FREE2CONFIG   § 219",
        "🇫🇮@FREE2CONFIG   § 220",
        "🇵🇱@FREE2CONFIG   § 221",
        "🇷🇺@FREE2CONFIG   § 222",
        "🇸🇪@FREE2CONFIG   § 223",
        "🇷🇺@FREE2CONFIG   § 224",
        "🇵🇱@FREE2CONFIG   § 225",
        "🇩🇪@FREE2CONFIG   § 226",
        "🇵🇱@FREE2CONFIG   § 227",
        "🇱🇹@FREE2CONFIG   § 228",
        "🇩🇪@FREE2CONFIG   § 229",
        "🇳🇱@FREE2CONFIG   § 230",
        "🇩🇪@FREE2CONFIG  § 231"
      ],
      "url": "http://cp.cloudflare.com",
      "interval": "10m0s",
      "tolerance": 1,
      "idle_timeout": "30m0s",
      "interrupt_exist_connections": true
    },
    {
      "type": "vless",
      "tag": "1🇳🇱@FREE2CONFIG   § 0",
      "server": "45.8.144.27",
      "server_port": 443,
      "uuid": "3b13042c-f6af-4a21-9872-00c09ff7e5b9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "nr9.strelkavpn.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "P2vHFiKpYCiEDB3HeRfKMUuzGk_ZXW2wXmcna6BRJW4",
          "short_id": "76bd7b341f61ab"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "2🇵🇱@FREE2CONFIG   § 1",
      "server": "51.250.109.47",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "3🇷🇺@FREE2CONFIG  § 2",
      "server": "217.16.24.170",
      "server_port": 443,
      "uuid": "a91e64f0-9295-499d-bf4a-661ad99d4938",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "ios"
        },
        "reality": {
          "enabled": true,
          "public_key": "8OsJx6xuHcpL_5e1w0U4bMBa-icevDgvvzNwPwZbORQ",
          "short_id": "5540e44a53c3d01c"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "4🇩🇪@FREE2CONFIG     § 3",
      "server": "152.53.133.72",
      "server_port": 443,
      "uuid": "cbabe86a-40a5-46af-898f-d6eaac66e141",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "7a-5DF4-Xk8h1Ex0zG-0CcSBgdhAnLrofVQ0rRdiSD8",
          "short_id": "0990c9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "5🇩🇪@FREE2CONFIG     § 4",
      "server": "152.53.86.94",
      "server_port": 443,
      "uuid": "23914cf2-2d38-4402-8862-4b02c60b84d9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mtalk.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "dqzabPbB3PzzynPZdUe6AtyKH0FIdi0eIyQBvn9azE0",
          "short_id": "23"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "6🇩🇪@FREE2CONFIG     § 5",
      "server": "152.53.142.51",
      "server_port": 443,
      "uuid": "e371c3c9-4ebd-4a17-9915-ee1331c02e74",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients3.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "q6ayd3-xiVbHZqOFRWTqZ8ftHSPhzcWKno4nfO3uOjI",
          "short_id": "5df42470e9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "7🇩🇪@FREE2CONFIG     § 6",
      "server": "152.53.141.19",
      "server_port": 443,
      "uuid": "cd1091f1-8deb-4080-bf0d-19cc1ee0da02",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mesu.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "uh_HksISuPiZ-j3DG6m8MNhPBEEu__J-ILHQVv3pnRE",
          "short_id": "f08d17de7d6380"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "8🇷🇺@FREE2CONFIG    § 7",
      "server": "80.249.131.236",
      "server_port": 444,
      "uuid": "48b2795f-de72-44ea-ae96-f635e5952d45",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "yt.fasssst.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "14S-a9NL1PacapqVE4ojKZeEM5995jFyfwS0xc9UtRk",
          "short_id": "7d20a73ab88583f8"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "9🇩🇪@FREE2CONFIG    § 8",
      "server": "152.53.144.195",
      "server_port": 443,
      "uuid": "6a0ddf8c-79bb-4328-b35b-55f62ae98dbc",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Ru5SHhsknPugwt4gwVO8ZIm4YkiHA-OQoeS8ddPClDk",
          "short_id": "9d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "10🇩🇪@FREE2CONFIG  § 9",
      "server": "152.53.145.111",
      "server_port": 443,
      "uuid": "5aad18e2-f53b-4927-a1ff-cda06c5d5b02",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "init.itunes.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "nc1sfrAmREkpj15hupqKM-l0t1_qlxvhUxgp2KvnpmE",
          "short_id": "d0"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "11🇩🇪@FREE2CONFIG     § 10",
      "server": "152.53.133.115",
      "server_port": 443,
      "uuid": "c1b1524f-549f-4a06-9bd1-86ec04b0a032",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "developer.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "z1mANGkdN1YaF6mpCULPlG4w2JfYnkxL3y0W4Frrqm4",
          "short_id": "88"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "12🇩🇪@FREE2CONFIG     § 11",
      "server": "152.53.187.28",
      "server_port": 443,
      "uuid": "e3af49ba-6a41-4fa1-8f21-f40d1f154c68",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "configuration.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "DJ1l1bgvwpj-SoHuC6eLVfzd3rp1zQmCV76fdVazMgc",
          "short_id": "173c58"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "13🇩🇪@FREE2CONFIG     § 12",
      "server": "152.53.142.129",
      "server_port": 443,
      "uuid": "5c00f0cb-905e-47ce-9b6b-2d4d137a1f9e",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "workers.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "BnwepsrMVlmIpiUMIOoAlBXJ5iZh5GMpgfjHuhwhklM",
          "short_id": "48"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "14🇩🇪@FREE2CONFIG    § 13",
      "server": "152.53.135.122",
      "server_port": 443,
      "uuid": "c9fc7cb8-6dde-46e9-a682-8022e4b6900b",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "d1.awsstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "c3ZHON336aVBpNfV34OnFA5B-ocWtNa-kc29ql-flD0",
          "short_id": "63"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "15🇩🇪@FREE2CONFIG     § 14",
      "server": "51.250.24.245",
      "server_port": 4249,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "16🇫🇷@FREE2CONFIG    § 15",
      "server": "62.60.157.37",
      "server_port": 443,
      "uuid": "d48ba610-6ef1-475b-9d33-be2a0db96f87",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "st.ozone.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "jVZNjr5dXzki9VxDHWg_zsiUjSrplC0mnZrG8tuP_2c",
          "short_id": "149adb1c3cb9ed11"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "17🇩🇪@FREE2CONFIG    § 16",
      "server": "152.53.133.244",
      "server_port": 443,
      "uuid": "615c6f31-eb83-4c09-8510-f1a0faadc8e8",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients2.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ytiNy-7llRPrWSHVUQL8ii6PEX29aTG-hS_NkCYaTBQ",
          "short_id": "1b9617"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "18🇪🇪@FREE2CONFIG   § 17",
      "server": "45.92.176.55",
      "server_port": 1243,
      "uuid": "d29bde62-daa4-4804-9c69-6e23a4150006",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "rontgen.fasssst.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "jcJeCbLo5JtfveFIQLV6WNm1148XzxDc0Rzy336hXy0",
          "short_id": "ff3cef7cdcf9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "19🇩🇪@FREE2CONFIG     § 18",
      "server": "152.53.186.174",
      "server_port": 443,
      "uuid": "b58d778d-f393-4280-940f-61230dbdd491",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "frSr5idN1FqLyEdsujtTf-BnCDx35Eji65qIsXuqNCo",
          "short_id": "3938"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "20🇩🇪@FREE2CONFIG    § 19",
      "server": "152.53.143.63",
      "server_port": 443,
      "uuid": "485fafeb-f806-40ad-996c-94e01ee84daf",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mtalk.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "lhwCcXyMGY8GEVV0wDTRsSApcOj-CM1fP8DRY0buRHg",
          "short_id": "eea9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "21🇦🇪@FREE2CONFIG   § 20",
      "server": "217.195.200.224",
      "server_port": 443,
      "uuid": "1437fec7-064b-4f8f-98f4-8c9aad3738b0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "HZM7SXNCsT5M_zWuBURZfplLY-L5Gqww5qRPJZAP8C4",
          "short_id": "754dc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "22🇷🇺@FREE2CONFIG    § 21",
      "server": "51.250.28.39",
      "server_port": 4248,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "23🇩🇪@FREE2CONFIG     § 22",
      "server": "152.53.133.132",
      "server_port": 443,
      "uuid": "4775848f-2595-4777-8524-b60b16c3cd79",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api.snapkit.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "bMd4ndQTVjCtOYI9nKspNZx_XZXmPgbrcfw20GZQckA",
          "short_id": "332d4a4e"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "24🇩🇪@FREE2CONFIG    § 23",
      "server": "93.114.56.67",
      "server_port": 443,
      "uuid": "22eba6de-256f-4d92-8c79-9b66204d40b0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "init.itunes.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SOloMl69oKpNpX3b-Ec5n3chWjmprNQ_UnFvAzI-JxE",
          "short_id": "056a"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "25🇩🇪@FREE2CONFIG     § 24",
      "server": "5.181.21.72",
      "server_port": 443,
      "uuid": "e4b8df56-b680-4a34-ab47-5bf5738ed718",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "v9CxKfIPtkKH1cTGKEer-1i-3JL31vZPpPl2Ujnbjh8",
          "short_id": "85225c27630d023f"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "26🇩🇪@FREE2CONFIG     § 25",
      "server": "185.140.14.166",
      "server_port": 8443,
      "uuid": "9e460075-dcb2-504a-b3d9-aab5c3095442",
      "tls": {
        "enabled": true,
        "server_name": "www.microsoft.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "qdcM4h1uoHcpGw_QnU99NnUXgcjDFyoE-E1_Ili3Xgo",
          "short_id": "3471fa2412678660"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "27🇩🇪@FREE2CONFIG     § 26",
      "server": "152.53.133.12",
      "server_port": 443,
      "uuid": "f81d5b9b-c5b7-46cb-8710-0cf41ab33570",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "WeNlf_hPscBLSwtg1PgOmurK1f7VyQSNPmOYeG0wIQw",
          "short_id": "6590cb"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "28🇩🇪@FREE2CONFIG     § 27",
      "server": "188.68.36.138",
      "server_port": 443,
      "uuid": "fc200ee7-2643-4e20-9231-d8b87ac03935",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients3.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "X_03fRoDo9vm437UVnLT5m_ZbGa2A6p0qhBKSfZYvGk",
          "short_id": "9dce"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "29🇩🇪@FREE2CONFIG     § 28",
      "server": "152.53.142.188",
      "server_port": 443,
      "uuid": "8c8e79ba-6bf6-42dc-9f16-04947ebf5325",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "xp.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "MvVhNhJedr9JB7tNjJ8d0z7z6FfHwXqcPGkZ15A-QGY",
          "short_id": "9c7a"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "30🇩🇪@FREE2CONFIG    § 29",
      "server": "152.53.87.20",
      "server_port": 443,
      "uuid": "6526d72e-95b3-460d-a2e6-1b0b66d18b60",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "developer.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "XjlDjEKKUfTB4uEdMjRYo35n8J_Rm1FQmvw87Mf4CTU",
          "short_id": "42fbfd"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 30",
      "server": "152.53.134.168",
      "server_port": 443,
      "uuid": "f6f74d98-8e6b-4f4a-8f88-79ae32f28edb",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ks76ikSkP9d-_uHJ5Ms_aEI6wjkXWvw7GEUxNBSp5T0",
          "short_id": "12d75b"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 31",
      "server": "152.53.144.46",
      "server_port": 443,
      "uuid": "9ddd1f39-e7e4-4d52-b202-7d7b2f13215a",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients2.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "4yvKWFMcxHUzMJCMupKIRvqw2gsCRsD_bfirrZ0LmAI",
          "short_id": "83e035aa57"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇰@FREE2CONFIG   § 32",
      "server": "45.92.176.55",
      "server_port": 2243,
      "uuid": "d7e2c1ec-b2ba-4a4c-a73a-c08f5bd7923b",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "rontgen.fasssst.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "_ee-ouMazAzx7Q4_cYhWbu6pw53-8VVpt7tuBuCXziU",
          "short_id": "e3cbc70477"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 33",
      "server": "89.58.55.196",
      "server_port": 443,
      "uuid": "1c83fafe-8107-46ed-a94c-1252de4ceba6",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "xp.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Y7WW7er4kSFYTxwTw8Lv7Iu-cPH0_Vt3kimM7vD9GHM",
          "short_id": "640054"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 34",
      "server": "37.120.171.194",
      "server_port": 443,
      "uuid": "4974a3b2-ba08-47e0-806b-85fb45d038a0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mesu.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "WXPq4NT1gqVRO7IUJGU3tv0NDe8gxEVN2WGa1dwjiCk",
          "short_id": "1b89"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇺🇸@FREE2CONFIG   § 35",
      "server": "216.133.149.139",
      "server_port": 23581,
      "uuid": "b5471668-94dc-4ea5-ae97-3bb9dabcd2a9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "EOYTqph-go2SazIPcSDl5pJGNyOnrR0mWaL8Tc_paEM"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG    § 36",
      "server": "185.234.59.74",
      "server_port": 8443,
      "uuid": "4a3ece53-6000-4ba3-a9fa-fd0d7ba61cf3",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "stats.vk-portal.net",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "mLmBhbVFfNuo2eUgBh6r9-5Koz9mUCn3aSzlR6IejUg",
          "short_id": "175d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇹🇷@FREE2CONFIG   § 37",
      "server": "213.156.152.223",
      "server_port": 443,
      "uuid": "cb7188cf-2c3a-43a5-af90-d893922e4917",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "eS0NqJCAo6Jn4PuU3nU4A5D7RyNbn3WyhipXViddnzI",
          "short_id": "5457"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 38",
      "server": "152.53.142.189",
      "server_port": 443,
      "uuid": "e23b2103-c1c2-4035-858c-d5c7080e541f",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "configuration.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Cj72nKei-IJbaEG4olVgyKMmNUQn3NqpyHtHxGyqn2k",
          "short_id": "7ce392"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 39",
      "server": "152.53.141.19",
      "server_port": 443,
      "uuid": "cd1091f1-8deb-4080-bf0d-19cc1ee0da02",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mesu.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "uh_HksISuPiZ-j3DG6m8MNhPBEEu__J-ILHQVv3pnRE",
          "short_id": "f08d17de7d6380"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 40",
      "server": "188.68.36.138",
      "server_port": 443,
      "uuid": "fc200ee7-2643-4e20-9231-d8b87ac03935",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients3.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "X_03fRoDo9vm437UVnLT5m_ZbGa2A6p0qhBKSfZYvGk",
          "short_id": "9dce"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 41",
      "server": "128.140.94.109",
      "server_port": 443,
      "uuid": "80683c47-3706-406b-83b8-1d3695fb1bfb",
      "tls": {
        "enabled": true,
        "server_name": "www.ea.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "uJqfENqH6w2k1sM4qJo2m_nJMmOo91DCNmsxUhgjpQc",
          "short_id": "7b4a5e44"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇳🇱@FREE2CONFIG   § 42",
      "server": "185.82.73.212",
      "server_port": 8443,
      "uuid": "4a3ece53-6000-4ba3-a9fa-fd0d7ba61cf3",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "stats.vk-portal.net",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "mLmBhbVFfNuo2eUgBh6r9-5Koz9mUCn3aSzlR6IejUg",
          "short_id": "d3b13f31"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 43",
      "server": "152.53.133.12",
      "server_port": 443,
      "uuid": "f81d5b9b-c5b7-46cb-8710-0cf41ab33570",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "WeNlf_hPscBLSwtg1PgOmurK1f7VyQSNPmOYeG0wIQw",
          "short_id": "6590cb"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 44",
      "server": "152.53.133.72",
      "server_port": 443,
      "uuid": "cbabe86a-40a5-46af-898f-d6eaac66e141",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "7a-5DF4-Xk8h1Ex0zG-0CcSBgdhAnLrofVQ0rRdiSD8",
          "short_id": "0990c9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 45",
      "server": "152.53.147.46",
      "server_port": 443,
      "uuid": "9fe667f5-ffea-4272-a0b6-3abd73941c52",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "MrCEmqtF6MdAfyvwu7VWipCvi_8P0RjI8TF571XT6l0",
          "short_id": "209f"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 46",
      "server": "152.53.144.46",
      "server_port": 443,
      "uuid": "9ddd1f39-e7e4-4d52-b202-7d7b2f13215a",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients2.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "4yvKWFMcxHUzMJCMupKIRvqw2gsCRsD_bfirrZ0LmAI",
          "short_id": "83e035aa57"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 47",
      "server": "152.53.187.28",
      "server_port": 443,
      "uuid": "e3af49ba-6a41-4fa1-8f21-f40d1f154c68",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "configuration.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "DJ1l1bgvwpj-SoHuC6eLVfzd3rp1zQmCV76fdVazMgc",
          "short_id": "173c58"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 48",
      "server": "152.53.134.168",
      "server_port": 443,
      "uuid": "f6f74d98-8e6b-4f4a-8f88-79ae32f28edb",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ks76ikSkP9d-_uHJ5Ms_aEI6wjkXWvw7GEUxNBSp5T0",
          "short_id": "12d75b"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 49",
      "server": "217.16.24.170",
      "server_port": 443,
      "uuid": "a91e64f0-9295-499d-bf4a-661ad99d4938",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "8OsJx6xuHcpL_5e1w0U4bMBa-icevDgvvzNwPwZbORQ",
          "short_id": "5540e44a53c3d01c"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 50",
      "server": "152.53.142.51",
      "server_port": 443,
      "uuid": "e371c3c9-4ebd-4a17-9915-ee1331c02e74",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients3.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "q6ayd3-xiVbHZqOFRWTqZ8ftHSPhzcWKno4nfO3uOjI",
          "short_id": "5df42470e9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 51",
      "server": "152.53.133.244",
      "server_port": 443,
      "uuid": "615c6f31-eb83-4c09-8510-f1a0faadc8e8",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients2.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ytiNy-7llRPrWSHVUQL8ii6PEX29aTG-hS_NkCYaTBQ",
          "short_id": "1b9617"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 52",
      "server": "152.53.146.1",
      "server_port": 443,
      "uuid": "1808de5c-08db-4d3f-8688-34ed85a0322d",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "workers.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "LyhCTXS-yRgKZ052TlzwAs-hbj4n1qvJE2OLnbnCGDo",
          "short_id": "dab7"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 53",
      "server": "152.53.133.115",
      "server_port": 443,
      "uuid": "c1b1524f-549f-4a06-9bd1-86ec04b0a032",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "developer.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "z1mANGkdN1YaF6mpCULPlG4w2JfYnkxL3y0W4Frrqm4",
          "short_id": "88"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 54",
      "server": "37.120.171.194",
      "server_port": 443,
      "uuid": "4974a3b2-ba08-47e0-806b-85fb45d038a0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mesu.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "WXPq4NT1gqVRO7IUJGU3tv0NDe8gxEVN2WGa1dwjiCk",
          "short_id": "1b89"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 55",
      "server": "152.53.87.20",
      "server_port": 443,
      "uuid": "6526d72e-95b3-460d-a2e6-1b0b66d18b60",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "developer.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "XjlDjEKKUfTB4uEdMjRYo35n8J_Rm1FQmvw87Mf4CTU",
          "short_id": "42fbfd"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 56",
      "server": "152.53.135.122",
      "server_port": 443,
      "uuid": "c9fc7cb8-6dde-46e9-a682-8022e4b6900b",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "d1.awsstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "c3ZHON336aVBpNfV34OnFA5B-ocWtNa-kc29ql-flD0",
          "short_id": "63"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 57",
      "server": "152.53.186.174",
      "server_port": 443,
      "uuid": "b58d778d-f393-4280-940f-61230dbdd491",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "frSr5idN1FqLyEdsujtTf-BnCDx35Eji65qIsXuqNCo",
          "short_id": "3938"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇦🇲@FREE2CONFIG   § 58",
      "server": "91.132.132.109",
      "server_port": 8443,
      "uuid": "c44d64d3-bc91-43ba-9d59-3a0906e7a2bd",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "wWi-AH24-O27OYXsaT390rLPZY9hqBRYuvBGIZ9vzkk"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 59",
      "server": "152.53.144.195",
      "server_port": 443,
      "uuid": "6a0ddf8c-79bb-4328-b35b-55f62ae98dbc",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Ru5SHhsknPugwt4gwVO8ZIm4YkiHA-OQoeS8ddPClDk",
          "short_id": "9d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇵🇱@FREE2CONFIG   § 60",
      "server": "2.56.125.166",
      "server_port": 443,
      "uuid": "ee9b2135-b149-437e-995a-bfadfad342f5",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "hls-svod.itunes.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "llaiqC-oIhL_bjc236FPq26LSn7IVhIa4cIC6OVytws",
          "short_id": "31"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇮@FREE2CONFIG   § 61",
      "server": "109.61.17.127",
      "server_port": 443,
      "uuid": "0771a171-7eea-4272-a6b1-3e29478e4473",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients4.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "C5xoRWKopqNXP5xmZsJQdejPRIoZpzWRgrtlNticyQA",
          "short_id": "78e514cf"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 62",
      "server": "185.234.59.74",
      "server_port": 8443,
      "uuid": "2ca07504-c06a-41a4-b26b-99807a7d24cf",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "stats.vk-portal.net",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "mLmBhbVFfNuo2eUgBh6r9-5Koz9mUCn3aSzlR6IejUg",
          "short_id": "e499f276e7bd6420"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇪🇸@FREE2CONFIG   § 63",
      "server": "5.22.216.192",
      "server_port": 443,
      "uuid": "7392bb3b-7b2c-4eba-b399-b5e9534c12b0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "HO6w1kV0-nVwjEbAsPFfzRc_plvZjIXB9Ut11owI3Ec",
          "short_id": "066b"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 64",
      "server": "152.53.87.208",
      "server_port": 443,
      "uuid": "83787f92-2c0b-4217-9aea-bee4448331ec",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "xoeuO8vB3K-bPdSqcjlGV7MNJqJZ1KlJYGQydLB9vnU",
          "short_id": "c560cdc5"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 65",
      "server": "152.53.145.111",
      "server_port": 443,
      "uuid": "5aad18e2-f53b-4927-a1ff-cda06c5d5b02",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "init.itunes.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "nc1sfrAmREkpj15hupqKM-l0t1_qlxvhUxgp2KvnpmE",
          "short_id": "d0"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 66",
      "server": "152.53.141.213",
      "server_port": 443,
      "uuid": "13f395b3-5d40-43f9-bd94-55feaae1fa70",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "d1.awsstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "KQ2kgnnjTCTNaHRBYu7-qmT9GnWefrPm3L67JrOw9wA",
          "short_id": "1d62"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 67",
      "server": "152.53.133.132",
      "server_port": 443,
      "uuid": "4775848f-2595-4777-8524-b60b16c3cd79",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api.snapkit.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "bMd4ndQTVjCtOYI9nKspNZx_XZXmPgbrcfw20GZQckA",
          "short_id": "332d4a4e"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇷@FREE2CONFIG   § 68",
      "server": "45.10.59.133",
      "server_port": 443,
      "uuid": "417a3a22-8019-4991-82e1-8e4e27e95022",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "9Bx-1do5J20bTshcos2BDFpgRfRHIig3MyRAJET11AY",
          "short_id": "07e75c2cb26c35"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 69",
      "server": "152.53.142.188",
      "server_port": 443,
      "uuid": "8c8e79ba-6bf6-42dc-9f16-04947ebf5325",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "xp.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "MvVhNhJedr9JB7tNjJ8d0z7z6FfHwXqcPGkZ15A-QGY",
          "short_id": "9c7a"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 70",
      "server": "152.53.142.129",
      "server_port": 443,
      "uuid": "5c00f0cb-905e-47ce-9b6b-2d4d137a1f9e",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "workers.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "BnwepsrMVlmIpiUMIOoAlBXJ5iZh5GMpgfjHuhwhklM",
          "short_id": "48"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 71",
      "server": "51.250.25.11",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇺🇸@FREE2CONFIG   § 72",
      "server": "216.133.149.139",
      "server_port": 23581,
      "uuid": "b5471668-94dc-4ea5-ae97-3bb9dabcd2a9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "EOYTqph-go2SazIPcSDl5pJGNyOnrR0mWaL8Tc_paEM"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇸🇪@FREE2CONFIG   § 73",
      "server": "95.111.208.215",
      "server_port": 443,
      "uuid": "902927e2-481e-4fc3-93e9-463b5cbf1663",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api.snapkit.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "BM8HKruNU-7Lg5Qb54Pv-qjdKwItDn_kY1S9vBPruAc",
          "short_id": "72d6"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 74",
      "server": "89.58.55.196",
      "server_port": 443,
      "uuid": "1c83fafe-8107-46ed-a94c-1252de4ceba6",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "xp.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Y7WW7er4kSFYTxwTw8Lv7Iu-cPH0_Vt3kimM7vD9GHM",
          "short_id": "640054"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 75",
      "server": "152.53.143.63",
      "server_port": 443,
      "uuid": "485fafeb-f806-40ad-996c-94e01ee84daf",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mtalk.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "lhwCcXyMGY8GEVV0wDTRsSApcOj-CM1fP8DRY0buRHg",
          "short_id": "eea9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇦🇪@FREE2CONFIG   § 76",
      "server": "217.195.200.224",
      "server_port": 443,
      "uuid": "1437fec7-064b-4f8f-98f4-8c9aad3738b0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "HZM7SXNCsT5M_zWuBURZfplLY-L5Gqww5qRPJZAP8C4",
          "short_id": "754dc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇺🇸@FREE2CONFIG   § 77",
      "server": "107.173.148.58",
      "server_port": 443,
      "uuid": "b98d4c6e-6770-4a31-8256-a4750cdea0e7",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.amazon.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "0i_xAxYgSNx5NMpK2lOaWGS-CvAiD_LneYPO0MF0owo",
          "short_id": "1a"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇦🇲@FREE2CONFIG   § 78",
      "server": "77.91.68.70",
      "server_port": 55983,
      "uuid": "f667a096-5231-4cfb-8759-92bb32473139",
      "tls": {
        "enabled": true,
        "server_name": "yahoo.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "nWQ7b9l9X6N3PrXLgIzOvMM8iSYrqjVHEb9ikWxqYSg",
          "short_id": "0e"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇷@FREE2CONFIG   § 79",
      "server": "216.106.189.107",
      "server_port": 8443,
      "uuid": "4468ae8a-7741-42dd-be69-d75cd94c9b0e",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.microsoft.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "iHDnFIEsw6lD514kP0JNtP1h7zlQ6AEZn6nKICyOYlY",
          "short_id": "5eac66585cbd595c"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇺🇸@FREE2CONFIG   § 80",
      "server": "47.253.226.114",
      "server_port": 443,
      "uuid": "055a1ce8-2a16-4a0d-a2c2-22826c9b2413",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Svl81isn16RPAFnjtmYw7A6TPnsEPLHuYYaJht65Rzc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇵🇱@FREE2CONFIG   § 81",
      "server": "2.56.125.209",
      "server_port": 49868,
      "uuid": "be015dd2-30b4-4fcf-a9ee-080c13ac13fb",
      "tls": {
        "enabled": true,
        "server_name": "yahoo.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "joEKL4Itljxodt1SOe1itSMrAH9bk_udpPtXgIjdu10",
          "short_id": "6d638e"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇨🇦@FREE2CONFIG   § 82",
      "server": "208.69.79.250",
      "server_port": 8443,
      "uuid": "89bb09d7-5a4b-4f6a-b73f-0ea67cb6f3a6",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.microsoft.com",
        "utls": {
          "enabled": true,
          "fingerprint": "safari"
        },
        "reality": {
          "enabled": true,
          "public_key": "ZnHyH5mL_cimo8JOfiosIRp-_IqvRVCzinNClSmsbVk",
          "short_id": "9b4be2de2162366d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇺🇸@FREE2CONFIG   § 83",
      "server": "47.251.25.74",
      "server_port": 443,
      "uuid": "18805ff3-b420-45de-af18-93be14024ae8",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.amazon.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "H56cOJhw0xw76lDEpt7IuJJmVGemK6_CK34KtHwDMX8"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇦🇺@FREE2CONFIG   § 84",
      "server": "192.9.162.122",
      "server_port": 1443,
      "uuid": "7a169e43-ff85-4572-9843-ba7207d07319",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "swdist.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ZIBYUH_qQSeI1T6xImXG6MEZXP2yZW3NqGa8W69Cfyk",
          "short_id": "dde50f55d81116"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇰🇿@FREE2CONFIG   § 85",
      "server": "178.236.16.98",
      "server_port": 35728,
      "uuid": "a00d89f6-ab7e-4e30-a5e5-54c701d62c93",
      "tls": {
        "enabled": true,
        "server_name": "yahoo.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "vhUFNoFcvtZAVMo8y5K5eU2V43m5q6yjmWIhp5RkFng",
          "short_id": "69a2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇷@FREE2CONFIG   § 86",
      "server": "62.60.157.37",
      "server_port": 443,
      "uuid": "d48ba610-6ef1-475b-9d33-be2a0db96f87",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "st.ozone.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "jVZNjr5dXzki9VxDHWg_zsiUjSrplC0mnZrG8tuP_2c",
          "short_id": "149adb1c3cb9ed11"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 87",
      "server": "152.53.86.94",
      "server_port": 443,
      "uuid": "23914cf2-2d38-4402-8862-4b02c60b84d9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mtalk.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "dqzabPbB3PzzynPZdUe6AtyKH0FIdi0eIyQBvn9azE0",
          "short_id": "23"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇳🇱@FREE2CONFIG   § 88",
      "server": "185.82.73.212",
      "server_port": 8443,
      "uuid": "4a3ece53-6000-4ba3-a9fa-fd0d7ba61cf3",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "stats.vk-portal.net",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "mLmBhbVFfNuo2eUgBh6r9-5Koz9mUCn3aSzlR6IejUg",
          "short_id": "175d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 89",
      "server": "95.163.215.93",
      "server_port": 8443,
      "uuid": "b89d0b93-0ce0-424d-b9ab-92102acd5b84",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ccfP5xSIpFgQVJIXA4Yj7fZ9Agjc9JVHvESTv3hnZjQ",
          "short_id": "62094d6a0b771c25"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 90",
      "server": "51.250.28.39",
      "server_port": 4248,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 91",
      "server": "185.234.59.74",
      "server_port": 8443,
      "uuid": "4a3ece53-6000-4ba3-a9fa-fd0d7ba61cf3",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "stats.vk-portal.net",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "mLmBhbVFfNuo2eUgBh6r9-5Koz9mUCn3aSzlR6IejUg",
          "short_id": "175d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 92",
      "server": "62.113.42.65",
      "server_port": 27121,
      "uuid": "cbf1ec03-2cff-4b1f-9eb5-5929c13fc20c",
      "tls": {
        "enabled": true,
        "server_name": "www.ok.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "QNLEBa5tV9JCrubA4hlAWhho06ddr2dtsT8LKZsGTgA",
          "short_id": "fdc8125ea6f61323"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 93",
      "server": "212.111.85.50",
      "server_port": 443,
      "uuid": "b89d0b93-0ce0-424d-b9ab-92102acd5b84",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "vkvideo.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "IIeEqSkqXaAv5CJP2iCXbLrzLBFRm3oZS56hm9JcBFU",
          "short_id": "3c6d5f8fa530f0c5"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇰@FREE2CONFIG   § 94",
      "server": "45.92.176.55",
      "server_port": 2243,
      "uuid": "d7e2c1ec-b2ba-4a4c-a73a-c08f5bd7923b",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "rontgen.fasssst.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "_ee-ouMazAzx7Q4_cYhWbu6pw53-8VVpt7tuBuCXziU",
          "short_id": "e3cbc70477"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇷@FREE2CONFIG   § 95",
      "server": "62.60.148.21",
      "server_port": 443,
      "uuid": "39e5cc2f-1294-4a42-bb58-306a8be785e1",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "st.ozone.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "BkAG_uWeUj7BCHqYjrz1JyH0TMvO_KywubV7WJN17ho",
          "short_id": "ee6f3e8f44b1f0b6"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇹🇷@FREE2CONFIG   § 96",
      "server": "45.92.176.55",
      "server_port": 7443,
      "uuid": "34af7cb7-e8a4-4112-9068-2647be927d8e",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "rontgen.fasssst.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "aIY78eatULBUOdhH73u8t4SzMIwWTk9Fhl8kHTeDYCU",
          "short_id": "4f4f60951d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇷@FREE2CONFIG   § 97",
      "server": "62.60.157.37",
      "server_port": 443,
      "uuid": "d48ba610-6ef1-475b-9d33-be2a0db96f87",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "st.ozone.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "jVZNjr5dXzki9VxDHWg_zsiUjSrplC0mnZrG8tuP_2c",
          "short_id": "149adb1c3cb9ed11"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 98",
      "server": "217.16.18.132",
      "server_port": 1695,
      "uuid": "93a4f24a-9c98-43cb-a977-2d4ff9a50034",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "2XNPDFPtNzLVuc7xO4aI7SErQZzoOGpSK1nlaDfbvgs",
          "short_id": "c3607d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 99",
      "server": "217.16.18.103",
      "server_port": 1695,
      "uuid": "93a4f24a-9c98-43cb-a977-2d4ff9a50034",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "2XNPDFPtNzLVuc7xO4aI7SErQZzoOGpSK1nlaDfbvgs",
          "short_id": "c3607d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 100",
      "server": "217.16.27.244",
      "server_port": 8443,
      "uuid": "93a4f24a-9c98-43cb-a977-2d4ff9a50034",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "4Sh7Von0eMReBfgcJgumDIulw8gsWccoDrH3q5NrcVU",
          "short_id": "37b991c951a6cf"
        }
      },
      "transport": {
        "type": "grpc",
        "service_name": "ads.x5.ru",
        "idle_timeout": "15s",
        "ping_timeout": "15s"
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 101",
      "server": "217.16.24.170",
      "server_port": 443,
      "uuid": "a91e64f0-9295-499d-bf4a-661ad99d4938",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "8OsJx6xuHcpL_5e1w0U4bMBa-icevDgvvzNwPwZbORQ",
          "short_id": "5540e44a53c3d01c"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 102",
      "server": "217.16.27.244",
      "server_port": 1695,
      "uuid": "93a4f24a-9c98-43cb-a977-2d4ff9a50034",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "2XNPDFPtNzLVuc7xO4aI7SErQZzoOGpSK1nlaDfbvgs",
          "short_id": "c3607d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 103",
      "server": "51.250.85.241",
      "server_port": 443,
      "uuid": "c4a27e9c-8ffc-4ec5-b68e-2b634fe25a74",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "BgH8ba_xaAeLa5pyvwwJp6HT7i09aNoiAsE1HgTXXkU",
          "short_id": "3275b9d98d3b69fc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇮@FREE2CONFIG   § 104",
      "server": "217.16.24.170",
      "server_port": 8443,
      "uuid": "a91e64f0-9295-499d-bf4a-661ad99d4938",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "8OsJx6xuHcpL_5e1w0U4bMBa-icevDgvvzNwPwZbORQ",
          "short_id": "5540e44a53c3d01c"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇵🇱@FREE2CONFIG   § 105",
      "server": "51.250.109.47",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 106",
      "server": "51.250.20.121",
      "server_port": 443,
      "uuid": "20cf5921-f7fa-47c5-81ae-947fbef83a4d",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "bYPDMM7Z7s3brAUozWIqspE24dQwgHyI60lDRZvscVo",
          "short_id": "a20d3ed244c76426"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇸🇪@FREE2CONFIG   § 107",
      "server": "51.250.28.8",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 108",
      "server": "51.250.28.39",
      "server_port": 4248,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇵🇱@FREE2CONFIG   § 109",
      "server": "51.250.99.190",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 110",
      "server": "51.250.25.11",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇵🇱@FREE2CONFIG   § 111",
      "server": "51.250.21.113",
      "server_port": 7443,
      "uuid": "2f0e01f3-8c74-458e-a474-b4aa4ac879aa",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "J5ITJbg5FQFembAfkogKHHQB6DigsFXQxK7xu-QMWUs",
          "short_id": "a20d3ed244c76426"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇱🇹@FREE2CONFIG   § 112",
      "server": "51.250.21.113",
      "server_port": 4249,
      "uuid": "20cf5921-f7fa-47c5-81ae-947fbef83a4d",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "qq"
        },
        "reality": {
          "enabled": true,
          "public_key": "ggIR4bVSlStYnXMClNFeB0Uejk-zw8HQzjAA0j8F7Dc",
          "short_id": "a20d3ed244c76426"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 113",
      "server": "51.250.24.245",
      "server_port": 4249,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇳🇱@FREE2CONFIG   § 114",
      "server": "84.201.178.99",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG  § 115",
      "server": "51.250.106.20",
      "server_port": 4249,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇳🇱@FREE2CONFIG   § 116",
      "server": "45.8.144.27",
      "server_port": 443,
      "uuid": "3b13042c-f6af-4a21-9872-00c09ff7e5b9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "nr9.strelkavpn.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "P2vHFiKpYCiEDB3HeRfKMUuzGk_ZXW2wXmcna6BRJW4",
          "short_id": "76bd7b341f61ab"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇵🇱@FREE2CONFIG   § 117",
      "server": "51.250.109.47",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG  § 118",
      "server": "217.16.24.170",
      "server_port": 443,
      "uuid": "a91e64f0-9295-499d-bf4a-661ad99d4938",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "ios"
        },
        "reality": {
          "enabled": true,
          "public_key": "8OsJx6xuHcpL_5e1w0U4bMBa-icevDgvvzNwPwZbORQ",
          "short_id": "5540e44a53c3d01c"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 119",
      "server": "152.53.133.72",
      "server_port": 443,
      "uuid": "cbabe86a-40a5-46af-898f-d6eaac66e141",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "7a-5DF4-Xk8h1Ex0zG-0CcSBgdhAnLrofVQ0rRdiSD8",
          "short_id": "0990c9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 120",
      "server": "152.53.86.94",
      "server_port": 443,
      "uuid": "23914cf2-2d38-4402-8862-4b02c60b84d9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mtalk.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "dqzabPbB3PzzynPZdUe6AtyKH0FIdi0eIyQBvn9azE0",
          "short_id": "23"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 121",
      "server": "152.53.142.51",
      "server_port": 443,
      "uuid": "e371c3c9-4ebd-4a17-9915-ee1331c02e74",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients3.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "q6ayd3-xiVbHZqOFRWTqZ8ftHSPhzcWKno4nfO3uOjI",
          "short_id": "5df42470e9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 122",
      "server": "152.53.141.19",
      "server_port": 443,
      "uuid": "cd1091f1-8deb-4080-bf0d-19cc1ee0da02",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mesu.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "uh_HksISuPiZ-j3DG6m8MNhPBEEu__J-ILHQVv3pnRE",
          "short_id": "f08d17de7d6380"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG    § 123",
      "server": "80.249.131.236",
      "server_port": 444,
      "uuid": "48b2795f-de72-44ea-ae96-f635e5952d45",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "yt.fasssst.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "14S-a9NL1PacapqVE4ojKZeEM5995jFyfwS0xc9UtRk",
          "short_id": "7d20a73ab88583f8"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG    § 124",
      "server": "152.53.144.195",
      "server_port": 443,
      "uuid": "6a0ddf8c-79bb-4328-b35b-55f62ae98dbc",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Ru5SHhsknPugwt4gwVO8ZIm4YkiHA-OQoeS8ddPClDk",
          "short_id": "9d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG  § 125",
      "server": "152.53.145.111",
      "server_port": 443,
      "uuid": "5aad18e2-f53b-4927-a1ff-cda06c5d5b02",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "init.itunes.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "nc1sfrAmREkpj15hupqKM-l0t1_qlxvhUxgp2KvnpmE",
          "short_id": "d0"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 126",
      "server": "152.53.133.115",
      "server_port": 443,
      "uuid": "c1b1524f-549f-4a06-9bd1-86ec04b0a032",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "developer.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "z1mANGkdN1YaF6mpCULPlG4w2JfYnkxL3y0W4Frrqm4",
          "short_id": "88"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 127",
      "server": "152.53.187.28",
      "server_port": 443,
      "uuid": "e3af49ba-6a41-4fa1-8f21-f40d1f154c68",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "configuration.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "DJ1l1bgvwpj-SoHuC6eLVfzd3rp1zQmCV76fdVazMgc",
          "short_id": "173c58"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 128",
      "server": "152.53.142.129",
      "server_port": 443,
      "uuid": "5c00f0cb-905e-47ce-9b6b-2d4d137a1f9e",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "workers.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "BnwepsrMVlmIpiUMIOoAlBXJ5iZh5GMpgfjHuhwhklM",
          "short_id": "48"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG    § 129",
      "server": "152.53.135.122",
      "server_port": 443,
      "uuid": "c9fc7cb8-6dde-46e9-a682-8022e4b6900b",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "d1.awsstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "c3ZHON336aVBpNfV34OnFA5B-ocWtNa-kc29ql-flD0",
          "short_id": "63"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 130",
      "server": "51.250.24.245",
      "server_port": 4249,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇷@FREE2CONFIG    § 131",
      "server": "62.60.157.37",
      "server_port": 443,
      "uuid": "d48ba610-6ef1-475b-9d33-be2a0db96f87",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "st.ozone.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "jVZNjr5dXzki9VxDHWg_zsiUjSrplC0mnZrG8tuP_2c",
          "short_id": "149adb1c3cb9ed11"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG    § 132",
      "server": "152.53.133.244",
      "server_port": 443,
      "uuid": "615c6f31-eb83-4c09-8510-f1a0faadc8e8",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients2.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ytiNy-7llRPrWSHVUQL8ii6PEX29aTG-hS_NkCYaTBQ",
          "short_id": "1b9617"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇪🇪@FREE2CONFIG   § 133",
      "server": "45.92.176.55",
      "server_port": 1243,
      "uuid": "d29bde62-daa4-4804-9c69-6e23a4150006",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "rontgen.fasssst.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "jcJeCbLo5JtfveFIQLV6WNm1148XzxDc0Rzy336hXy0",
          "short_id": "ff3cef7cdcf9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 134",
      "server": "152.53.186.174",
      "server_port": 443,
      "uuid": "b58d778d-f393-4280-940f-61230dbdd491",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "frSr5idN1FqLyEdsujtTf-BnCDx35Eji65qIsXuqNCo",
          "short_id": "3938"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG    § 135",
      "server": "152.53.143.63",
      "server_port": 443,
      "uuid": "485fafeb-f806-40ad-996c-94e01ee84daf",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mtalk.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "lhwCcXyMGY8GEVV0wDTRsSApcOj-CM1fP8DRY0buRHg",
          "short_id": "eea9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇦🇪@FREE2CONFIG   § 136",
      "server": "217.195.200.224",
      "server_port": 443,
      "uuid": "1437fec7-064b-4f8f-98f4-8c9aad3738b0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "HZM7SXNCsT5M_zWuBURZfplLY-L5Gqww5qRPJZAP8C4",
          "short_id": "754dc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG    § 137",
      "server": "51.250.28.39",
      "server_port": 4248,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 138",
      "server": "152.53.133.132",
      "server_port": 443,
      "uuid": "4775848f-2595-4777-8524-b60b16c3cd79",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api.snapkit.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "bMd4ndQTVjCtOYI9nKspNZx_XZXmPgbrcfw20GZQckA",
          "short_id": "332d4a4e"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG    § 139",
      "server": "93.114.56.67",
      "server_port": 443,
      "uuid": "22eba6de-256f-4d92-8c79-9b66204d40b0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "init.itunes.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SOloMl69oKpNpX3b-Ec5n3chWjmprNQ_UnFvAzI-JxE",
          "short_id": "056a"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 140",
      "server": "5.181.21.72",
      "server_port": 443,
      "uuid": "e4b8df56-b680-4a34-ab47-5bf5738ed718",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "v9CxKfIPtkKH1cTGKEer-1i-3JL31vZPpPl2Ujnbjh8",
          "short_id": "85225c27630d023f"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 141",
      "server": "185.140.14.166",
      "server_port": 8443,
      "uuid": "9e460075-dcb2-504a-b3d9-aab5c3095442",
      "tls": {
        "enabled": true,
        "server_name": "www.microsoft.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "qdcM4h1uoHcpGw_QnU99NnUXgcjDFyoE-E1_Ili3Xgo",
          "short_id": "3471fa2412678660"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 142",
      "server": "152.53.133.12",
      "server_port": 443,
      "uuid": "f81d5b9b-c5b7-46cb-8710-0cf41ab33570",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "WeNlf_hPscBLSwtg1PgOmurK1f7VyQSNPmOYeG0wIQw",
          "short_id": "6590cb"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 143",
      "server": "188.68.36.138",
      "server_port": 443,
      "uuid": "fc200ee7-2643-4e20-9231-d8b87ac03935",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients3.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "X_03fRoDo9vm437UVnLT5m_ZbGa2A6p0qhBKSfZYvGk",
          "short_id": "9dce"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 144",
      "server": "152.53.142.188",
      "server_port": 443,
      "uuid": "8c8e79ba-6bf6-42dc-9f16-04947ebf5325",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "xp.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "MvVhNhJedr9JB7tNjJ8d0z7z6FfHwXqcPGkZ15A-QGY",
          "short_id": "9c7a"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG    § 145",
      "server": "152.53.87.20",
      "server_port": 443,
      "uuid": "6526d72e-95b3-460d-a2e6-1b0b66d18b60",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "developer.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "XjlDjEKKUfTB4uEdMjRYo35n8J_Rm1FQmvw87Mf4CTU",
          "short_id": "42fbfd"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 146",
      "server": "152.53.134.168",
      "server_port": 443,
      "uuid": "f6f74d98-8e6b-4f4a-8f88-79ae32f28edb",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ks76ikSkP9d-_uHJ5Ms_aEI6wjkXWvw7GEUxNBSp5T0",
          "short_id": "12d75b"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 147",
      "server": "152.53.144.46",
      "server_port": 443,
      "uuid": "9ddd1f39-e7e4-4d52-b202-7d7b2f13215a",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients2.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "4yvKWFMcxHUzMJCMupKIRvqw2gsCRsD_bfirrZ0LmAI",
          "short_id": "83e035aa57"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇰@FREE2CONFIG   § 148",
      "server": "45.92.176.55",
      "server_port": 2243,
      "uuid": "d7e2c1ec-b2ba-4a4c-a73a-c08f5bd7923b",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "rontgen.fasssst.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "_ee-ouMazAzx7Q4_cYhWbu6pw53-8VVpt7tuBuCXziU",
          "short_id": "e3cbc70477"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 149",
      "server": "89.58.55.196",
      "server_port": 443,
      "uuid": "1c83fafe-8107-46ed-a94c-1252de4ceba6",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "xp.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Y7WW7er4kSFYTxwTw8Lv7Iu-cPH0_Vt3kimM7vD9GHM",
          "short_id": "640054"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG     § 150",
      "server": "37.120.171.194",
      "server_port": 443,
      "uuid": "4974a3b2-ba08-47e0-806b-85fb45d038a0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mesu.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "WXPq4NT1gqVRO7IUJGU3tv0NDe8gxEVN2WGa1dwjiCk",
          "short_id": "1b89"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇺🇸@FREE2CONFIG   § 151",
      "server": "216.133.149.139",
      "server_port": 23581,
      "uuid": "b5471668-94dc-4ea5-ae97-3bb9dabcd2a9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "EOYTqph-go2SazIPcSDl5pJGNyOnrR0mWaL8Tc_paEM"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG    § 152",
      "server": "185.234.59.74",
      "server_port": 8443,
      "uuid": "4a3ece53-6000-4ba3-a9fa-fd0d7ba61cf3",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "stats.vk-portal.net",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "mLmBhbVFfNuo2eUgBh6r9-5Koz9mUCn3aSzlR6IejUg",
          "short_id": "175d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇹🇷@FREE2CONFIG   § 153",
      "server": "213.156.152.223",
      "server_port": 443,
      "uuid": "cb7188cf-2c3a-43a5-af90-d893922e4917",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "eS0NqJCAo6Jn4PuU3nU4A5D7RyNbn3WyhipXViddnzI",
          "short_id": "5457"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 154",
      "server": "152.53.142.189",
      "server_port": 443,
      "uuid": "e23b2103-c1c2-4035-858c-d5c7080e541f",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "configuration.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Cj72nKei-IJbaEG4olVgyKMmNUQn3NqpyHtHxGyqn2k",
          "short_id": "7ce392"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 155",
      "server": "152.53.141.19",
      "server_port": 443,
      "uuid": "cd1091f1-8deb-4080-bf0d-19cc1ee0da02",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mesu.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "uh_HksISuPiZ-j3DG6m8MNhPBEEu__J-ILHQVv3pnRE",
          "short_id": "f08d17de7d6380"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 156",
      "server": "188.68.36.138",
      "server_port": 443,
      "uuid": "fc200ee7-2643-4e20-9231-d8b87ac03935",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients3.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "X_03fRoDo9vm437UVnLT5m_ZbGa2A6p0qhBKSfZYvGk",
          "short_id": "9dce"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 157",
      "server": "128.140.94.109",
      "server_port": 443,
      "uuid": "80683c47-3706-406b-83b8-1d3695fb1bfb",
      "tls": {
        "enabled": true,
        "server_name": "www.ea.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "uJqfENqH6w2k1sM4qJo2m_nJMmOo91DCNmsxUhgjpQc",
          "short_id": "7b4a5e44"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇳🇱@FREE2CONFIG   § 158",
      "server": "185.82.73.212",
      "server_port": 8443,
      "uuid": "4a3ece53-6000-4ba3-a9fa-fd0d7ba61cf3",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "stats.vk-portal.net",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "mLmBhbVFfNuo2eUgBh6r9-5Koz9mUCn3aSzlR6IejUg",
          "short_id": "d3b13f31"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 159",
      "server": "152.53.133.12",
      "server_port": 443,
      "uuid": "f81d5b9b-c5b7-46cb-8710-0cf41ab33570",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "WeNlf_hPscBLSwtg1PgOmurK1f7VyQSNPmOYeG0wIQw",
          "short_id": "6590cb"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 160",
      "server": "152.53.133.72",
      "server_port": 443,
      "uuid": "cbabe86a-40a5-46af-898f-d6eaac66e141",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "7a-5DF4-Xk8h1Ex0zG-0CcSBgdhAnLrofVQ0rRdiSD8",
          "short_id": "0990c9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 161",
      "server": "152.53.147.46",
      "server_port": 443,
      "uuid": "9fe667f5-ffea-4272-a0b6-3abd73941c52",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "MrCEmqtF6MdAfyvwu7VWipCvi_8P0RjI8TF571XT6l0",
          "short_id": "209f"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 162",
      "server": "152.53.144.46",
      "server_port": 443,
      "uuid": "9ddd1f39-e7e4-4d52-b202-7d7b2f13215a",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients2.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "4yvKWFMcxHUzMJCMupKIRvqw2gsCRsD_bfirrZ0LmAI",
          "short_id": "83e035aa57"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 163",
      "server": "152.53.187.28",
      "server_port": 443,
      "uuid": "e3af49ba-6a41-4fa1-8f21-f40d1f154c68",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "configuration.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "DJ1l1bgvwpj-SoHuC6eLVfzd3rp1zQmCV76fdVazMgc",
          "short_id": "173c58"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 164",
      "server": "152.53.134.168",
      "server_port": 443,
      "uuid": "f6f74d98-8e6b-4f4a-8f88-79ae32f28edb",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ks76ikSkP9d-_uHJ5Ms_aEI6wjkXWvw7GEUxNBSp5T0",
          "short_id": "12d75b"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 165",
      "server": "217.16.24.170",
      "server_port": 443,
      "uuid": "a91e64f0-9295-499d-bf4a-661ad99d4938",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "8OsJx6xuHcpL_5e1w0U4bMBa-icevDgvvzNwPwZbORQ",
          "short_id": "5540e44a53c3d01c"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 166",
      "server": "152.53.142.51",
      "server_port": 443,
      "uuid": "e371c3c9-4ebd-4a17-9915-ee1331c02e74",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients3.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "q6ayd3-xiVbHZqOFRWTqZ8ftHSPhzcWKno4nfO3uOjI",
          "short_id": "5df42470e9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 167",
      "server": "152.53.133.244",
      "server_port": 443,
      "uuid": "615c6f31-eb83-4c09-8510-f1a0faadc8e8",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients2.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ytiNy-7llRPrWSHVUQL8ii6PEX29aTG-hS_NkCYaTBQ",
          "short_id": "1b9617"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 168",
      "server": "152.53.146.1",
      "server_port": 443,
      "uuid": "1808de5c-08db-4d3f-8688-34ed85a0322d",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "workers.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "LyhCTXS-yRgKZ052TlzwAs-hbj4n1qvJE2OLnbnCGDo",
          "short_id": "dab7"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 169",
      "server": "152.53.133.115",
      "server_port": 443,
      "uuid": "c1b1524f-549f-4a06-9bd1-86ec04b0a032",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "developer.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "z1mANGkdN1YaF6mpCULPlG4w2JfYnkxL3y0W4Frrqm4",
          "short_id": "88"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 170",
      "server": "37.120.171.194",
      "server_port": 443,
      "uuid": "4974a3b2-ba08-47e0-806b-85fb45d038a0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mesu.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "WXPq4NT1gqVRO7IUJGU3tv0NDe8gxEVN2WGa1dwjiCk",
          "short_id": "1b89"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 171",
      "server": "152.53.87.20",
      "server_port": 443,
      "uuid": "6526d72e-95b3-460d-a2e6-1b0b66d18b60",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "developer.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "XjlDjEKKUfTB4uEdMjRYo35n8J_Rm1FQmvw87Mf4CTU",
          "short_id": "42fbfd"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 172",
      "server": "152.53.135.122",
      "server_port": 443,
      "uuid": "c9fc7cb8-6dde-46e9-a682-8022e4b6900b",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "d1.awsstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "c3ZHON336aVBpNfV34OnFA5B-ocWtNa-kc29ql-flD0",
          "short_id": "63"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 173",
      "server": "152.53.186.174",
      "server_port": 443,
      "uuid": "b58d778d-f393-4280-940f-61230dbdd491",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "frSr5idN1FqLyEdsujtTf-BnCDx35Eji65qIsXuqNCo",
          "short_id": "3938"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇦🇲@FREE2CONFIG   § 174",
      "server": "91.132.132.109",
      "server_port": 8443,
      "uuid": "c44d64d3-bc91-43ba-9d59-3a0906e7a2bd",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "wWi-AH24-O27OYXsaT390rLPZY9hqBRYuvBGIZ9vzkk"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 175",
      "server": "152.53.144.195",
      "server_port": 443,
      "uuid": "6a0ddf8c-79bb-4328-b35b-55f62ae98dbc",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Ru5SHhsknPugwt4gwVO8ZIm4YkiHA-OQoeS8ddPClDk",
          "short_id": "9d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇵🇱@FREE2CONFIG   § 176",
      "server": "2.56.125.166",
      "server_port": 443,
      "uuid": "ee9b2135-b149-437e-995a-bfadfad342f5",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "hls-svod.itunes.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "llaiqC-oIhL_bjc236FPq26LSn7IVhIa4cIC6OVytws",
          "short_id": "31"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇮@FREE2CONFIG   § 177",
      "server": "109.61.17.127",
      "server_port": 443,
      "uuid": "0771a171-7eea-4272-a6b1-3e29478e4473",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "clients4.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "C5xoRWKopqNXP5xmZsJQdejPRIoZpzWRgrtlNticyQA",
          "short_id": "78e514cf"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 178",
      "server": "185.234.59.74",
      "server_port": 8443,
      "uuid": "2ca07504-c06a-41a4-b26b-99807a7d24cf",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "stats.vk-portal.net",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "mLmBhbVFfNuo2eUgBh6r9-5Koz9mUCn3aSzlR6IejUg",
          "short_id": "e499f276e7bd6420"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇪🇸@FREE2CONFIG   § 179",
      "server": "5.22.216.192",
      "server_port": 443,
      "uuid": "7392bb3b-7b2c-4eba-b399-b5e9534c12b0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "HO6w1kV0-nVwjEbAsPFfzRc_plvZjIXB9Ut11owI3Ec",
          "short_id": "066b"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 180",
      "server": "152.53.87.208",
      "server_port": 443,
      "uuid": "83787f92-2c0b-4217-9aea-bee4448331ec",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "fonts.gstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "xoeuO8vB3K-bPdSqcjlGV7MNJqJZ1KlJYGQydLB9vnU",
          "short_id": "c560cdc5"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 181",
      "server": "152.53.145.111",
      "server_port": 443,
      "uuid": "5aad18e2-f53b-4927-a1ff-cda06c5d5b02",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "init.itunes.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "nc1sfrAmREkpj15hupqKM-l0t1_qlxvhUxgp2KvnpmE",
          "short_id": "d0"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 182",
      "server": "152.53.141.213",
      "server_port": 443,
      "uuid": "13f395b3-5d40-43f9-bd94-55feaae1fa70",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "d1.awsstatic.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "KQ2kgnnjTCTNaHRBYu7-qmT9GnWefrPm3L67JrOw9wA",
          "short_id": "1d62"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 183",
      "server": "152.53.133.132",
      "server_port": 443,
      "uuid": "4775848f-2595-4777-8524-b60b16c3cd79",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api.snapkit.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "bMd4ndQTVjCtOYI9nKspNZx_XZXmPgbrcfw20GZQckA",
          "short_id": "332d4a4e"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇷@FREE2CONFIG   § 184",
      "server": "45.10.59.133",
      "server_port": 443,
      "uuid": "417a3a22-8019-4991-82e1-8e4e27e95022",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "9Bx-1do5J20bTshcos2BDFpgRfRHIig3MyRAJET11AY",
          "short_id": "07e75c2cb26c35"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 185",
      "server": "152.53.142.188",
      "server_port": 443,
      "uuid": "8c8e79ba-6bf6-42dc-9f16-04947ebf5325",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "xp.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "MvVhNhJedr9JB7tNjJ8d0z7z6FfHwXqcPGkZ15A-QGY",
          "short_id": "9c7a"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 186",
      "server": "152.53.142.129",
      "server_port": 443,
      "uuid": "5c00f0cb-905e-47ce-9b6b-2d4d137a1f9e",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "workers.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "BnwepsrMVlmIpiUMIOoAlBXJ5iZh5GMpgfjHuhwhklM",
          "short_id": "48"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 187",
      "server": "51.250.25.11",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇺🇸@FREE2CONFIG   § 188",
      "server": "216.133.149.139",
      "server_port": 23581,
      "uuid": "b5471668-94dc-4ea5-ae97-3bb9dabcd2a9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "EOYTqph-go2SazIPcSDl5pJGNyOnrR0mWaL8Tc_paEM"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇸🇪@FREE2CONFIG   § 189",
      "server": "95.111.208.215",
      "server_port": 443,
      "uuid": "902927e2-481e-4fc3-93e9-463b5cbf1663",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api.snapkit.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "BM8HKruNU-7Lg5Qb54Pv-qjdKwItDn_kY1S9vBPruAc",
          "short_id": "72d6"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 190",
      "server": "89.58.55.196",
      "server_port": 443,
      "uuid": "1c83fafe-8107-46ed-a94c-1252de4ceba6",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "xp.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Y7WW7er4kSFYTxwTw8Lv7Iu-cPH0_Vt3kimM7vD9GHM",
          "short_id": "640054"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 191",
      "server": "152.53.143.63",
      "server_port": 443,
      "uuid": "485fafeb-f806-40ad-996c-94e01ee84daf",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mtalk.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "lhwCcXyMGY8GEVV0wDTRsSApcOj-CM1fP8DRY0buRHg",
          "short_id": "eea9"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇦🇪@FREE2CONFIG   § 192",
      "server": "217.195.200.224",
      "server_port": 443,
      "uuid": "1437fec7-064b-4f8f-98f4-8c9aad3738b0",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ajax.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "HZM7SXNCsT5M_zWuBURZfplLY-L5Gqww5qRPJZAP8C4",
          "short_id": "754dc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇺🇸@FREE2CONFIG   § 193",
      "server": "107.173.148.58",
      "server_port": 443,
      "uuid": "b98d4c6e-6770-4a31-8256-a4750cdea0e7",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.amazon.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "0i_xAxYgSNx5NMpK2lOaWGS-CvAiD_LneYPO0MF0owo",
          "short_id": "1a"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇦🇲@FREE2CONFIG   § 194",
      "server": "77.91.68.70",
      "server_port": 55983,
      "uuid": "f667a096-5231-4cfb-8759-92bb32473139",
      "tls": {
        "enabled": true,
        "server_name": "yahoo.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "nWQ7b9l9X6N3PrXLgIzOvMM8iSYrqjVHEb9ikWxqYSg",
          "short_id": "0e"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇷@FREE2CONFIG   § 195",
      "server": "216.106.189.107",
      "server_port": 8443,
      "uuid": "4468ae8a-7741-42dd-be69-d75cd94c9b0e",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.microsoft.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "iHDnFIEsw6lD514kP0JNtP1h7zlQ6AEZn6nKICyOYlY",
          "short_id": "5eac66585cbd595c"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇺🇸@FREE2CONFIG   § 196",
      "server": "47.253.226.114",
      "server_port": 443,
      "uuid": "055a1ce8-2a16-4a0d-a2c2-22826c9b2413",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.cloudflare.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "Svl81isn16RPAFnjtmYw7A6TPnsEPLHuYYaJht65Rzc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇵🇱@FREE2CONFIG   § 197",
      "server": "2.56.125.209",
      "server_port": 49868,
      "uuid": "be015dd2-30b4-4fcf-a9ee-080c13ac13fb",
      "tls": {
        "enabled": true,
        "server_name": "yahoo.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "joEKL4Itljxodt1SOe1itSMrAH9bk_udpPtXgIjdu10",
          "short_id": "6d638e"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇨🇦@FREE2CONFIG   § 198",
      "server": "208.69.79.250",
      "server_port": 8443,
      "uuid": "89bb09d7-5a4b-4f6a-b73f-0ea67cb6f3a6",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.microsoft.com",
        "utls": {
          "enabled": true,
          "fingerprint": "safari"
        },
        "reality": {
          "enabled": true,
          "public_key": "ZnHyH5mL_cimo8JOfiosIRp-_IqvRVCzinNClSmsbVk",
          "short_id": "9b4be2de2162366d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇺🇸@FREE2CONFIG   § 199",
      "server": "47.251.25.74",
      "server_port": 443,
      "uuid": "18805ff3-b420-45de-af18-93be14024ae8",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "www.amazon.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "H56cOJhw0xw76lDEpt7IuJJmVGemK6_CK34KtHwDMX8"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇦🇺@FREE2CONFIG   § 200",
      "server": "192.9.162.122",
      "server_port": 1443,
      "uuid": "7a169e43-ff85-4572-9843-ba7207d07319",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "swdist.apple.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ZIBYUH_qQSeI1T6xImXG6MEZXP2yZW3NqGa8W69Cfyk",
          "short_id": "dde50f55d81116"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇰🇿@FREE2CONFIG   § 201",
      "server": "178.236.16.98",
      "server_port": 35728,
      "uuid": "a00d89f6-ab7e-4e30-a5e5-54c701d62c93",
      "tls": {
        "enabled": true,
        "server_name": "yahoo.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "vhUFNoFcvtZAVMo8y5K5eU2V43m5q6yjmWIhp5RkFng",
          "short_id": "69a2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇷@FREE2CONFIG   § 202",
      "server": "62.60.157.37",
      "server_port": 443,
      "uuid": "d48ba610-6ef1-475b-9d33-be2a0db96f87",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "st.ozone.ru",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "jVZNjr5dXzki9VxDHWg_zsiUjSrplC0mnZrG8tuP_2c",
          "short_id": "149adb1c3cb9ed11"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 203",
      "server": "152.53.86.94",
      "server_port": 443,
      "uuid": "23914cf2-2d38-4402-8862-4b02c60b84d9",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "mtalk.google.com",
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "dqzabPbB3PzzynPZdUe6AtyKH0FIdi0eIyQBvn9azE0",
          "short_id": "23"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇳🇱@FREE2CONFIG   § 204",
      "server": "185.82.73.212",
      "server_port": 8443,
      "uuid": "4a3ece53-6000-4ba3-a9fa-fd0d7ba61cf3",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "stats.vk-portal.net",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "mLmBhbVFfNuo2eUgBh6r9-5Koz9mUCn3aSzlR6IejUg",
          "short_id": "175d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 205",
      "server": "95.163.215.93",
      "server_port": 8443,
      "uuid": "b89d0b93-0ce0-424d-b9ab-92102acd5b84",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "ccfP5xSIpFgQVJIXA4Yj7fZ9Agjc9JVHvESTv3hnZjQ",
          "short_id": "62094d6a0b771c25"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 206",
      "server": "51.250.28.39",
      "server_port": 4248,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 207",
      "server": "185.234.59.74",
      "server_port": 8443,
      "uuid": "4a3ece53-6000-4ba3-a9fa-fd0d7ba61cf3",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "stats.vk-portal.net",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "mLmBhbVFfNuo2eUgBh6r9-5Koz9mUCn3aSzlR6IejUg",
          "short_id": "175d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 208",
      "server": "62.113.42.65",
      "server_port": 27121,
      "uuid": "cbf1ec03-2cff-4b1f-9eb5-5929c13fc20c",
      "tls": {
        "enabled": true,
        "server_name": "www.ok.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "QNLEBa5tV9JCrubA4hlAWhho06ddr2dtsT8LKZsGTgA",
          "short_id": "fdc8125ea6f61323"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 209",
      "server": "212.111.85.50",
      "server_port": 443,
      "uuid": "b89d0b93-0ce0-424d-b9ab-92102acd5b84",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "vkvideo.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "IIeEqSkqXaAv5CJP2iCXbLrzLBFRm3oZS56hm9JcBFU",
          "short_id": "3c6d5f8fa530f0c5"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇰@FREE2CONFIG   § 210",
      "server": "45.92.176.55",
      "server_port": 2243,
      "uuid": "d7e2c1ec-b2ba-4a4c-a73a-c08f5bd7923b",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "rontgen.fasssst.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "_ee-ouMazAzx7Q4_cYhWbu6pw53-8VVpt7tuBuCXziU",
          "short_id": "e3cbc70477"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇷@FREE2CONFIG   § 211",
      "server": "62.60.148.21",
      "server_port": 443,
      "uuid": "39e5cc2f-1294-4a42-bb58-306a8be785e1",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "st.ozone.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "BkAG_uWeUj7BCHqYjrz1JyH0TMvO_KywubV7WJN17ho",
          "short_id": "ee6f3e8f44b1f0b6"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇹🇷@FREE2CONFIG   § 212",
      "server": "45.92.176.55",
      "server_port": 7443,
      "uuid": "34af7cb7-e8a4-4112-9068-2647be927d8e",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "rontgen.fasssst.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "aIY78eatULBUOdhH73u8t4SzMIwWTk9Fhl8kHTeDYCU",
          "short_id": "4f4f60951d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇷@FREE2CONFIG   § 213",
      "server": "62.60.157.37",
      "server_port": 443,
      "uuid": "d48ba610-6ef1-475b-9d33-be2a0db96f87",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "st.ozone.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "jVZNjr5dXzki9VxDHWg_zsiUjSrplC0mnZrG8tuP_2c",
          "short_id": "149adb1c3cb9ed11"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 214",
      "server": "217.16.18.132",
      "server_port": 1695,
      "uuid": "93a4f24a-9c98-43cb-a977-2d4ff9a50034",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "2XNPDFPtNzLVuc7xO4aI7SErQZzoOGpSK1nlaDfbvgs",
          "short_id": "c3607d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 215",
      "server": "217.16.18.103",
      "server_port": 1695,
      "uuid": "93a4f24a-9c98-43cb-a977-2d4ff9a50034",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "2XNPDFPtNzLVuc7xO4aI7SErQZzoOGpSK1nlaDfbvgs",
          "short_id": "c3607d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 216",
      "server": "217.16.27.244",
      "server_port": 8443,
      "uuid": "93a4f24a-9c98-43cb-a977-2d4ff9a50034",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "4Sh7Von0eMReBfgcJgumDIulw8gsWccoDrH3q5NrcVU",
          "short_id": "37b991c951a6cf"
        }
      },
      "transport": {
        "type": "grpc",
        "service_name": "ads.x5.ru",
        "idle_timeout": "15s",
        "ping_timeout": "15s"
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 217",
      "server": "217.16.24.170",
      "server_port": 443,
      "uuid": "a91e64f0-9295-499d-bf4a-661ad99d4938",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "8OsJx6xuHcpL_5e1w0U4bMBa-icevDgvvzNwPwZbORQ",
          "short_id": "5540e44a53c3d01c"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 218",
      "server": "217.16.27.244",
      "server_port": 1695,
      "uuid": "93a4f24a-9c98-43cb-a977-2d4ff9a50034",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "2XNPDFPtNzLVuc7xO4aI7SErQZzoOGpSK1nlaDfbvgs",
          "short_id": "c3607d"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 219",
      "server": "51.250.85.241",
      "server_port": 443,
      "uuid": "c4a27e9c-8ffc-4ec5-b68e-2b634fe25a74",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "BgH8ba_xaAeLa5pyvwwJp6HT7i09aNoiAsE1HgTXXkU",
          "short_id": "3275b9d98d3b69fc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇫🇮@FREE2CONFIG   § 220",
      "server": "217.16.24.170",
      "server_port": 8443,
      "uuid": "a91e64f0-9295-499d-bf4a-661ad99d4938",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "8OsJx6xuHcpL_5e1w0U4bMBa-icevDgvvzNwPwZbORQ",
          "short_id": "5540e44a53c3d01c"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇵🇱@FREE2CONFIG   § 221",
      "server": "51.250.109.47",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 222",
      "server": "51.250.20.121",
      "server_port": 443,
      "uuid": "20cf5921-f7fa-47c5-81ae-947fbef83a4d",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "bYPDMM7Z7s3brAUozWIqspE24dQwgHyI60lDRZvscVo",
          "short_id": "a20d3ed244c76426"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇸🇪@FREE2CONFIG   § 223",
      "server": "51.250.28.8",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇷🇺@FREE2CONFIG   § 224",
      "server": "51.250.28.39",
      "server_port": 4248,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇵🇱@FREE2CONFIG   § 225",
      "server": "51.250.99.190",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 226",
      "server": "51.250.25.11",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇵🇱@FREE2CONFIG   § 227",
      "server": "51.250.21.113",
      "server_port": 7443,
      "uuid": "2f0e01f3-8c74-458e-a474-b4aa4ac879aa",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "J5ITJbg5FQFembAfkogKHHQB6DigsFXQxK7xu-QMWUs",
          "short_id": "a20d3ed244c76426"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇱🇹@FREE2CONFIG   § 228",
      "server": "51.250.21.113",
      "server_port": 4249,
      "uuid": "20cf5921-f7fa-47c5-81ae-947fbef83a4d",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "qq"
        },
        "reality": {
          "enabled": true,
          "public_key": "ggIR4bVSlStYnXMClNFeB0Uejk-zw8HQzjAA0j8F7Dc",
          "short_id": "a20d3ed244c76426"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG   § 229",
      "server": "51.250.24.245",
      "server_port": 4249,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇳🇱@FREE2CONFIG   § 230",
      "server": "84.201.178.99",
      "server_port": 1488,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "ads.x5.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "vless",
      "tag": "🇩🇪@FREE2CONFIG  § 231",
      "server": "51.250.106.20",
      "server_port": 4249,
      "uuid": "4a6de183-2ad3-456c-b420-feeac81f6257",
      "flow": "xtls-rprx-vision",
      "tls": {
        "enabled": true,
        "server_name": "api-maps.yandex.ru",
        "insecure": true,
        "utls": {
          "enabled": true,
          "fingerprint": "chrome"
        },
        "reality": {
          "enabled": true,
          "public_key": "SbVKOEMjK0sIlbwg4akyBg5mL5KZwwB-ed4eEE7YnRc",
          "short_id": "6ba85179e30d4fc2"
        }
      },
      "packet_encoding": "xudp"
    },
    {
      "type": "dns",
      "tag": "dns-out"
    },
    {
      "type": "direct",
      "tag": "direct"
    },
    {
      "type": "direct",
      "tag": "direct-fragment",
      "tls_fragment": {
        "enabled": true,
        "size": "10-30",
        "sleep": "2-8"
      }
    },
    {
      "type": "direct",
      "tag": "bypass"
    },
    {
      "type": "block",
      "tag": "block"
    }
  ],
  "route": {
    "rules": [
      {
        "inbound": "dns-in",
        "outbound": "dns-out"
      },
      {
        "port": 53,
        "outbound": "dns-out"
      },
      {
        "domain_suffix": ".ru",
        "outbound": "direct"
      },
      {
        "rule_set": [
          "geoip-ru",
          "geosite-ru"
        ],
        "outbound": "direct"
      }
    ],
    "rule_set": [
      {
        "type": "remote",
        "tag": "geoip-ru",
        "format": "binary",
        "url": "https://raw.githubusercontent.com/hiddify/hiddify-geo/rule-set/country/geoip-ru.srs",
        "update_interval": "120h0m0s"
      },
      {
        "type": "remote",
        "tag": "geosite-ru",
        "format": "binary",
        "url": "https://raw.githubusercontent.com/hiddify/hiddify-geo/rule-set/country/geosite-ru.srs",
        "update_interval": "120h0m0s"
      }
    ],
    "final": "select",
    "auto_detect_interface": true,
    "override_android_vpn": true
  },
  "experimental": {
    "cache_file": {
      "enabled": true,
      "path": "clash.db"
    },
    "clash_api": {
      "external_controller": "127.0.0.1:16756",
      "secret": "Xi0gt9XQvNR6ezOV"
    }
  }
}
