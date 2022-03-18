---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c1e27cb129841fda08dd11a178d32474bfee0e8b
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558669"
---
# <a name="adcprop_asyncthreadpriority_enum"></a>ADCPROPASYNCTHREADPRIORITYENUM\_\_

**S’applique à** : Access 2013, Office 2013

Pour un objet [Recordset](recordset-object-ado.md) RDS, spécifie la priorité d’exécution du thème asynchrone qui recherche des données.

Utilisez ces constantes avec la propriété dynamique « **Background Thread Priority** » du **Recordset**, qui est référencée dans l’index des propriétés dynamiques ADO et expliquée dans la documentation [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).


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
<td><p><strong>adPriorityAboveNormal</strong></p></td>
<td><p>4</p></td>
<td><p>Définit le niveau de priorité, normal ou maximum.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPriorityBelowNormal</strong></p></td>
<td><p>2</p></td>
<td><p>Définit le niveau de priorité, minimum ou normal.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPriorityHighest</strong></p></td>
<td><p>5</p></td>
<td><p>Définit le niveau de priorité le plus élevé possible.</p></td>
</tr>
<tr class="even">
<td><p><strong>AdPriorityLowest</strong></p></td>
<td><p>1</p></td>
<td><p>Définit le niveau de priorité le plus bas possible.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPriorityNormal</strong></p></td>
<td><p>3</p></td>
<td><p>Définit le niveau de priorité normal.</p></td>
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
<td><p>AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.LOWEST</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.AdcPropAsyncThreadPriority.NORMAL</p></td>
</tr>
</tbody>
</table>

