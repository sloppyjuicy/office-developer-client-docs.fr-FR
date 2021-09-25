---
title: PersistFormatEnum (référence de base de données de bureau Access)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 79b861831b4edadead1b49e6246de57ada874b55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565148"
---
# <a name="persistformatenum"></a>PersistFormatEnum

**S’applique à** : Access 2013, Office 2013

Spécifie le format dans lequel enregistrer un objet [Recordset](recordset-object-ado.md).

<br/>

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
<td><p><strong>adPersistADTG</strong></p></td>
<td><p>0</p></td>
<td><p>Indique le format Advanced Data TableGram (ADTG) de Microsoft.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPersistADO</strong></p></td>
<td><p>1</p></td>
<td><p>Indique que le format XML (Extensible Markup Language) propre à ADO sera utilisé. Cette valeur est identique à adPersistXML et autorise la compatibilité ascendante.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPersistXML</strong></p></td>
<td><p>1</p></td>
<td><p>Indique le format XML (Extensible Markup Language).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPersistProviderSpecific</strong></p></td>
<td><p>2</p></td>
<td><p>Indique que le fournisseur maintient <strong>Recordset</strong> à l'aide de son propre format.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.PersistFormat.ADTG</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.PersistFormat.XML</p></td>
</tr>
</tbody>
</table>

