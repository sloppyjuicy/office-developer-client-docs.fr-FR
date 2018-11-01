---
title: SortColumn, propriété (RDS)
TOCTitle: SortColumn Property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a613ed053bd91685286066bfa534c41b99edbdd1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874754"
---
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="3222a-102">SortColumn, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="3222a-102">SortColumn Property (RDS)</span></span>


<span data-ttu-id="3222a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3222a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3222a-104">Indique la colonne selon laquelle les enregistrements sont triés.</span><span class="sxs-lookup"><span data-stu-id="3222a-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="3222a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3222a-105">Syntax</span></span>

<span data-ttu-id="3222a-106">*DataControl*. SortColumn = *chaîne*</span><span class="sxs-lookup"><span data-stu-id="3222a-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="3222a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3222a-107">Parameters</span></span>

  - <span data-ttu-id="3222a-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3222a-108">*DataControl*</span></span>

  - <span data-ttu-id="3222a-109">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3222a-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="3222a-110">*String*</span><span class="sxs-lookup"><span data-stu-id="3222a-110">*String*</span></span>

  - <span data-ttu-id="3222a-111">Une valeur **String** qui représente le nom ou l'alias de la colonne selon laquelle les enregistrements sont triés.</span><span class="sxs-lookup"><span data-stu-id="3222a-111">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>

## <a name="remarks"></a><span data-ttu-id="3222a-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="3222a-112">Remarks</span></span>

<span data-ttu-id="3222a-p101">Les propriétés **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) et [FilterColumn](filtercolumn-property-rds.md) fournissent les fonctionnalités de tri et filtrage sur le cache côté client. La fonctionnalité de tri organise les enregistrements par valeur dans une colonne. La fonctionnalité de filtrage affiche un sous-ensemble d'enregistrements basés sur des critères de recherche tandis que le [Recordset](recordset-object-ado.md) complet est conservé dans le cache. La méthode [Reset](reset-method-rds.md) exécute les critères et remplace le **Recordset** actuel par un **Recordset** actualisable.</span><span class="sxs-lookup"><span data-stu-id="3222a-p101">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="3222a-117">Pour trier un **Recordset**, vous devez tout d'abord enregistrer toutes les modifications effectuées.</span><span class="sxs-lookup"><span data-stu-id="3222a-117">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="3222a-118">Si vous utilisez le **RDS.DataControl**, vous pouvez utiliser la méthode [SubmitChanges](submitchanges-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3222a-118">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="3222a-119">Par exemple, si votre **RDS. DataControl** est nommé ADC1, votre code sera ADC1. SubmitChanges.</span><span class="sxs-lookup"><span data-stu-id="3222a-119">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="3222a-120">Si vous utilisez un **Recordset** ADO, vous pouvez utiliser sa méthode [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3222a-120">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="3222a-121">La méthode recommandée pour les objets **Recordset** créés avec la méthode **CreateRecordset** est [UpdateBatch](createrecordset-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3222a-121">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="3222a-122">Par exemple, votre code peut être myRS.UpdateBatch ou.</span><span class="sxs-lookup"><span data-stu-id="3222a-122">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="3222a-123">Si vous utilisez un **Recordset** ADO, vous pouvez utiliser sa méthode [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3222a-123">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="3222a-124">La méthode recommandée pour les objets **Recordset** créés avec la méthode **CreateRecordset** est [UpdateBatch](createrecordset-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3222a-124">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="3222a-125">Par exemple, votre code peut être myRS.UpdateBatch ou ADC1. Recordset.UpdateBatch.</span><span class="sxs-lookup"><span data-stu-id="3222a-125">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>

