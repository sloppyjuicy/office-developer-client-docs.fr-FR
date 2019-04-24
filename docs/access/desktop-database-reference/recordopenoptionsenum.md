---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caaf755ebd63f1805d0c77ef79a0f5863a85050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300685"
---
# <a name="recordopenoptionsenum"></a>RecordOpenOptionsEnum


**S’applique à** : Access 2013, Office 2013

Spécifie des options pour l'ouverture d'un [Record](record-object-ado.md). Les valeurs peuvent être combinées en utilisant OR.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adDelayFetchFields</strong></p></td>
<td><p>0x8000</p></td>
<td><p>Indique au fournisseur que les champs associés au <strong>Record</strong> n'ont pas besoin d'être extraits tout de suite ; ils peuvent l'être à la première tentative d'accès. Le fonctionnement par défaut, indiqué par l'absence de cet indicateur, est d'extraire tous les champs de l'objet <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelayFetchStream</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Indique au fournisseur que la chaîne de données par défaut associée au <strong>Record</strong> n'a pas besoin d'être extraite tout de suite. Le fonctionnement par défaut, indiqué par l'absence de cet indicateur, est d'extraire la chaîne par défaut associée à l'objet <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenAsync</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Indique que l’objet <strong>Record</strong> est ouvert en mode asynchrone.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenExecuteCommand</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Indique que la chaîne source contient le texte des commandes qui doivent être exécutées. Cette valeur est équivalente à l'option <strong>adCmdText</strong> de <strong>Recordset.Open</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenRecordUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Par défaut. Indique qu'aucune option n'est spécifiée.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenOutput</strong></p></td>
<td><p>0x800000</p></td>
<td><p>Indique que si la source pointe sur un nœud contenant un script exécutable (comme une page .ASP), le <strong>Record</strong> ouvert contiendra le résultat de ce script. Cette valeur n'est valide qu'avec les enregistrements sans collection.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Ces constantes ne possèdent pas d'équivalent ADO/WFC.

