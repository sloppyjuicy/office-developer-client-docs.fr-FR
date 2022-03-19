---
title: Présentation du fichier de personnalisation
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 89fa141fb6d4b97298ed27ee2431d4307bc6c6fa
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626401"
---
# <a name="understanding-the-customization-file"></a>Présentation du fichier de personnalisation


**S’applique à** : Access 2013, Office 2013

Chaque en-tête de section du fichier de personnalisation se compose de crochets (**\[\]**) contenant un type et un paramètre. Les quatre types de section sont signalés par les chaînes littérales **connect**, **sql**, **userlist** ou **logs**. Le paramètre est la chaîne littérale, la valeur par défaut, un identificateur spécifié par l'utilisateur ou rien.

En conséquence, chaque section est marquée par l'un des en-têtes de section suivants :

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

Les en-têtes de section comportent les parties suivantes.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Quitter</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>connect</strong></p></td>
<td><p>Chaîne littérale qui modifie une chaîne de connexion.</p></td>
</tr>
<tr class="even">
<td><p><strong>sql</strong></p></td>
<td><p>Chaîne littérale qui modifie une chaîne de commande.</p></td>
</tr>
<tr class="odd">
<td><p><strong>userlist</strong></p></td>
<td><p>Chaîne littérale qui modifie les droits d'accès d'un utilisateur spécifique.</p></td>
</tr>
<tr class="even">
<td><p><strong>logs</strong></p></td>
<td><p>Chaîne littérale qui spécifie un fichier journal dans lequel les erreurs liées aux opérations sont consignées.</p></td>
</tr>
<tr class="odd">
<td><p><strong>default</strong></p></td>
<td><p>Chaîne littérale utilisée si aucun identificateur n'a été spécifié ou trouvé.</p></td>
</tr>
<tr class="even">
<td><p><em>identificateur</em></p></td>
<td><p>Chaîne qui correspond à une chaîne de la chaîne <strong>connect</strong> ou <strong>command</strong>.</p>
<p></p>
<ul>
<li><p>Utilisez cette section si l'en-tête de section contient la chaîne <strong>connect</strong> et si la chaîne de l'identificateur figure dans la chaîne de connexion.</p></li>
<li><p>Utilisez cette section si l'en-tête de section contient la chaîne <strong>sql</strong> et si la chaîne de l'identificateur figure dans la chaîne de connexion.</p></li>
<li><p>Utilisez cette section si l'en-tête de section contient la chaîne <strong>userlist</strong> et si la chaîne de l'identificateur correspond à un identificateur de section <strong>connect</strong>.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


L'objet **DataFactory** appelle le gestionnaire et lui passe les paramètres clients. Le gestionnaire recherche les chaînes entières dans les paramètres clients qui correspondent aux identificateurs des en-têtes de section appropriés. Si la recherche est infructueuse, le contenu de cette section est appliqué aux paramètres clients.

Une section spécifique est utilisée dans les circonstances suivantes :

  - Une section **connect** est utilisée si la partie valeur du mot-clé de la chaîne de connexion « **Data Source=**_valeur_ » cliente correspond à un identificateur de section **connect***.*

  - Une section **sql** est utilisée si la chaîne de commande cliente contient une chaîne qui correspond à un identificateur de section **sql**.

  - Une section **connect** ou **sql** avec un paramètre par défaut est utilisée en l'absence d'identificateur correspondant.

  - Une section **userlist** est utilisée si l'identificateur de section **userlist** correspond à un identificateur de section **connect**. Si c'est le cas, le contenu de la section **userlist** est appliqué à la connexion régie par la section **connect**.

  - Si la chaîne de connexion ou de commande ne correspond pas à l'identificateur d'un en-tête de section **connect** ou **sql** et en l'absence d'un en-tête de section **connect** ou **sql** doté d'un paramètre par défaut, la chaîne cliente est utilisée telle quelle.

  - La section **logs** est utilisée chaque fois que l'objet **DataFactory** est utilisé.

