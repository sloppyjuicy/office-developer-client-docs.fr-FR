---
title: Recordset2.UpdateOptions Property (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04f47f7a4affd68a55ae72287fb102a1c0f6d8be
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877939"
---
# <a name="recordset2updateoptions-property-dao"></a><span data-ttu-id="8af3e-102">Recordset2.UpdateOptions Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="8af3e-102">Recordset2.UpdateOptions Property (DAO)</span></span>


<span data-ttu-id="8af3e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8af3e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="8af3e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8af3e-104">Syntax</span></span>

<span data-ttu-id="8af3e-105">*expression* . UpdateOptions (OptionsMAJ)</span><span class="sxs-lookup"><span data-stu-id="8af3e-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="8af3e-106">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="8af3e-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8af3e-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="8af3e-107">Remarks</span></span>

<span data-ttu-id="8af3e-108">Lorsqu'une méthode **[Update](recordset2-update-method-dao.md)** en mode de traitement par lot est exécutée, DAO et la bibliothèque client de curseurs par lots créent une série d'instructions SQL UPDATE pour apporter les modifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="8af3e-108">When a batch-mode **[Update](recordset2-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="8af3e-109">Une clause SQL WHERE est créée pour chaque mise à jour afin d'isoler les enregistrements marqués comme étant modifiés par la propriété **[RecordStatus](recordset2-recordstatus-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8af3e-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset2-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="8af3e-110">Dans la mesure où certains serveurs distants utilisent des déclencheurs ou d'autres moyens pour appliquer l'intégrité référentielle, il est souvent essentiel de limiter les champs à mettre à jour aux seuls champs affectés par la modification.</span><span class="sxs-lookup"><span data-stu-id="8af3e-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="8af3e-111">Pour ce faire, affectez à la propriété **UpdateOptions** l'une des constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** ou **dbCriteriaTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="8af3e-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="8af3e-112">De cette façon, seule la partie minimale indispensable du code de déclencheur est exécutée.</span><span class="sxs-lookup"><span data-stu-id="8af3e-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="8af3e-113">Ainsi, l'opération de mise à jour est exécutée plus rapidement et est moins susceptible de contenir des erreurs.</span><span class="sxs-lookup"><span data-stu-id="8af3e-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="8af3e-p103">h **dbCriteriaDeleteInsert** **dbCriteriaUpdate** **UpdateOptions**</span><span class="sxs-lookup"><span data-stu-id="8af3e-p103">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server. In the former case, two separate operations are required to update the record. In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="8af3e-117">Si vous ne spécifiez pas de constantes, **dbCriteriaUpdate** et **dbCriteriaKey** seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="8af3e-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="8af3e-118">Dans la mesure où les enregistrements récemment ajoutés génèrent toujours des instructions INSERT et les enregistrements supprimés toujours des instructions DELETE, cette propriété ne concerne que la façon dont la bibliothèque de curseurs met à jour les enregistrements modifiés.</span><span class="sxs-lookup"><span data-stu-id="8af3e-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

