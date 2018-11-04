---
title: Méthode DBEngine.SetOption (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2d6d40d88051e708944dadfabb984d44cc8c5cbc
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949886"
---
# <a name="dbenginesetoption-method-dao"></a>Méthode DBEngine.SetOption (DAO)

**S’applique à**: Access 2013, Office 2013

Remplace temporairement les valeurs des clés du moteur de base de données Microsoft Access dans le Registre de Windows (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . SetOption (***Option***, ***valeur***)

*expression* Expression qui renvoie un objet **DBEngine** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Entier long</strong></p></td>
<td><p>Constante décrite dans les Notes.</p></td>
</tr>
<tr class="even">
<td><p><em>Valeur</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>La valeur que vous souhaitez définir l’option.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Chaque constante renvoie à la clé de Registre correspondante dans le chemin d’accès HKEY\_LOCAL\_ordinateur\\logiciel\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\moteurs\\ACE (autrement dit, **dbSharedAsyncDelay** correspond à la clé HKEY\_LOCAL\_ordinateur\\logiciel\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\moteurs\\ACE \\SharedAsyncDelay, et ainsi de suite).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbPageTimeout</strong></p></td>
<td><p>Clé PageTimeout</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSharedAsyncDelay</strong></p></td>
<td><p>Clé SharedAsyncDelay</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbExclusiveAsyncDelay</strong></p></td>
<td><p>Clé ExclusiveAsyncDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLockRetry</strong></p></td>
<td><p>Clé LockRetry</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbUserCommitSync</strong></p></td>
<td><p>Clé UserCommitSync</p></td>
</tr>
<tr class="even">
<td><p><strong>dbImplicitCommitSync</strong></p></td>
<td><p>Clé ImplicitCommitSync</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbMaxBufferSize</strong></p></td>
<td><p>Clé MaxBufferSize</p></td>
</tr>
<tr class="even">
<td><p><strong>dbMaxLocksPerFile</strong></p></td>
<td><p>Clé MaxLocksPerFile</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLockDelay</strong></p></td>
<td><p>Clé LockDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbRecycleLVs</strong></p></td>
<td><p>Clé RecycleLVs</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFlushTransactionTimeout</strong></p></td>
<td><p>Clé FlushTransactionTimeout</p></td>
</tr>
</tbody>
</table>


Utilisez la méthode **SetOption** pour remplacer les valeurs de registre lors de l'exécution. Les nouvelles valeurs définies avec la méthode **SetOption** restent activées tant qu'elles ne sont pas modifiées de nouveau par un autre appel de la méthode **SetOption** ou que l'objet **DBEngine** n'est pas fermé.

