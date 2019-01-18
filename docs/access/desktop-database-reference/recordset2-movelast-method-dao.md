---
title: Méthode Recordset2.MoveLast (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 829c4dd759bce86388cc65aa5b63276eec438ea0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713757"
---
# <a name="recordset2movelast-method-dao"></a><span data-ttu-id="7d9b5-102">Méthode Recordset2.MoveLast (DAO)</span><span class="sxs-lookup"><span data-stu-id="7d9b5-102">Recordset2.MoveLast method (DAO)</span></span>

<span data-ttu-id="7d9b5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d9b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d9b5-104">Atteint le dernier enregistrement d'un objet **Recordset** spécifié et en fait l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d9b5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d9b5-105">Syntax</span></span>

<span data-ttu-id="7d9b5-106">*expression* . MoveLast (***Options***)</span><span class="sxs-lookup"><span data-stu-id="7d9b5-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="7d9b5-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="7d9b5-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d9b5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d9b5-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d9b5-109">Nom</span><span class="sxs-lookup"><span data-stu-id="7d9b5-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7d9b5-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="7d9b5-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7d9b5-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="7d9b5-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7d9b5-112">Description</span><span class="sxs-lookup"><span data-stu-id="7d9b5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d9b5-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="7d9b5-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="7d9b5-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7d9b5-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="7d9b5-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="7d9b5-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="7d9b5-116">Associez ce paramètre à la constante <strong>dbRunAsync</strong> pour obtenir une exécution asynchrone de l'appel de <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="7d9b5-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7d9b5-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="7d9b5-117">Remarks</span></span>

<span data-ttu-id="7d9b5-118">Utilisez les méthodes **Move** pour vous déplacer entre les enregistrements sans appliquer de condition.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="7d9b5-p101">Si vous modifiez l'enregistrement actif, veillez à utiliser la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous accédez à un autre enregistrement alors que vous effectuez une mise à jour, les modifications seront perdues sans notification.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="7d9b5-p102">Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** a la valeur **False**. Si l'objet **Recordset** ne contient pas d'enregistrements, la propriété **BOF** a la valeur **True** et aucun enregistrement n'est actif.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="7d9b5-123">Si le premier ou le dernier enregistrement est déjà actif lorsque vous utilisez la méthode **MoveFirst** ou **MoveLast**, l'enregistrement actif ne change pas.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="7d9b5-124">Si le jeu d’enregistrements fait référence à un **objet Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="7d9b5-125">Vous pouvez définir l'index actif à l'aide de la propriété **Index**.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="7d9b5-126">Si vous ne définissez pas l'index actuel, l'ordre des enregistrements renvoyés est indéfini.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-126">If you don't set the current index, the order of returned records is undefined.</span></span>

> [!NOTE]
> <span data-ttu-id="7d9b5-127">[!REMARQUE] Vous pouvez utiliser la méthode **MoveLast** pour remplir entièrement un objet **Recordset** de type feuille de réponse dynamique ou instantané en vue de fournir le nombre actuel d'enregistrements présents dans l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-127">You can use the **MoveLast** method to fully populate a dynaset- or snapshot-type **Recordset** to provide the current number of records in the **Recordset**.</span></span> <span data-ttu-id="7d9b5-128">Toutefois, si vous utilisez **MoveLast** de cette manière, vous risquez de ralentir l'exécution de votre application.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-128">However, if you use **MoveLast** in this way, you can slow down your application's performance.</span></span> <span data-ttu-id="7d9b5-129">Il n'est conseillé d'utiliser la méthode **MoveLast** qu'en cas de nécessité absolue d'obtenir un décompte précis des enregistrements présents dans un objet **Recordset** récemment ouvert.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-129">You should only use **MoveLast** to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened **Recordset**.</span></span> 
>
> <span data-ttu-id="7d9b5-130">Si vous utilisez la constante **dbRunAsync** avec **MoveLast**, l'appel de la méthode est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-130">If you use the **dbRunAsync** constant with **MoveLast**, the method call is asynchronous.</span></span> <span data-ttu-id="7d9b5-131">Vous pouvez utiliser la propriété **StillExecuting** pour déterminer à quel moment l'enregistrement **Recordset** est rempli entièrement, de même que vous pouvez utiliser la méthode **Cancel** pour terminer l'exécution de l'appel asynchrone de la méthode **MoveLast**.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-131">You can use the **StillExecuting** property to determine when the **Recordset** is fully populated, and you can use the **Cancel** method to terminate execution of the asynchronous **MoveLast** method call.</span></span>

<span data-ttu-id="7d9b5-132">Vous ne pouvez pas utiliser les méthodes **MoveFirst**, **MoveLast**et **MovePrevious** sur un objet **Recordset** de type avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="7d9b5-133">Pour déplacer la position de l'enregistrement actif dans un objet **Recordset** d'un objet d'un nombre d'enregistrements spécifique vers l'avant ou l'arrière, utilisez la méthode **Move**.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

