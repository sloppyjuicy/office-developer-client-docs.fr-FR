---
title: Parameter members (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 66215908f402ac74225c968fd4b6623f9a61ecd7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568767"
---
# <a name="parameter-members-dao"></a>Parameter members (DAO)

**S’applique à** : Access 2013, Office 2013

Un objet Parameter représente une valeur fournie à une requête. Le paramètre est associé à un objet QueryDef créé à partir d'une requête avec paramètres

## <a name="properties"></a>Propriétés

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></p></td>
<td><p><strong>NOTE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</p>
<p>Définit ou renvoit une valeur qui indique si un objet <strong><a href="parameter-object-dao.md">Parameter</a></strong> représente un paramètre d'entrée, de sortie, ou les deux, ou la valeur de retour de la procédure (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-name-property-dao.md">Name</a></strong></p></td>
<td><p>Renvoie le nom de l'objet spécifié. En lecture seule <strong>chaîne</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-type-property-dao.md">Type</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type <strong>Integer</strong> en lecture-écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-value-property-dao.md">Valeur</a></strong></p></td>
<td><p>Définit ou renvoie la valeur d'un objet. Type <strong>Variant</strong> en lecture/écriture.</p></td>
</tr>
</tbody>
</table>

