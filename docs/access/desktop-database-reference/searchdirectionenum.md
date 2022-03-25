---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7c0ce48cc245cd54eb088d0b5fcf3138f52a891e
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63725321"
---
# <a name="searchdirectionenum"></a>SearchDirectionEnum


**S’applique à** : Access 2013, Office 2013

Spécifie le sens d’une recherche d’enregistrement dans un [Recordset](recordset-object-ado.md).

<table>
<colgroup>
<col />
<col />
<col />
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
<td><p><strong>adSearchBackward</strong></p></td>
<td><p>-1</p></td>
<td><p>Recherche vers le début, en s’arrêtant en haut du <strong>Recordset</strong>. Si aucune correspondance n’est trouvée, le pointeur de l’enregistrement est placé sur <a href="bof-eof-properties-ado.md">BOF</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adSearchForward</strong></p></td>
<td><p>1</p></td>
<td><p>Recherche vers la fin, en s’arrêtant en bas du <strong>Recordset</strong>. Si aucune correspondance n’est trouvée, le pointeur de l’enregistrement est placé sur <a href="bof-eof-properties-ado.md">EOF</a>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.SearchDirection.BACKWARD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.SearchDirection.FORWARD</p></td>
</tr>
</tbody>
</table>

