# Indonesian Vehicle License Plate Numbers

JSON file that contains data for all area codes (kode wilayah propinsi, kota, kabupaten) for vehicle license plate numbers in Indonesia (nopol atau nomor plat kendaraan). This JSON file is used on [pelatchat.com](https://pelatchat.com), which is one of my projects. 

[![N|Solid](https://images.prismic.io/pelatchat/40eee65f-41ea-4fd5-a75f-7faad87e5dde_DALL%C2%B7E+2023-06-18+11.53.25+-+cars+in+traffic.jpg?auto=compress,format)](https://pelatchat.com)

**About Plate Numbers in Indonesia**
Plate numbers in Indonesia are divided into 3 segments, especially for civilian vehicles (exclude institution vehicles such as police or military).

> Segment #1 Alphabet: `[A-Z]{1,2}` minimum 1 digit, maximum 2 digits
> Segment #2  Numeral: `d{1,4}` minimum 1 digit, maximum 4 digits, from 1 to 9999
> Segment #3  Alphabet: `[A-Z]{0,3}` maximum 3 digits, there's no minimum or it can be blank

The first segment is the code for the province or a combined area like JADETABEK (Jakarta, Depok, Tangerang, Bekasi). The second segment is a code for identification and type of vehicle (such as a car, motorbike or truck). The third segment is a code for identification and specific area (for region like city or subregion like regency) which is taken from the first letter of the third segment. We can identify the origin of the vehicle from which area as long as the third segment is present, the license plate number is not modified or fake.

**Example**
The plate number of `B 1704 CJE` is from `Tangerang, Banten` because the first segment is `B` where from `JADETABEK` area and the first letter in the third segment is `C` which is `Tangerang, Banten`.

```
"B": ["JADETABEK",
	{
		"U": "Jakarta Utara",
		"B": "Jakarta Barat",
		"P": "Jakarta Pusat",
		"T": "Jakarta Timur",
		"S": "Jakarta Selatan",
		"W": "Tangerang Selatan, Banten",
		"C": "Tangerang, Banten",
		"V": "Tangerang, Banten",
		"G": "Tangerang, Banten",
		"N": "Tangerang, Banten",
		"E": "Depok, Jawa Barat",
		"Z": "Depok, Jawa Barat",
		"F": "Bekasi, Jawa Barat",
		"K": "Bekasi, Jawa Barat"
	}
]
```

**Credits**
Region codes data source from [auto200.co.id](https://auto2000.co.id/berita-dan-tips/kode-plat-nomor-belakang).

