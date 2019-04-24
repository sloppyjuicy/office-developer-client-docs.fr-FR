---
title: SeekEnum (référence de base de données de bureau Access)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f8334cbfc8e0f6a362a36e03984739d1d52b6f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314657"
---
# <a name="seekenum"></a>SeekEnum

**S’applique à** : Access 2013, Office 2013

Spécifie le type de [Seek](seek-method-ado.md) à exécuter.

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
<td><p>adSeekFirstEQ</p></td>
<td><p>0,1</p></td>
<td><p>Recherche la première clé égale à <em>KeyValues</em>.</p></td>
</tr>
<tr class="even">
<td><p>adSeekLastEQ</p></td>
<td><p>n°2</p></td>
<td><p>Recherche la dernière clé égale à <em>KeyValues</em>.</p></td>
</tr>
<tr class="odd">
<td><p>adSeekAfterEQ</p></td>
<td><p>4</p></td>
<td><p>Recherche soit une clé égale à <em>KeyValues</em>, soit l'emplacement théorique suivant.</p></td>
</tr>
<tr class="even">
<td><p>adSeekAfter</p></td>
<td><p>8bits</p></td>
<td><p>Recherche une clé à l'emplacement théorique suivant de la correspondance avec <em>KeyValues</em>.</p></td>
</tr>
<tr class="odd">
<td><p>adSeekBeforeEQ</p></td>
<td><p>Seiz</p></td>
<td><p>Recherche une clé égale à <em>KeyValues</em>, ou l'emplacement théorique suivant de cette correspondance.</p></td>
</tr>
<tr class="even">
<td><p>adSeekBefore</p></td>
<td><p>32</p></td>
<td><p>Recherche une clé juste avant l'emplacement théorique d'une correspondance avec <em>KeyValues</em>.</p></td>
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
<td><p>AdoEnums. Seek. FIRSTEQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Seek. LASTEQ</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Seek. AFTEREQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Seek. AFTER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Seek. BEFOREEQ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Seek. BEFORe</p></td>
</tr>
</tbody>
</table>

