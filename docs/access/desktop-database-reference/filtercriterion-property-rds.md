---
title: FilterCriterion, propriété (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e290f51e134c331c3944e65da4fa6a0758384c0e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612119"
---
# <a name="filtercriterion-property-rds"></a>FilterCriterion, propriété (RDS)

**S’applique à** : Access 2013, Office 2013

Indique l'opérateur d'évaluation à utiliser dans la valeur du filtre.

## <a name="syntax"></a>Syntaxe

*DataControl*. FilterCriterion = *Chaîne*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*DataControl* |Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Une valeur **String** indiquant l'opérateur d'évaluation de la [FilterValue](filtervalue-property-rds.md) sur les enregistrements. Peut être l’une des valeurs suivantes : \<, \<=, \> , \> =, =, =, ou \<\> .|

## <a name="remarks"></a>Remarques

Les propriétés [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion** et [FilterColumn](filtercolumn-property-rds.md) fournissent les fonctionnalités de tri et filtrage sur le cache côté client. La fonctionnalité de tri organise les enregistrements par valeur dans une colonne. La fonctionnalité de filtrage affiche un sous-ensemble d’enregistrements basés sur des critères de recherche tandis que le [Recordset](recordset-object-ado.md) complet est conservé dans le cache. La méthode [Reset](reset-method-rds.md) exécute les critères et remplace le **Recordset** actuel par un **Recordset** actualisable.

\!L’opérateur « = » n’est pas valide pour **FilterCriterion**; à la place, utilisez « \<\> ».

Si les propriétés Filter et Sort sont définies et que vous appelez la méthode **Reset**, l'ensemble de lignes est tout d'abord filtré, puis trié. Dans les tris ascendants, les valeurs nulles sont en haut ; dans les tris descendants, les valeurs nulles sont en bas (le tri descendant est utilisé par défaut).

