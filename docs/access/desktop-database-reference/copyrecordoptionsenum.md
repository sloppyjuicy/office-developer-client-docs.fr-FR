---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 961077f4a11b54e84878a1a87b0ef4f9bf5dea3f
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633602"
---
# <a name="copyrecordoptionsenum"></a>CopyRecordOptionsEnum


**S’applique à** : Access 2013, Office 2013

Spécifie le fonctionnement de la méthode [CopyRecord](copyrecord-method-ado.md).

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
<td><p><strong>adCopyAllowEmulation</strong></p></td>
<td><p>4</p></td>
<td><p>Indique que le fournisseur <em>Source</em> essaye de simuler une copie à l’aide d’opérations de téléchargement et de chargement si cette méthode échoue parce que <em>Destination</em> se trouve sur un serveur différent ou si le fournisseur est différent de celui de la <em>Source</em>. Il est à noter que, selon les fonctions des fournisseurs, les performances peuvent varier, allant jusqu’à la perte de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyNonRecursive</strong></p></td>
<td><p>2</p></td>
<td><p>Copie le répertoire en cours, mais aucun de ses sous-répertoires, vers l'emplacement de destination. L'opération de copie n'est pas récursive.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCopyOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Remplace le fichier ou le répertoire si la <em>Destination</em> pointe sur un fichier ou un répertoire existant.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Par défaut. Effectue l'opération de copie par défaut : l'opération échoue si le fichier ou le répertoire de destination existe déjà, ou si l'opération effectue une copie récursive.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Ces constantes ne possèdent pas d'équivalent ADO/WFC.

