---
title: XactAttributeEnum (référence de base de données de bureau Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7a8de78fb8d12684f117ddc6adef80a48f9a4fe3
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461791"
---
# <a name="xactattributeenum"></a>XactAttributeEnum

**S’applique à** : Access 2013, Office 2013

Spécifie les attributs de transaction d’un objet [Connection](connection-object-ado.md).


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
<td><p><strong>adXactAbortRetaining</strong></p></td>
<td><p>262144</p></td>
<td><p>effectue des abandons de rétention ; autrement dit, <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">l’appel de RollbackTrans</a> démarre automatiquement une nouvelle transaction. Les fournisseurs ne prennent pas tous en charge cette fonctionnalité.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactCommitRetaining</strong></p></td>
<td><p>131072</p></td>
<td><p>Effectue des validations de rétention ; autrement dit, <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">l’appel de CommitTrans</a> démarre automatiquement une nouvelle transaction. Les fournisseurs ne prennent pas tous en charge cette fonctionnalité.</p></td>
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
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.XactAttribute.ABORTRETAINING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.XactAttribute.COMMITRETAINING</p></td>
</tr>
</tbody>
</table>

