---
title: SortDirection, propriété (RDS)
TOCTitle: SortDirection property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0db4bd5661bc32cb6f9ce8191dd4ac5bad7eff4c
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950110"
---
# <a name="sortdirection-property-rds"></a><span data-ttu-id="5dc97-102">SortDirection, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="5dc97-102">SortDirection property (RDS)</span></span>

<span data-ttu-id="5dc97-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5dc97-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5dc97-104">Indique si l'ordre de tri est croissant ou décroissant.</span><span class="sxs-lookup"><span data-stu-id="5dc97-104">Indicates whether a sort order is ascending or descending.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc97-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5dc97-105">Syntax</span></span>

<span data-ttu-id="5dc97-106">*DataControl*. SortDirection = *valeur*</span><span class="sxs-lookup"><span data-stu-id="5dc97-106">*DataControl*.SortDirection = *value*</span></span>

## <a name="parameters"></a><span data-ttu-id="5dc97-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5dc97-107">Parameters</span></span>

|<span data-ttu-id="5dc97-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5dc97-108">Parameter</span></span>|<span data-ttu-id="5dc97-109">Description</span><span class="sxs-lookup"><span data-stu-id="5dc97-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5dc97-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="5dc97-110">*DataControl*</span></span> |<span data-ttu-id="5dc97-111">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="5dc97-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="5dc97-112">*Value*</span><span class="sxs-lookup"><span data-stu-id="5dc97-112">*Value*</span></span> |<span data-ttu-id="5dc97-p101">Une valeur **booléenne** qui, lorsqu'elle est égale à **True**, indique que l'ordre de tri est croissant. **False** indique un ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="5dc97-p101">A **Boolean** value that, when set to **True**, indicates the sort direction is ascending. **False** indicates descending order.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5dc97-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="5dc97-115">Remarks</span></span>

<span data-ttu-id="5dc97-p102">Les propriétés [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) et [FilterColumn](filtercolumn-property-rds.md) fournissent les fonctionnalités de tri et filtrage sur le cache côté client. La fonctionnalité de tri organise les enregistrements par valeur dans une colonne. La fonctionnalité de filtrage affiche un sous-ensemble d'enregistrements basés sur des critères de recherche tandis que le [Recordset](recordset-object-ado.md) complet est conservé dans le cache. La méthode **Reset** exécute les critères et remplace le **Recordset** actuel par un **Recordset** actualisable.</span><span class="sxs-lookup"><span data-stu-id="5dc97-p102">The [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

