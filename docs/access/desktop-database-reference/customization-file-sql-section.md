---
title: Section SQL du fichier de personnalisation
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 629c7a5601f35253f034bb9b488aef3c8a369fc5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622479"
---
# <a name="customization-file-sql-section"></a>Section SQL du fichier de personnalisation


**S’applique à** : Access 2013, Office 2013

La section **sql** peut contenir une nouvelle chaîne SQL qui remplace la chaîne de commande cliente. Si aucune chaîne SQL ne figure dans la section, celle-ci est ignorée.

La nouvelle chaîne SQL peut être *paramétrée*. En d'autres termes, les paramètres dans la chaîne SQL de la section **sql** (signalée par le caractère '?') peuvent être remplacés par les arguments correspondants dans un *identificateur* de la chaîne de commande cliente (il s'agit d'une liste séparée par des virgules entre parenthèses). L'identificateur et la liste des arguments ont un comportement similaire à celui d'un appel de fonction.

Par exemple, supposons que la chaîne de commande cliente est « CustomerByID(4) », l’en-tête de section SQL est SQL CustomerByID et la nouvelle chaîne de section SQL est « \[ SELECT FROM Customers WHERE \] \* CustomerID = ». Le handler génère , l’en-tête de section SQL est SQL CustomerByID et la nouvelle chaîne de section SQL est « \[ SELECT FROM Customers WHERE \] \* CustomerID = ». Le handler génère « SELECT FROM Customers WHERE CustomerID = 4 » et utilise cette chaîne pour interroger \* la source de données.

Si la nouvelle instruction SQL est une chaîne vide (""), la section est ignorée.

Si la chaîne de la nouvelle instruction SQL n'est pas valide, l'exécution de l'instruction échoue. Le paramètre client est ignoré. Vous pouvez avoir recours à cette programmation intentionnellement pour « désactiver » toutes les commandes SQL clientes en spécifiant :

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a>Syntaxe

Une chaîne d'entrée SQL de remplacement a la forme suivante :

**SQL=*sqlString***

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Quitter</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>SQL</strong></p></td>
<td><p>Chaîne littérale qui indique qu'il s'agit d'une entrée de section SQL.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>sqlString</em></strong></p></td>
<td><p>Chaîne SQL qui remplace la chaîne cliente.</p></td>
</tr>
</tbody>
</table>

