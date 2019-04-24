---
title: SortColumn, propriété (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54e6df1f2a94bd59f1e4cf9f9c0be77d785a3048
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306887"
---
# <a name="sortcolumn-property-rds"></a>SortColumn, propriété (RDS)

**S’applique à** : Access 2013, Office 2013

Indique la colonne selon laquelle les enregistrements sont triés.

## <a name="syntax"></a>Syntaxe

*DataControl*. SortColumn = *chaîne*

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*DataControl* |Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Une valeur **String** qui représente le nom ou l'alias de la colonne selon laquelle les enregistrements sont triés.|

## <a name="remarks"></a>Remarques

Les propriétés **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) et [FilterColumn](filtercolumn-property-rds.md) fournissent les fonctionnalités de tri et filtrage sur le cache côté client. La fonctionnalité de tri organise les enregistrements par valeur dans une colonne. La fonctionnalité de filtrage affiche un sous-ensemble d’enregistrements basés sur des critères de recherche tandis que le [Recordset](recordset-object-ado.md) complet est conservé dans le cache. La méthode [Reset](reset-method-rds.md) exécute les critères et remplace le **Recordset** actuel par un **Recordset** actualisable.

Pour trier un **Recordset**, vous devez tout d'abord enregistrer toutes les modifications effectuées. Si vous utilisez le **RDS.DataControl**, vous pouvez utiliser la méthode [SubmitChanges](submitchanges-method-rds.md). Par exemple, si votre **objet RDS. DataControl** est nommé ADC1, votre code doit être ADC1. SubmitChanges. Si vous utilisez un **Recordset** ADO, vous pouvez utiliser sa méthode [UpdateBatch](updatebatch-method-ado.md). La méthode recommandée pour les objets **Recordset** créés avec la méthode **CreateRecordset** est [UpdateBatch](createrecordset-method-rds.md). Par exemple, votre code peut être myRS. UpdateBatch ou. Si vous utilisez un **Recordset** ADO, vous pouvez utiliser sa méthode [UpdateBatch](updatebatch-method-ado.md). La méthode recommandée pour les objets **Recordset** créés avec la méthode **CreateRecordset** est [UpdateBatch](createrecordset-method-rds.md). Par exemple, votre code peut être myRS. UpdateBatch ou ADC1. Recordset. UpdateBatch.

