---
title: FilterColumn, propriété (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d29c591c88de4b53535c26430bf369cbd3f53284
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292439"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="50e94-102">FilterColumn, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="50e94-102">FilterColumn property (RDS)</span></span>

<span data-ttu-id="50e94-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50e94-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50e94-104">Indique la colonne sur laquelle portent les critères de filtre.</span><span class="sxs-lookup"><span data-stu-id="50e94-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e94-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50e94-105">Syntax</span></span>

<span data-ttu-id="50e94-106">*DataControl*. FilterColumn = *Chaîne*</span><span class="sxs-lookup"><span data-stu-id="50e94-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="50e94-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50e94-107">Parameters</span></span>

|<span data-ttu-id="50e94-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="50e94-108">Parameter</span></span>|<span data-ttu-id="50e94-109">Description</span><span class="sxs-lookup"><span data-stu-id="50e94-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="50e94-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="50e94-110">*DataControl*</span></span> |<span data-ttu-id="50e94-111">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="50e94-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="50e94-112">*String*</span><span class="sxs-lookup"><span data-stu-id="50e94-112">*String*</span></span> |<span data-ttu-id="50e94-p101">Une valeur **String** qui spécifie la colonne sur laquelle porte les critères de filtrage. Les critères de filtre sont spécifiés dans la propriété [FilterCriterion](filtercriterion-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="50e94-p101">A **String** value that specifies the column on which to evaluate the filter criteria. The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="50e94-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="50e94-115">Remarks</span></span>

<span data-ttu-id="50e94-116">Les propriétés [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) et **FilterColumn** fournissent les fonctionnalités de tri et filtrage sur le cache côté client.</span><span class="sxs-lookup"><span data-stu-id="50e94-116">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="50e94-117">La fonctionnalité de tri organise les enregistrements par valeur dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="50e94-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="50e94-118">La fonctionnalité de filtrage affiche un sous-ensemble d'enregistrements basés sur des critères de recherche tandis que le [Recordset](recordset-object-ado.md) complet est conservé dans le cache.</span><span class="sxs-lookup"><span data-stu-id="50e94-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> 

<span data-ttu-id="50e94-119">La méthode [Reset](reset-method-rds.md) exécute les critères et remplace le **Recordset** actuel par un **Recordset** actualisable.</span><span class="sxs-lookup"><span data-stu-id="50e94-119">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

