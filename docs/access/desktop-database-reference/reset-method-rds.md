---
title: Reset, méthode (RDS - référence du bureau de la base de données Access)
TOCTitle: Reset Method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3932eaab38498b8c82256ceb0de49a9c78030cdd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470824"
---
# <a name="reset-method-rds"></a><span data-ttu-id="1973d-102">Reset, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="1973d-102">Reset Method (RDS)</span></span>


<span data-ttu-id="1973d-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1973d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1973d-104">Applique un tri ou un filtre à un objet **Recordset** côté client en fonction des propriétés de tri et de filtre spécifiées.</span><span class="sxs-lookup"><span data-stu-id="1973d-104">Executes the sort or filter on a client-side **Recordset** based on the specified sort and filter properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1973d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1973d-105">Syntax</span></span>

<span data-ttu-id="1973d-106">*DataControl*. Réinitialisation (*valeur*)</span><span class="sxs-lookup"><span data-stu-id="1973d-106">*DataControl*.Reset(*value*)</span></span>

## <a name="parameters"></a><span data-ttu-id="1973d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1973d-107">Parameters</span></span>

  - <span data-ttu-id="1973d-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="1973d-108">*DataControl*</span></span>

  - <span data-ttu-id="1973d-109">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="1973d-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="1973d-110">*valeur*</span><span class="sxs-lookup"><span data-stu-id="1973d-110">*value*</span></span>

  - <span data-ttu-id="1973d-p101">Facultatif. Valeur de type **Boolean**. Si la valeur est **True** (par défaut), cela permet d'effectuer un filtrage sur l'ensemble de lignes « filtré » actuel. Si la valeur est **False**, le filtrage porte sur l'ensemble de lignes d'origine, supprimant toutes les options de filtre précédentes.</span><span class="sxs-lookup"><span data-stu-id="1973d-p101">Optional. A **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset. **False** indicates that you filter on the original rowset, removing any previous filter options.</span></span>

## <a name="remarks"></a><span data-ttu-id="1973d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1973d-114">Remarks</span></span>

<span data-ttu-id="1973d-p102">Les propriétés [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) et [FilterColumn](filtercolumn-property-rds.md) fournissent des fonctionnalités de tri et de filtrage pour le cache côté client. La fonctionnalité de tri classe les enregistrements en fonction des valeurs d'une seule colonne. La fonctionnalité de filtre affiche un sous-ensemble d'enregistrements en fonction de certains critères de recherche définis alors que l'objet [Recordset](recordset-object-ado.md) complet est conservé dans le cache. La méthode **Reset** exécute les critères et remplace l'objet **Recordset** actif par un objet **Recordset** qui peut être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="1973d-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on a find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="1973d-p103">Si des modifications apportées aux données d'origine n'ont pas encore été soumises, la méthode **Reset** échoue. Avant tout, utilisez la méthode [SubmitChanges](submitchanges-method-rds.md) pour enregistrer les éventuelles modifications dans un objet **Recordset** en lecture/écriture puis employez la méthode **Reset** pour trier ou filtrer les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="1973d-p103">If there are changes to the original data that haven't yet been submitted, the **Reset** method will fail. First, use the [SubmitChanges](submitchanges-method-rds.md) method to save any changes in a read/write **Recordset**, and then use the **Reset** method to sort or filter the records.</span></span>

<span data-ttu-id="1973d-121">Si vous souhaitez effectuer plusieurs filtres sur votre ensemble de lignes, vous pouvez utiliser l’option argument *Boolean* avec la méthode **Reset** .</span><span class="sxs-lookup"><span data-stu-id="1973d-121">If you want to perform more than one filter on your rowset, you can use the optional *Boolean* argument with the **Reset** method.</span></span> <span data-ttu-id="1973d-122">L'exemple suivant montre comment procéder :</span><span class="sxs-lookup"><span data-stu-id="1973d-122">The following example shows how to do this:</span></span>

