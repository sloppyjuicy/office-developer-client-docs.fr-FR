---
title: À propos des constantes de devise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82253123
ms.localizationpriority: medium
ms.assetid: d94c740f-29e1-1e7f-39f6-8aa215f3111d
description: Pour mettre en forme un nombre en tant que valeur monétaire, vous pouvez utiliser la fonction CY et transmettre une constante facultative afin de définir la devise à utiliser. Les constantes monétaires peuvent être définies sous forme de numéros d’ID correspondant à un pays/une région ou sous forme de chaîne (placée entre guillemets) représentant une abréviation ISO 4217 de 3 caractères.
ms.openlocfilehash: 17e559e9c2cdc2a09ce437af5918ce4457b144dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608759"
---
# <a name="about-currency-constants"></a>À propos des constantes de devise

Pour mettre en forme un nombre en tant que valeur monétaire, vous pouvez utiliser la fonction CY et transmettre une constante facultative afin de définir la devise à utiliser. Les constantes monétaires peuvent être définies sous forme de numéros d’ID correspondant à un pays/une région ou sous forme de chaîne (placée entre guillemets) représentant une abréviation ISO 4217 de 3 caractères.
  
Si vous affichez des symboles monétaires ne figurant pas dans les paramètres régionaux du système, le symbole du dollar ($) est utilisé.
  
## <a name="ids-and-abbreviations"></a>ID et abréviations

|**ID**|**Abréviation**|**Currency**|
|:-----|:-----|:-----|
| 0  <br/> | SYS  <br/> | Utilise les paramètres du système  <br/> |
| 1  <br/> | XXX  <br/> | Met en forme sous forme de nombre  <br/> |
| 2 - 9  <br/> | Reserved  <br/> |
| 10  <br/> | EUR  <br/> | Euro  <br/> |
| 11  <br/> | USD  <br/> | Dollar américain  <br/> |
| 12   <br/> | ATS  <br/> | Schilling autrichien  <br/> |
| 13  <br/> | AUD  <br/> | Dollar australien  <br/> |
| 14   <br/> | BEF  <br/> | Franc belge  <br/> |
| 15   <br/> | CAD  <br/> | Dollar canadien  <br/> |
| 16   <br/> | CHF  <br/> | Franc suisse  <br/> |
| 17   <br/> | CNY  <br/> | Yuan renminbi chinois  <br/> |
| 18   <br/> | DEM  <br/> | Deutsche Mark  <br/> |
| 19  <br/> | DKK  <br/> | Couronne danoise  <br/> |
| 20  <br/> | ESP  <br/> | Peseta espagnole  <br/> |
|  21  <br/> | FIM  <br/> | Mark finlandais  <br/> |
| 22  <br/> | FRF  <br/> | Franc français  <br/> |
| 23  <br/> | GBP  <br/> | Livre sterling  <br/> |
| 24  <br/> | GRD  <br/> | Drachme  <br/> |
| 25  <br/> | HKD  <br/> | Dollar de la zone administrative spéciale de Hong Kong  <br/> |
| 26  <br/> | HUF  <br/> | Forint hongrois  <br/> |
| 27  <br/> | IDR  <br/> | Roupie indonésienne  <br/> |
| 28  <br/> | IEP  <br/> | Livre irlandaise  <br/> |
| 29  <br/> | ILS  <br/> | Shekel israélien  <br/> |
| 30  <br/> | ITL  <br/> | Lire  <br/> |
| 31  <br/> | JPY  <br/> | Yen  <br/> |
| 32  <br/> | KRW  <br/> | Won coréen  <br/> |
| 33  <br/> | LUF  <br/> | Franc luxembourgeois  <br/> |
| 34  <br/> | MXN  <br/> | Peso mexicain  <br/> |
| 35  <br/> | MYR  <br/> | Ringgit malais  <br/> |
| 36  <br/> | NLG  <br/> | Florin néerlandais  <br/> |
| 37  <br/> | NOK  <br/> | Couronne norvégienne  <br/> |
| 38  <br/> | NZD  <br/> | Dollar néo-zélandais  <br/> |
| 39  <br/> | PHP  <br/> | Peso philippin  <br/> |
| 40  <br/> | PLZ (Historique. Utiliser PLN.)  <br/> | Zloty polonais  <br/> |
| 41  <br/> | PTE  <br/> | Escudo portugais  <br/> |
| 42  <br/> | ROL  <br/> | Leu roumain  <br/> |
| 43  <br/> | RUR (Historique. Utiliser RUB.)  <br/> | Rouble russe  <br/> |
| 44  <br/> | SEK  <br/> | Couronne suédoise  <br/> |
| 45  <br/> | SGD  <br/> | Dollar de Singapour  <br/> |
| 46  <br/> | THB  <br/> | Baht thaïlandais  <br/> |
| 47  <br/> | TWD  <br/> | Nouveau dollar taïwanais  <br/> |
| 48  <br/> | XEU (Historique. Utiliser EUR.)  <br/> | ECU (pré-1998)  <br/> |
| 49  <br/> | YUN (Historique. Utiliser YUM.)  <br/> | Dinar yougoslave  <br/> |
| 50  <br/> | ZAR  <br/> | Rand sud-africain  <br/> |
| 51 - 55  <br/> | Reserved  <br/> |
| 56  <br/> | ARS  <br/> | Peso argentin  <br/> |
| 57  <br/> | BMD  <br/> | Dollar des Bermudes  <br/> |
| 58  <br/> | BOB  <br/> | Boliviano bolivien  <br/> |
| 59  <br/> | BRR (Historique. Utiliser BRL.)  <br/> | Cruzeiro real brésilien  <br/> |
| 60  <br/> | BSD  <br/> | Dollar des Bahamas  <br/> |
| 61  <br/> | CLP  <br/> | Peso chilien  <br/> |
| 62  <br/> | COP  <br/> | Peso colombien  <br/> |
| 63  <br/> | CRC  <br/> | Colon de Costa Rica  <br/> |
| 64  <br/> | CZK  <br/> | Couronne tchèque  <br/> |
| 65  <br/> | DOP  <br/> | Peso dominicain  <br/> |
| 66  <br/> | ECS  <br/> | Sucre équatorien  <br/> |
| 67  <br/> | EGP  <br/> | Livre égyptienne  <br/> |
| 68  <br/> | HNL  <br/> | Lempira hondurien  <br/> |
| 69  <br/> | INR  <br/> | Roupie indienne  <br/> |
| 70  <br/> | JMD  <br/> | Dollar jamaïcain  <br/> |
| 71  <br/> | JOD  <br/> | Dinar jordanien  <br/> |
| 72  <br/> | KWD  <br/> | Dinar koweïtien  <br/> |
| 73  <br/> | MOP  <br/> | Pataca de Macao  <br/> |
| 74  <br/> | CHOSE  <br/> | Córdoba nicaraguayen  <br/> |
| 75  <br/> | PAB  <br/> | Balboa panaméen  <br/> |
| 76  <br/> | PEN  <br/> | Nouveau sol péruvien  <br/> |
| 77  <br/> | PKR  <br/> | Roupie pakistanaise  <br/> |
| 78  <br/> | PYG  <br/> | Guaraní paraguayen  <br/> |
| 79  <br/> | SAR  <br/> | Riyal d’Arabie saoudite  <br/> |
| 80  <br/> | SIT  <br/> | Tolar slovène  <br/> |
| 81  <br/> | SKK  <br/> | Couronne slovaque  <br/> |
| 82  <br/> | SVC  <br/> | Colon salvadorien  <br/> |
| 83  <br/> | TRY  <br/> | Nouvelle Livre turque  <br/> |
| 84  <br/> | TTD  <br/> | Dollar de Trinidad et Tobago  <br/> |
| 85  <br/> | UYOU  <br/> | Peso uruguayen  <br/> |
| 86  <br/> | VEB  <br/> | Bolívar vénézuélien  <br/> |
| 87  <br/> | VND  <br/> | Dong vietnamien  <br/> |
| 88  <br/> | BRL  <br/> | Real brésilien  <br/> |
| 89  <br/> | PLN  <br/> | Zloty polonais  <br/> |
| 90  <br/> | RUB  <br/> | Rouble russe  <br/> |
| 91  <br/> | YUM  <br/> | Dinar yougoslave  <br/> |
| 92  <br/> | BYB (Historique. Utiliser BYR.)  <br/> | Rouble du Belarus  <br/> |
| 93  <br/> | UAH  <br/> | Hryvnia ukrainienne  <br/> |
| 94  <br/> | AFA  <br/> | Afghani (ajouté dans Visio 2002)  <br/> |
| 95  <br/> | TOUT  <br/> | Lek (ajouté dans Visio 2002)  <br/> |
| 96  <br/> | DZD  <br/> | Dinar algérien (ajouté dans Visio 2002)  <br/> |
| 97  <br/> | ADP  <br/> | Peseta d’Andorre (ajouté dans Visio 2002)  <br/> |
| 98  <br/> | AOA  <br/> | Nouveau kwanza (ajouté dans Visio 2002)  <br/> |
| 99  <br/> | XCD  <br/> | Dollar des Caraïbes de l’Est (ajouté dans Visio 2002)  <br/> |
| 100  <br/> | AMD  <br/> | Dram arménien (ajouté dans Visio 2002)  <br/> |
| 101  <br/> | AWG  <br/> | Florin arubain (ajouté dans Visio 2002)  <br/> |
| 102  <br/> | AZM  <br/> | Manat d’Azerbaïdjan (ajouté dans Visio 2002)  <br/> |
| 103  <br/> | BHD  <br/> | Dinar de Bahreïn (ajouté dans Visio 2002)  <br/> |
| 104  <br/> | BDT  <br/> | Taka (ajouté dans Visio 2002)  <br/> |
| 105  <br/> | BBD  <br/> | Dollar des Barbades (ajouté dans Visio 2002)  <br/> |
| 106  <br/> | BYR  <br/> | Rouble du Belarus (ajouté dans Visio 2002)  <br/> |
| 107  <br/> | BZD  <br/> | Dollar de Belize (ajouté dans Visio 2002)  <br/> |
| 108  <br/> | XOF  <br/> | Franc CFA BCEAO (ajouté dans Visio 2002)  <br/> |
| 109  <br/> | BTN  <br/> | Ngultrum (ajouté dans Visio 2002)  <br/> |
| 110  <br/> | CENTRE D’ACTIVITÉS  <br/> | Marks convertibles (ajouté dans Visio 2002)  <br/> |
| 111  <br/> | BWP  <br/> | Pula (ajouté dans Visio 2002)  <br/> |
| 112  <br/> | BND  <br/> | Dollar de Brunei (ajouté dans Visio 2002)  <br/> |
| 113  <br/> | BGL (Historique. Utiliser BGN.)  <br/> | Lev  <br/> |
| 114  <br/> | BGN  <br/> | Lev bulgare (ajouté dans Visio 2002)  <br/> |
| 115  <br/> | BIF  <br/> | Franc burundais (ajouté dans Visio 2002)  <br/> |
| 116  <br/> | KHR  <br/> | Riel (ajouté dans Visio 2002)  <br/> |
| 117  <br/> | XAF  <br/> | Franc CFA BEAC (ajouté dans Visio 2002)  <br/> |
| 118  <br/> | CVE  <br/> | Escudo du Cap Vert (ajouté dans Visio 2002)  <br/> |
| 119  <br/> | KYD  <br/> | Dollar des îles Cayman (ajouté dans Visio 2002)  <br/> |
| 120  <br/> | KMF  <br/> | Franc des Comores (ajouté dans Visio 2002)  <br/> |
| 121  <br/> | CDF  <br/> | Franc congolais (ajouté dans Visio 2002)  <br/> |
| 122  <br/> | HRK  <br/> | Kuna (ajouté dans Visio 2002)  <br/> |
| 123  <br/> | CUP  <br/> | Peso cubain (ajouté dans Visio 2002)  <br/> |
| 124  <br/> | CYP  <br/> | Livre cypriote (ajouté dans Visio 2002)  <br/> |
| 125  <br/> | DJF  <br/> | Franc de Djibouti (ajouté dans Visio 2002)  <br/> |
| 126  <br/> | TPE  <br/> | Escudo du Timor (ajouté dans Visio 2002)  <br/> |
| 127  <br/> | ERN  <br/> | Nakfa (ajouté dans Visio 2002)  <br/> |
| 128  <br/> | EEK  <br/> | Couronne (ajouté dans Visio 2002)  <br/> |
| 129  <br/> | ETB  <br/> | Birr ethiopien (ajouté dans Visio 2002)  <br/> |
| 130  <br/> | FKP  <br/> | Livre des îles Falkland (îles Malouines) (ajouté dans Visio 2002)  <br/> |
| 131  <br/> | FJD  <br/> | Dollar des Fidji (ajouté dans Visio 2002)  <br/> |
| 132  <br/> | XPF  <br/> | Franc CFP (ajouté dans Visio 2002)  <br/> |
| 133  <br/> | GMD  <br/> | Dalasi (ajouté dans Visio 2002)  <br/> |
| 134  <br/> | GEL  <br/> | Lari (ajouté dans Visio 2002)  <br/> |
| 135  <br/> | GHC  <br/> | Cedi (ajouté dans Visio 2002)  <br/> |
| 136  <br/> | GIP  <br/> | Livre de Gibraltar (ajouté dans Visio 2002)  <br/> |
| 137  <br/> | GTQ  <br/> | Quetzal (ajouté dans Visio 2002)  <br/> |
| 138  <br/> | GNF  <br/> | Franc guinéen (ajouté dans Visio 2002)  <br/> |
| 139  <br/> | GWP  <br/> | Peso de Guinée-Bissau (ajouté dans Visio 2002)  <br/> |
| 140  <br/> | GYD  <br/> | Dollar guyanais (ajouté dans Visio 2002)  <br/> |
| 141  <br/> | HTG  <br/> | Gourde (ajouté dans Visio 2002)  <br/> |
| 142  <br/> | ISK  <br/> | Couronne islandaise (ajouté dans Visio 2002)  <br/> |
| 143  <br/> | TRI  <br/> | Rial iranien (ajouté dans Visio 2002)  <br/> |
| 144  <br/> | IQD  <br/> | Dinar irakien (ajouté dans Visio 2002)  <br/> |
| 145  <br/> | KZT  <br/> | Tenge (ajouté dans Visio 2002)  <br/> |
| 146  <br/> | KES  <br/> | Shilling kenyan (ajouté dans Visio 2002)  <br/> |
| 147  <br/> | KPW  <br/> | Won nord-coréen (ajouté dans Visio 2002)  <br/> |
| 148  <br/> | KGS  <br/> | Som (ajouté dans Visio 2002)  <br/> |
| 149  <br/> | LAK  <br/> | Kip (ajouté dans Visio 2002)  <br/> |
| 150  <br/> | LVL (Historique. Utiliser EUR.)  <br/> | Lats letton (ajouté dans Visio 2002)  <br/> |
| 151  <br/> | LBP  <br/> | Livre libanaise (ajouté dans Visio 2002)  <br/> |
| 152  <br/> | LSL  <br/> | Loti (ajouté dans Visio 2002)  <br/> |
| 153  <br/> | LRD  <br/> | Dollar libérien (ajouté dans Visio 2002)  <br/> |
| 154  <br/> | LYD  <br/> | Dinar libyen (ajouté dans Visio 2002)  <br/> |
| 155  <br/> | LTL  <br/> | Litas (ajouté dans Visio 2002)  <br/> |
| 156  <br/> | MKD  <br/> | Denar (ajouté dans Visio 2002)  <br/> |
| 157  <br/> | MGF (Historique. Utiliser MGA.)  <br/> | Franc malgache (ajouté dans Visio 2002)  <br/> |
| 158  <br/> | MWK  <br/> | Kwacha (ajouté dans Visio 2002)  <br/> |
| 159  <br/> | MVR  <br/> | Rufiyaa (ajouté dans Visio 2002)  <br/> |
| 160  <br/> | MTL  <br/> | Lire maltaise (ajouté dans Visio 2002)  <br/> |
| 161  <br/> | MRO  <br/> | Ouguiya (ajouté dans Visio 2002)  <br/> |
| 162  <br/> | MUR  <br/> | Roupie mauricienne (ajouté dans Visio 2002)  <br/> |
| 163  <br/> | MDL  <br/> | Leu de Moldova (ajouté dans Visio 2002)  <br/> |
| 164  <br/> | MNT  <br/> | Tugrik (ajouté dans Visio 2002)  <br/> |
| 165  <br/> | MAD  <br/> | Dirham marocain (ajouté dans Visio 2002)  <br/> |
| 166  <br/> | MZM  <br/> | Metical (ajouté dans Visio 2002)  <br/> |
| 167  <br/> | MMK  <br/> | Kyat (ajouté dans Visio 2002)  <br/> |
| 168  <br/> | NAD  <br/> | Dollar de Namibie (ajouté dans Visio 2002)  <br/> |
| 169  <br/> | NPR  <br/> | Roupie népalaise (ajouté dans Visio 2002)  <br/> |
| 170  <br/> | ANG  <br/> | Florin des Antilles néerlandaises (ajouté dans Visio 2002)  <br/> |
| 171  <br/> | NGN  <br/> | Naira (ajouté dans Visio 2002)  <br/> |
| 172  <br/> | OMR  <br/> | Rial d’Oman (ajouté dans Visio 2002)  <br/> |
| 173  <br/> | PGK  <br/> | Kina (ajouté dans Visio 2002)  <br/> |
| 174  <br/> | QAR  <br/> | Rial du Qatar (ajouté dans Visio 2002)  <br/> |
| 175  <br/> | RWF  <br/> | Franc rwandais (ajouté dans Visio 2002)  <br/> |
| 176  <br/> | S HP  <br/> | Livre de Ste. Hélène (ajouté dans Visio 2002)  <br/> |
| 177  <br/> | WST  <br/> | Tala (ajouté dans Visio 2002)  <br/> |
| 178  <br/> | STD  <br/> | Dobra (ajouté dans Visio 2002)  <br/> |
| 179  <br/> | SCR  <br/> | Roupie seychelloise (ajouté dans Visio 2002)  <br/> |
| 180  <br/> | SLL  <br/> | Leone (ajouté dans Visio 2002)  <br/> |
| 181  <br/> | SBD  <br/> | Dollar des îles Salomon (ajouté dans Visio 2002)  <br/> |
| 182  <br/> | SOS  <br/> | Shilling somalien (ajouté dans Visio 2002)  <br/> |
| 183  <br/> | LKR  <br/> | Roupie sri lankaise (ajouté dans Visio 2002)  <br/> |
| 184  <br/> | SDD  <br/> | Dinar soudanais (ajouté dans Visio 2002)  <br/> |
| 185  <br/> | SRG  <br/> | Florin de Surinam (ajouté dans Visio 2002)  <br/> |
| 186  <br/> | SZL  <br/> | Lilangeni (ajouté dans Visio 2002)  <br/> |
| 187  <br/> | SYP  <br/> | Livre syrienne (ajouté dans Visio 2002)  <br/> |
| 188  <br/> | TJR (Historique. Utiliser TJS.)  <br/> | Rouble tajik  <br/> |
| 189  <br/> | TJS  <br/> | Somoni (ajouté dans Visio 2002)  <br/> |
| 190  <br/> | TZS  <br/> | Shilling tanzanien (ajouté dans Visio 2002)  <br/> |
| 191  <br/> | RETOUR AU DÉBUT  <br/> | Pa’anga (ajouté dans Visio 2002)  <br/> |
| 192  <br/> | TND  <br/> | Dinar tunisien (ajouté dans Visio 2002)  <br/> |
| 193  <br/> | TMM  <br/> | Manat (ajouté dans Visio 2002)  <br/> |
| 194  <br/> | UGX  <br/> | Shilling ougandais (ajouté dans Visio 2002)  <br/> |
| 195  <br/> | AED  <br/> | Dirham E.A.U (ajouté dans Visio 2002)  <br/> |
| 196  <br/> | UZS  <br/> | Sum d’Ouzbékistan (ajouté dans Visio 2002)  <br/> |
| 197  <br/> | VUV  <br/> | Vatu (ajouté dans Visio 2002)  <br/> |
| 198  <br/> | YER  <br/> | Riyal yéménite (ajouté dans Visio 2002)  <br/> |
| 199  <br/> | ZMK  <br/> | Kwacha (ajouté dans Visio 2002)  <br/> |
| 200  <br/> | ZWD  <br/> | Dollar du Zimbabwe (ajouté dans Visio 2002)  <br/> |
|201  <br/> |VEF  <br/> |Bolívar vénézuélien Fuerte (ajouté dans Visio 2010)  <br/> |
|202  <br/> |MGA  <br/> |Ariary malgache (ajouté dans Visio 2010)  <br/> |
|203  <br/> |RSD  <br/> |Dinar serbe (ajouté dans Visio 2010)  <br/> |
|204  <br/> |CSD (Historique. Utiliser RSD.)  <br/> |Dinar serbe (ajouté dans Visio 2010)  <br/> |
   

