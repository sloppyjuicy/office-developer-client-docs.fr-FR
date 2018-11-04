---
title: FilterCriterion, propriété (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9887551d4d8a141c8390764bcd23c98c59edc26
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950222"
---
# <a name="filtercriterion-property-rds"></a><span data-ttu-id="205be-102">FilterCriterion, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="205be-102">FilterCriterion property (RDS)</span></span>

<span data-ttu-id="205be-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="205be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="205be-104">Indique l'opérateur d'évaluation à utiliser dans la valeur du filtre.</span><span class="sxs-lookup"><span data-stu-id="205be-104">Indicates the evaluation operator to use in the filter value.</span></span>

## <a name="syntax"></a><span data-ttu-id="205be-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="205be-105">Syntax</span></span>

<span data-ttu-id="205be-106">*DataControl*. FilterCriterion = *chaîne*</span><span class="sxs-lookup"><span data-stu-id="205be-106">*DataControl*.FilterCriterion = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="205be-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="205be-107">Parameters</span></span>

|<span data-ttu-id="205be-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="205be-108">Parameter</span></span>|<span data-ttu-id="205be-109">Description</span><span class="sxs-lookup"><span data-stu-id="205be-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="205be-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="205be-110">*DataControl*</span></span> |<span data-ttu-id="205be-111">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="205be-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="205be-112">*String*</span><span class="sxs-lookup"><span data-stu-id="205be-112">*String*</span></span> |<span data-ttu-id="205be-113">Une valeur **String** indiquant l'opérateur d'évaluation de la [FilterValue](filtervalue-property-rds.md) sur les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="205be-113">A **String** value that specifies the evaluation operator of the [FilterValue](filtervalue-property-rds.md) to the records.</span></span> <span data-ttu-id="205be-114">Peut être l’une des opérations suivantes : \<, \<=, \>, \>=, = ou \< \>.</span><span class="sxs-lookup"><span data-stu-id="205be-114">Can be any one of the following: \<, \<=, \>, \>=, =, or \<\>.</span></span>|

## <a name="remarks"></a><span data-ttu-id="205be-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="205be-115">Remarks</span></span>

<span data-ttu-id="205be-p102">Les propriétés [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion** et [FilterColumn](filtercolumn-property-rds.md) fournissent les fonctionnalités de tri et filtrage sur le cache côté client. La fonctionnalité de tri organise les enregistrements par valeur dans une colonne. La fonctionnalité de filtrage affiche un sous-ensemble d'enregistrements basés sur des critères de recherche tandis que le [Recordset](recordset-object-ado.md) complet est conservé dans le cache. La méthode [Reset](reset-method-rds.md) exécute les critères et remplace le **Recordset** actuel par un **Recordset** actualisable.</span><span class="sxs-lookup"><span data-stu-id="205be-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion**, and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="205be-120">La «\!= « opérateur n’est pas valide pour **FilterCriterion**; Utilisez plutôt «\<\>».</span><span class="sxs-lookup"><span data-stu-id="205be-120">The "\!=" operator is not valid for **FilterCriterion**; instead, use "\<\>".</span></span>

<span data-ttu-id="205be-p103">Si les propriétés Filter et Sort sont définies et que vous appelez la méthode **Reset**, l'ensemble de lignes est tout d'abord filtré, puis trié. Dans les tris ascendants, les valeurs nulles sont en haut ; dans les tris descendants, les valeurs nulles sont en bas (le tri descendant est utilisé par défaut).</span><span class="sxs-lookup"><span data-stu-id="205be-p103">If both the filter and sort properties are set and you call the **Reset** method, the rowset is first filtered and then it is sorted. For ascending sorts, the null values are at the top; for descending sorts, null values are at the bottom (ascending is default behavior).</span></span>

