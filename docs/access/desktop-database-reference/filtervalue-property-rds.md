---
title: FilterValue, propriété (RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70dca16f4a949cc6088779c1406e0c77cb477ba1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292404"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="d1df6-102">FilterValue, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="d1df6-102">FilterValue property (RDS)</span></span>

<span data-ttu-id="d1df6-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1df6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d1df6-104">Indique la valeur selon laquelle filtrer les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="d1df6-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1df6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1df6-105">Syntax</span></span>

<span data-ttu-id="d1df6-106">*DataControl*. FilterValue = *Chaîne*</span><span class="sxs-lookup"><span data-stu-id="d1df6-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="d1df6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1df6-107">Parameters</span></span>

|<span data-ttu-id="d1df6-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d1df6-108">Parameter</span></span>|<span data-ttu-id="d1df6-109">Description</span><span class="sxs-lookup"><span data-stu-id="d1df6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d1df6-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="d1df6-110">*DataControl*</span></span> |<span data-ttu-id="d1df6-111">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="d1df6-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="d1df6-112">*String*</span><span class="sxs-lookup"><span data-stu-id="d1df6-112">*String*</span></span> |<span data-ttu-id="d1df6-113">Valeur **de** chaîne qui représente une valeur de données avec laquelle filtrer les enregistrements (par exemple, « Programmeur » ou 125 ).</span><span class="sxs-lookup"><span data-stu-id="d1df6-113">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="d1df6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1df6-114">Remarks</span></span>

<span data-ttu-id="d1df6-115">Les propriétés [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) et [FilterColumn](filtercolumn-property-rds.md) fournissent les fonctionnalités de tri et filtrage sur le cache côté client.</span><span class="sxs-lookup"><span data-stu-id="d1df6-115">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="d1df6-116">La fonctionnalité de tri organise les enregistrements par valeur dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="d1df6-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="d1df6-117">La fonctionnalité de filtrage affiche un sous-ensemble d'enregistrements basés sur des critères de recherche tandis que le [Recordset](recordset-object-ado.md) complet est conservé dans le cache.</span><span class="sxs-lookup"><span data-stu-id="d1df6-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="d1df6-118">La méthode [Reset](reset-method-rds.md) exécute les critères et remplace le **Recordset** actuel par un **Recordset** actualisable.</span><span class="sxs-lookup"><span data-stu-id="d1df6-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="d1df6-119">Les valeurs NULL provoquent une erreur d'incompatibilité.</span><span class="sxs-lookup"><span data-stu-id="d1df6-119">Null values result in a type mismatch error.</span></span>

