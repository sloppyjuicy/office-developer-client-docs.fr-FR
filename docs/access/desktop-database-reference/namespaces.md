---
title: Espaces de noms (référence de base de données de bureau Access)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 905edba502fcc2994be6f6b8e50a7200b66a82b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288624"
---
# <a name="namespaces"></a>Espaces de noms

**S’applique à** : Access 2013, Office 2013

Le format XML de persistance dans ADO utilise les quatre espaces de noms suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Préfixe</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>Fait référence à &quot;l'espace de&quot; noms XML-Data contenant les éléments et les attributs qui définissent le schéma de l' <strong>objet Recordset</strong>actif.</p></td>
</tr>
<tr class="even">
<td><p>couche</p></td>
<td><p>Fait référence à la spécification des définitions du type de données.</p></td>
</tr>
<tr class="odd">
<td><p>RS</p></td>
<td><p>Fait référence à l'espace de nom contenant les éléments et les attributs spécifiques aux propriétés et attributs d'un <strong>jeu d'enregistrements</strong> ADO.</p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>Fait référence au schéma du jeu de lignes actif.</p></td>
</tr>
</tbody>
</table>


Il est déconseillé au client d'ajouter ses propres balises dans ces espaces de noms, comme défini dans les caractéristiques. Par exemple, il est déconseillé de définir un espace de noms comme « urn:schemas-microsoft-com:rowset » et d'écrire ensuite quelque chose comme « rs:MaPropreBalise ». Pour en savoir plus sur les espaces de noms, voir [Espaces de noms XML](https://www.w3.org/tr/xml-names/).

> [!NOTE]
> [!REMARQUE] L'ID de la balise du schéma doit être « RowsetSchema » et les espaces de noms utilisés pour faire référence au schéma du jeu de lignes actif doivent pointer vers « #RowsetSchema ».

Notez que le préfixe de l'espace de noms, c'est-à-dire la partie à droite des deux points et à gauche du signe égal, est arbitraire.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

Vous pouvez lui attribuer n'importe quel nom à condition qu'il soit utilisé partout dans le document XML. ADO écrit toujours « s », « rs », « dt » et « z », mais ces préfixes ne sont pas pré-programmés dans le composant de chargement.



