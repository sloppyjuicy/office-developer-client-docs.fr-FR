---
title: Recordset2.MovePrevious Method (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 8c433810-4b19-e7c1-3cee-a0bc50b23e8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197336(v=office.15)
ms:contentKeyID: 48546235
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d437fe3bb271cc50c187b185bcd3078b523a73a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469306"
---
# <a name="recordset2moveprevious-method-dao"></a><span data-ttu-id="2a38e-102">Recordset2.MovePrevious Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="2a38e-102">Recordset2.MovePrevious Method (DAO)</span></span>


<span data-ttu-id="2a38e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a38e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2a38e-104">Atteint l'enregistrement précédent d'un objet **Recordset** spécifié et en fait l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="2a38e-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a38e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a38e-105">Syntax</span></span>

<span data-ttu-id="2a38e-106">*expression* . MovePrevious</span><span class="sxs-lookup"><span data-stu-id="2a38e-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="2a38e-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="2a38e-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a38e-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a38e-108">Remarks</span></span>

<span data-ttu-id="2a38e-109">Utilisez les méthodes **Move** pour vous déplacer entre les enregistrements sans appliquer de condition.</span><span class="sxs-lookup"><span data-stu-id="2a38e-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="2a38e-p101">Si vous modifiez l'enregistrement actif, veillez à utiliser la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous accédez à un autre enregistrement alors que vous effectuez une mise à jour, les modifications seront perdues sans notification.</span><span class="sxs-lookup"><span data-stu-id="2a38e-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="2a38e-p102">Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** prend la valeur **False**. Si l'objet **Recordset** ne contient pas d'enregistrement, la propriété **BOF** prend la valeur **True**, et il n'y a pas d'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="2a38e-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="2a38e-p103">Si vous utilisez **MovePrevious** alors que le premier enregistrement est actif, la propriété **BOF** a la valeur **True**, et aucun enregistrement n'est actif. Si vous utilisez à nouveau **MovePrevious**, une erreur se produit et **BOF** conserve la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="2a38e-p103">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record. If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="2a38e-116">Si le jeu d’enregistrements fait référence à un **objet Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="2a38e-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="2a38e-117">Vous pouvez définir l'index actif à l'aide de la propriété **Index**.</span><span class="sxs-lookup"><span data-stu-id="2a38e-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="2a38e-118">Si vous ne définissez pas l'index actif, l'ordre des enregistrements renvoyés est indéfini.</span><span class="sxs-lookup"><span data-stu-id="2a38e-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="2a38e-119">Vous ne pouvez pas utiliser les méthodes **MoveFirst**, **MoveLast**et **MovePrevious** sur un objet **Recordset** de type avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="2a38e-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="2a38e-120">Pour déplacer la position de l'enregistrement actif dans un objet **Recordset** d'un objet d'un nombre d'enregistrements spécifique vers l'avant ou l'arrière, utilisez la méthode **Move**.</span><span class="sxs-lookup"><span data-stu-id="2a38e-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

