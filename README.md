# AusPostCodeCFWorker
A simple Cloudflare Worker-based API for looking up Australian suburbs to find their postcodes, and vice versa.

The API returns simple JSON search results, including the postcode (p), suburb (l) and state (s).

**Look up suburb names from postcodes:**

`GET https://cloudflareworker.example.com/pc/7330`

Response:

```
[
	{
		"p": 7330,
		"l": "TROWUTTA",
		"s": "TAS"
	},
	{
		"p": 7330,
		"l": "WEST MONTAGU",
		"s": "TAS"
    },
]
```

**Look up suburb names from postcodes:**

`GET https://cloudflareworker.example.com/pc/search?suburb=CARRARANG`

Response:

```
[
	{
		"p":6532,
		"l":"CARRARANG",
		"s":"WA"
	}
]
```

