---
title: Database.Version, propriété (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ea3d061025619ec2368b1cc3c732c82b2f291ba4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581545"
---
# <a name="databaseversion-property-dao"></a>Database.Version, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Dans un espace de travail Microsoft Access, renvoie la version du moteur de base de données Microsoft Jet ou Microsoft Access qui a créé la base de données. Valeur **String** en lecture seule

## <a name="syntax"></a>Syntaxe

*.* Version

*expression* Variable qui représente un objet **Database**.

## <a name="remarks"></a>Remarques

La valeur de retour est une chaîne (type de données String) qui est évaluée à un numéro de version et mise en forme comme suit.

- Espace de travail Microsoft Access : numéro de version sous la forme « *version.inter* ». Par exemple, « 3.0 ». Le numéro de version du produit est constitué du numéro de version (3), d’un point et du numéro de version intermédiaire (0).

Le tableau suivant montre la version du moteur de base de données incluse dans différentes versions de produits Microsoft.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Moteur de base de données</p></th>
<th><p>Version (année de sortie)</p></th>
<th><p>Microsoft Access</p></th>
<th><p>Microsoft Visual Basic</p></th>
<th><p>Microsoft Excel</p></th>
<th><p>Microsoft Visual C++</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>1.0 (1992)</p></td>
<td><p>1.0</p></td>
<td><p>N/A</p></td>
<td><p>N/A</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>1.1 (1993)</p></td>
<td><p>1.1</p></td>
<td><p>3.0</p></td>
<td><p>N/A</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>2.0 (1994)</p></td>
<td><p>2.0</p></td>
<td><p>N/A</p></td>
<td><p>N/A</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>2.5 (1995)</p></td>
<td><p>N/A</p></td>
<td><p>4.0 (16 bits)</p></td>
<td><p>N/A</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>3.0 (1995)</p></td>
<td><p>‘95 (7.0)</p></td>
<td><p>4.0 (32 bits)</p></td>
<td><p>‘95 (7.0)</p></td>
<td><p>4.x</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>3.5 (1996)</p></td>
<td><p>‘97 (8.0)</p></td>
<td><p>5.0</p></td>
<td><p>‘97 (8.0)</p></td>
<td><p>5.0</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>4.0 (2000)</p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Moteur de base de données Microsoft Access</p></td>
<td><p>12.0 (2007)</p></td>
<td><p>2007</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

