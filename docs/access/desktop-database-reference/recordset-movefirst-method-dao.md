---
title: Méthode Recordset.MoveFirst (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 338f7e86-6997-b80a-fc7a-a395d10b4a62
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192329(v=office.15)
ms:contentKeyID: 48544109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3cf56a5ab5c84423933dfb9d3c77a11c41a9ebbb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873438"
---
# <a name="recordsetmovefirst-method-dao"></a><span data-ttu-id="cb3d0-102">Méthode Recordset.MoveFirst (DAO)</span><span class="sxs-lookup"><span data-stu-id="cb3d0-102">Recordset.MoveFirst Method (DAO)</span></span>


<span data-ttu-id="cb3d0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb3d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb3d0-104">Atteint le premier enregistrement d'un objet **Recordset** spécifié et en fait l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="cb3d0-104">Moves to the first record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb3d0-105">Syntax</span></span>

<span data-ttu-id="cb3d0-106">*expression* . MoveFirst</span><span class="sxs-lookup"><span data-stu-id="cb3d0-106">*expression* .MoveFirst</span></span>

<span data-ttu-id="cb3d0-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="cb3d0-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb3d0-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="cb3d0-108">Remarks</span></span>

<span data-ttu-id="cb3d0-109">Utilisez les méthodes **Move** pour vous déplacer entre les enregistrements sans appliquer de condition.</span><span class="sxs-lookup"><span data-stu-id="cb3d0-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="cb3d0-p101">Si vous modifiez l'enregistrement actif, veillez à utiliser la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous accédez à un autre enregistrement alors que vous effectuez une mise à jour, les modifications seront perdues sans notification.</span><span class="sxs-lookup"><span data-stu-id="cb3d0-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="cb3d0-p102">Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** a la valeur **False**. Si l'objet **Recordset** ne contient pas d'enregistrements, la propriété **BOF** a la valeur **True** et aucun enregistrement n'est actif.</span><span class="sxs-lookup"><span data-stu-id="cb3d0-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="cb3d0-114">Si le premier ou le dernier enregistrement est déjà actif lorsque vous utilisez la méthode **MoveFirst** ou **MoveLast**, l'enregistrement actif ne change pas.</span><span class="sxs-lookup"><span data-stu-id="cb3d0-114">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="cb3d0-115">Si le jeu d’enregistrements fait référence à un **objet Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="cb3d0-115">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="cb3d0-116">Vous pouvez définir l'index actif à l'aide de la propriété **Index**.</span><span class="sxs-lookup"><span data-stu-id="cb3d0-116">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="cb3d0-117">Si vous ne définissez pas l'index actif, l'ordre des enregistrements renvoyés est indéfini.</span><span class="sxs-lookup"><span data-stu-id="cb3d0-117">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="cb3d0-118">Vous ne pouvez pas utiliser les méthodes **MoveFirst**, **MoveLast**et **MovePrevious** sur un objet **Recordset** de type avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="cb3d0-118">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="cb3d0-119">Pour déplacer la position de l'enregistrement actif dans un objet **Recordset** d'un objet d'un nombre d'enregistrements spécifique vers l'avant ou l'arrière, utilisez la méthode **Move**.</span><span class="sxs-lookup"><span data-stu-id="cb3d0-119">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

