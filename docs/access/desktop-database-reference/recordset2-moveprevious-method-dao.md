---
title: Recordset2.MovePrevious, méthode (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 8c433810-4b19-e7c1-3cee-a0bc50b23e8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197336(v=office.15)
ms:contentKeyID: 48546235
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9753d3bbb586e2c1bd44755deb529758d8eab060
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307244"
---
# <a name="recordset2moveprevious-method-dao"></a><span data-ttu-id="14efe-102">Recordset2.MovePrevious, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="14efe-102">Recordset2.MovePrevious method (DAO)</span></span>


<span data-ttu-id="14efe-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14efe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14efe-104">Atteint l’enregistrement d’un objet **Recordset** précédent spécifié et en fait l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="14efe-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="14efe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14efe-105">Syntax</span></span>

<span data-ttu-id="14efe-106">*.* MovePrevious</span><span class="sxs-lookup"><span data-stu-id="14efe-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="14efe-107">*expression* Variable qui représente un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="14efe-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="14efe-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="14efe-108">Remarks</span></span>

<span data-ttu-id="14efe-109">La méthode **Move** permet de passer d’un enregistrement à un autre sans appliquer de condition.</span><span class="sxs-lookup"><span data-stu-id="14efe-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="14efe-p101">Si vous modifiez l’enregistrement actif, utilisez la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous passez à un autre enregistrement sans procéder à la mise à jour, vos modifications seront perdues sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="14efe-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="14efe-p102">Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** a la valeur **False**. Si l’objet **Recordset** ne contient pas d’enregistrements, la propriété **BOF** a la valeur **True** et aucun enregistrement n’est actif.</span><span class="sxs-lookup"><span data-stu-id="14efe-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="14efe-p103">Si vous utilisez **MovePrevious** alors que le premier enregistrement est actif, la propriété **BOF** a la valeur **True**, et aucun enregistrement n'est actif. Si vous utilisez à nouveau **MovePrevious**, une erreur se produit et **BOF** conserve la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="14efe-p103">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record. If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="14efe-116">Si recordset fait référence à un objet **Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="14efe-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="14efe-117">Vous pouvez définir l'index actuel par le biais de la propriété **Index**.</span><span class="sxs-lookup"><span data-stu-id="14efe-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="14efe-118">Si vous ne définissez pas l’index actuel, l’ordre des enregistrements renvoyés est indéfini.</span><span class="sxs-lookup"><span data-stu-id="14efe-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="14efe-119">Vous ne pouvez pas appliquer les méthodes **MoveFirst**, **MoveLast** et **MovePrevious** à un objet **Recordset** de type avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="14efe-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="14efe-120">Pour faire avancer ou reculer l’enregistrement actif d’un certain nombre d’enregistrements dans un objet **Recordset**, utilisez la méthode **Move**.</span><span class="sxs-lookup"><span data-stu-id="14efe-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

