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
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="ac4af-102">SortColumn, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="ac4af-102">SortColumn property (RDS)</span></span>

<span data-ttu-id="ac4af-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac4af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ac4af-104">Indique la colonne selon laquelle les enregistrements sont triés.</span><span class="sxs-lookup"><span data-stu-id="ac4af-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac4af-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac4af-105">Syntax</span></span>

<span data-ttu-id="ac4af-106">*DataControl*. SortColumn = *Chaîne*</span><span class="sxs-lookup"><span data-stu-id="ac4af-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="ac4af-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac4af-107">Parameters</span></span>

|<span data-ttu-id="ac4af-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ac4af-108">Parameter</span></span>|<span data-ttu-id="ac4af-109">Description</span><span class="sxs-lookup"><span data-stu-id="ac4af-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ac4af-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="ac4af-110">*DataControl*</span></span> |<span data-ttu-id="ac4af-111">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="ac4af-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="ac4af-112">*String*</span><span class="sxs-lookup"><span data-stu-id="ac4af-112">*String*</span></span> |<span data-ttu-id="ac4af-113">Une valeur **String** qui représente le nom ou l'alias de la colonne selon laquelle les enregistrements sont triés.</span><span class="sxs-lookup"><span data-stu-id="ac4af-113">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ac4af-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac4af-114">Remarks</span></span>

<span data-ttu-id="ac4af-p101">Les propriétés **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) et [FilterColumn](filtercolumn-property-rds.md) fournissent les fonctionnalités de tri et filtrage sur le cache côté client. La fonctionnalité de tri organise les enregistrements par valeur dans une colonne. La fonctionnalité de filtrage affiche un sous-ensemble d’enregistrements basés sur des critères de recherche tandis que le [Recordset](recordset-object-ado.md) complet est conservé dans le cache. La méthode [Reset](reset-method-rds.md) exécute les critères et remplace le **Recordset** actuel par un **Recordset** actualisable.</span><span class="sxs-lookup"><span data-stu-id="ac4af-p101">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="ac4af-119">Pour trier un **Recordset**, vous devez tout d'abord enregistrer toutes les modifications effectuées.</span><span class="sxs-lookup"><span data-stu-id="ac4af-119">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="ac4af-120">Si vous utilisez le **RDS.DataControl**, vous pouvez utiliser la méthode [SubmitChanges](submitchanges-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="ac4af-120">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="ac4af-121">Par exemple, si votre **RDS. DataControl** est nommé ADC1, votre code serait ADC1. SubmitChanges .</span><span class="sxs-lookup"><span data-stu-id="ac4af-121">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="ac4af-122">Si vous utilisez un **Recordset** ADO, vous pouvez utiliser sa méthode [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ac4af-122">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="ac4af-123">La méthode recommandée pour les objets **Recordset** créés avec la méthode **CreateRecordset** est [UpdateBatch](createrecordset-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="ac4af-123">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="ac4af-124">Par exemple, votre code peut être myRS.UpdateBatch ou .</span><span class="sxs-lookup"><span data-stu-id="ac4af-124">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="ac4af-125">Si vous utilisez un **Recordset** ADO, vous pouvez utiliser sa méthode [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ac4af-125">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="ac4af-126">La méthode recommandée pour les objets **Recordset** créés avec la méthode **CreateRecordset** est [UpdateBatch](createrecordset-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="ac4af-126">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="ac4af-127">Par exemple, votre code peut être myRS.UpdateBatch ou ADC1. Recordset.UpdateBatch .</span><span class="sxs-lookup"><span data-stu-id="ac4af-127">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>

