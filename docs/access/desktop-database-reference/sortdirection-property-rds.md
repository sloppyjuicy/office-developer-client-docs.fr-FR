---
title: SortDirection, propriété (RDS)
TOCTitle: SortDirection property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fd09eb22d9f751ab1140db948356d2b168b30afb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711356"
---
# <a name="sortdirection-property-rds"></a>SortDirection, propriété (RDS)

**S’applique à**: Access 2013, Office 2013

Indique si l'ordre de tri est croissant ou décroissant.

## <a name="syntax"></a>Syntaxe

*DataControl*. SortDirection = *valeur*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*DataControl* |Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).|
|*Value* |Une valeur **booléenne** qui, lorsqu'elle est égale à **True**, indique que l'ordre de tri est croissant. **False** indique un ordre décroissant.|

## <a name="remarks"></a>Remarques

Les propriétés [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) et [FilterColumn](filtercolumn-property-rds.md) fournissent les fonctionnalités de tri et filtrage sur le cache côté client. La fonctionnalité de tri organise les enregistrements par valeur dans une colonne. La fonctionnalité de filtrage affiche un sous-ensemble d'enregistrements basés sur des critères de recherche tandis que le [Recordset](recordset-object-ado.md) complet est conservé dans le cache. La méthode **Reset** exécute les critères et remplace le **Recordset** actuel par un **Recordset** actualisable.

