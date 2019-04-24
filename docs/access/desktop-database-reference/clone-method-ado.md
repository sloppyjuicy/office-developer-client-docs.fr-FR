---
title: Clone, méthode-ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 095191bbfe55f2c38529cb1c260979c48dd2d5f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296345"
---
# <a name="clone-method-ado"></a>Clone, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Crée une copie de l'objet [Recordset](recordset-object-ado.md) à partir d'un objet **Recordset** existant. Spécifie éventuellement que le clone doit être en lecture seule.

## <a name="syntax"></a>Syntaxe

**Définir** *rstDuplicate*  =  *rstOriginal*. Clone (*LockType*)

## <a name="return-value"></a>Valeur renvoyée

Retourne une référence d'objet **Recordset**.

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*rstDuplicate* |Variable objet qui identifie la copie de l'objet **Recordset** à créer.|
|*rstOriginal* |Variable objet qui identifie l'objet **Recordset** à dupliquer.|
|*LockType* |Facultatif. Valeur [LockTypeEnum](locktypeenum.md) qui spécifie le type de verrou de l'objet **Recordset** d'origine ou un objet **Recordset** en lecture seule. Les valeurs valides sont **adLockUnspecified** ou **adLockReadOnly**.|

## <a name="remarks"></a>Remarques

Faites appel à la méthode **Clone** pour créer plusieurs copies de l'objet **Recordset**, notamment si vous voulez conserver plusieurs enregistrements actifs dans un jeu d'enregistrements donné. L'utilisation de la méthode **Clone** est plus efficace que la création et l'ouverture d'un nouvel objet **Recordset** avec la même définition que l'original.

Si elle existe, la propriété [Filter](filter-property-ado.md) de l'objet **Recordset** d'origine, n'est pas appliquée au clone. Définissez la propriété **Filter** du nouvel objet **Recordset** afin de filtrer les résultats. Le moyen le plus simple de copier une valeur **Filter** existante consiste à l'affecter directement de cette façon :

L'enregistrement actif du clone que vous venez de créer correspond au premier enregistrement.

Les modifications apportées à un objet **Recordset** apparaissent dans tous ses clones, quel que soit le type de curseur utilisé. Toutefois, après l'exécution de la méthode [Requery](requery-method-ado.md) sur l'objet **Recordset** d'origine, les clones ne sont plus synchronisés avec l'original.

De même que la fermeture de l'objet **Recordset** d'origine ne ferme pas ses clones, la fermeture d'un clone ne ferme pas l'original ni aucune autre copie.

Vous ne pouvez cloner qu'un objet **Recordset** prenant en charge les signets. Les valeurs de signet sont interchangeables ; cela signifie qu'une référence de signet d'un objet **Recordset** renvoie au même enregistrement dans l'un de ses clones.

Some **Recordset** events that are triggered will also fire in all **Recordset** clones. However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.

Par exemple, si vous modifiez la valeur d’un champ, un événement [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) est déclenché au niveau de l’objet **Recordset** modifié et de tous ses clones. Le paramètre *Fields* de l’événement **WillChangeField** d’un objet **Recordset** cloné (qui, lui, n’a pas été modifié) référencera simplement les champs de l’enregistrement actif du clone, qui peut correspondre à un enregistrement différent de celui de l’objet **Recordset** d’origine au niveau duquel la modification a été appliquée.

Le tableau suivant répertorie tous les événements **Recordset** et indique s'ils sont valides et s'ils sont déclenchés pour tous les clones de l'objet Recordset générés à l'aide de la méthode **Clone**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Événement</p></th>
<th><p>Déclenché au niveau des clones ?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchcomplete-event-ado.md">FetchComplete,</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress,</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></p></td>
<td><p>Non</p></td>
</tr>
</tbody>
</table>

