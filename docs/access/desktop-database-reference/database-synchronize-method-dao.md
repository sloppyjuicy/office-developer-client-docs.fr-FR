---
title: Database.Synchronize, méthode (DAO)
TOCTitle: Synchronize Method
ms:assetid: 5e716a4a-2430-8106-5c34-a02dd28bc4f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194659(v=office.15)
ms:contentKeyID: 48545137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053357
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: db468e09a89a4af3f6ffd6622395dcc83e131591
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630762"
---
# <a name="databasesynchronize-method-dao"></a>Database.Synchronize, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

Synchronise deux réplicas. (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* Synchronize(***DbPathName** _, _*_ExchangeType_**)

*expression* Variable qui représente un objet **Database**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DbPathName</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Chemin d'accès au réplica cible, avec lequel la base de données est synchronisée.</p></td>
</tr>
<tr class="even">
<td><p><em>ExchangeType</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> indiquant le sens de synchronisation des modifications entre les deux bases de données.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous utilisez **Synchronize** pour échanger des données et des modifications de conception entre deux bases de données. Les modifications de conception ont toujours lieu en premier. Les deux bases de données doivent se trouver au même niveau de conception avant de pouvoir échanger des données. Par exemple, un échange de type **dbRepExportChanges** peut entraîner des modifications de conception au niveau d’un réplica, même si les modifications de données ne circulent que de la base de données vers DbPathName.

Le réplica identifié dans DbPathName doit faire partie du même jeu de réplicas. Si les deux réplicas possèdent le même paramètre de propriété **ReplicaID** ou sont des réplicas-maîtres pour deux ensembles de réplicas différents, la synchronisation échoue.

Lorsque vous synchronisez deux réplicas sur Internet, vous devez utiliser la constante **dbRepSyncInternet**. Dans ce cas, vous spécifiez une adresse URL (Uniform Resource Locator) pour l’argument DbPathName au lieu de spécifier un chemin d’accès réseau local.


> [!NOTE]
> [!REMARQUE] Vous ne pouvez pas synchroniser des réplicas partiels avec d'autres réplicas partiels. Pour plus d'informations, reportez-vous à la méthode [PopulatePartial](database-populatepartial-method-dao.md).


