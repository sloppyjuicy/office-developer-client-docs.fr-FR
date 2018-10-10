---
title: FilterColumn, propriété (RDS)
TOCTitle: FilterColumn Property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 459fc61dbb8c8b1eecffdea3d2c5d2f105b9212a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469936"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="1db36-102">FilterColumn, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="1db36-102">FilterColumn Property (RDS)</span></span>


<span data-ttu-id="1db36-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1db36-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="1db36-104">Indique la colonne sur laquelle portent les critères de filtre.</span><span class="sxs-lookup"><span data-stu-id="1db36-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="1db36-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1db36-105">Syntax</span></span>

<span data-ttu-id="1db36-106">*DataControl*. FilterColumn = *chaîne*</span><span class="sxs-lookup"><span data-stu-id="1db36-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="1db36-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1db36-107">Parameters</span></span>

  - <span data-ttu-id="1db36-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="1db36-108">*DataControl*</span></span>

  - <span data-ttu-id="1db36-109">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="1db36-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="1db36-110">*String*</span><span class="sxs-lookup"><span data-stu-id="1db36-110">*String*</span></span>

  - <span data-ttu-id="1db36-p101">Une valeur **String** qui spécifie la colonne sur laquelle porte les critères de filtrage. Les critères de filtre sont spécifiés dans la propriété [FilterCriterion](filtercriterion-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="1db36-p101">A **String** value that specifies the column on which to evaluate the filter criteria. The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="1db36-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="1db36-113">Remarks</span></span>

<span data-ttu-id="1db36-p102">Les propriétés [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) et **FilterColumn** fournissent les fonctionnalités de tri et filtrage sur le cache côté client. La fonctionnalité de tri organise les enregistrements par valeur dans une colonne. La fonctionnalité de filtrage affiche un sous-ensemble d'enregistrements basés sur des critères de recherche tandis que le [Recordset](recordset-object-ado.md) complet est conservé dans le cache. La méthode [Reset](reset-method-rds.md) exécute les critères et remplace le **Recordset** actuel par un **Recordset** actualisable.</span><span class="sxs-lookup"><span data-stu-id="1db36-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

