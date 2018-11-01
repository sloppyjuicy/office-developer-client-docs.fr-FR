---
title: FilterValue, propriété (RDS)
TOCTitle: FilterValue Property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 818a38c4c7d11442b1deb7ddeef72a828283c897
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887333"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="00a88-102">FilterValue, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="00a88-102">FilterValue Property (RDS)</span></span>


<span data-ttu-id="00a88-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="00a88-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="00a88-104">Indique la valeur selon laquelle filtrer les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="00a88-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a88-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00a88-105">Syntax</span></span>

<span data-ttu-id="00a88-106">*DataControl*. FilterValue = *chaîne*</span><span class="sxs-lookup"><span data-stu-id="00a88-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="00a88-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00a88-107">Parameters</span></span>

  - <span data-ttu-id="00a88-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="00a88-108">*DataControl*</span></span>

  - <span data-ttu-id="00a88-109">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="00a88-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="00a88-110">*String*</span><span class="sxs-lookup"><span data-stu-id="00a88-110">*String*</span></span>

  - <span data-ttu-id="00a88-111">Une valeur de **type String** qui représente la valeur selon laquelle filtrer les enregistrements (par exemple 'Programmer' ou 125).</span><span class="sxs-lookup"><span data-stu-id="00a88-111">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>

## <a name="remarks"></a><span data-ttu-id="00a88-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="00a88-112">Remarks</span></span>

<span data-ttu-id="00a88-p101">Les propriétés [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) et [FilterColumn](filtercolumn-property-rds.md) fournissent les fonctionnalités de tri et filtrage sur le cache côté client. La fonctionnalité de tri organise les enregistrements par valeur dans une colonne. La fonctionnalité de filtrage affiche un sous-ensemble d'enregistrements basés sur des critères de recherche tandis que le [Recordset](recordset-object-ado.md) complet est conservé dans le cache. La méthode [Reset](reset-method-rds.md) exécute les critères et remplace le **Recordset** actuel par un **Recordset** actualisable.</span><span class="sxs-lookup"><span data-stu-id="00a88-p101">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="00a88-117">Les valeurs NULL provoquent une erreur d'incompatibilité.</span><span class="sxs-lookup"><span data-stu-id="00a88-117">Null values result in a type mismatch error.</span></span>

