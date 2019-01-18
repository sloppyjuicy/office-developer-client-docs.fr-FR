---
title: Méthode Recordset.MoveLast (DAO)
TOCTitle: MoveLast method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 79799742499e163a43d51a2d8553adcadf27b36d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715269"
---
# <a name="recordsetmovelast-method-dao"></a><span data-ttu-id="2b7a6-102">Méthode Recordset.MoveLast (DAO)</span><span class="sxs-lookup"><span data-stu-id="2b7a6-102">Recordset.MoveLast method (DAO)</span></span>

<span data-ttu-id="2b7a6-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b7a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b7a6-104">Atteint le dernier enregistrement d'un objet **Recordset** spécifié et en fait l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b7a6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b7a6-105">Syntax</span></span>

<span data-ttu-id="2b7a6-106">*expression* . MoveLast (***Options***)</span><span class="sxs-lookup"><span data-stu-id="2b7a6-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="2b7a6-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2b7a6-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b7a6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b7a6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b7a6-109">Nom</span><span class="sxs-lookup"><span data-stu-id="2b7a6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2b7a6-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="2b7a6-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2b7a6-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="2b7a6-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="2b7a6-112">Description</span><span class="sxs-lookup"><span data-stu-id="2b7a6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b7a6-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="2b7a6-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="2b7a6-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2b7a6-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="2b7a6-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="2b7a6-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="2b7a6-116">Associez ce paramètre à la constante <strong>dbRunAsync</strong> pour obtenir une exécution asynchrone de l'appel de <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="2b7a6-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2b7a6-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="2b7a6-117">Remarks</span></span>

<span data-ttu-id="2b7a6-118">Utilisez les méthodes **Move** pour vous déplacer entre les enregistrements sans appliquer de condition.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="2b7a6-p101">Si vous modifiez l'enregistrement actif, veillez à utiliser la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous accédez à un autre enregistrement alors que vous effectuez une mise à jour, les modifications seront perdues sans notification.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="2b7a6-p102">Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** a la valeur **False**. Si l'objet **Recordset** ne contient pas d'enregistrements, la propriété **BOF** a la valeur **True** et aucun enregistrement n'est actif.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="2b7a6-123">Si le premier ou le dernier enregistrement est déjà actif lorsque vous utilisez la méthode **MoveFirst** ou **MoveLast**, l'enregistrement actif ne change pas.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="2b7a6-124">Si le jeu d’enregistrements fait référence à un **objet Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="2b7a6-125">Vous pouvez définir l'index actif à l'aide de la propriété **Index**.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="2b7a6-126">Si vous ne définissez pas l'index actuel, l'ordre des enregistrements renvoyés est indéfini.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-126">If you don't set the current index, the order of returned records is undefined.</span></span>

> [!NOTE]
> <span data-ttu-id="2b7a6-127">[!REMARQUE] Vous pouvez utiliser la méthode **MoveLast** pour remplir entièrement un objet **Recordset** de type feuille de réponse dynamique ou instantané en vue de fournir le nombre actuel d'enregistrements présents dans l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-127">You can use the **MoveLast** method to fully populate a dynaset- or snapshot-type **Recordset** to provide the current number of records in the **Recordset**.</span></span> <span data-ttu-id="2b7a6-128">Toutefois, si vous utilisez **MoveLast** de cette manière, vous risquez de ralentir l'exécution de votre application.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-128">However, if you use **MoveLast** in this way, you can slow down your application's performance.</span></span> <span data-ttu-id="2b7a6-129">Il n'est conseillé d'utiliser la méthode **MoveLast** qu'en cas de nécessité absolue d'obtenir un décompte précis des enregistrements présents dans un objet **Recordset** récemment ouvert.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-129">You should only use **MoveLast** to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened **Recordset**.</span></span> 
> 
> <span data-ttu-id="2b7a6-130">Si vous utilisez la constante **dbRunAsync** avec **MoveLast**, l'appel de la méthode est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-130">If you use the **dbRunAsync** constant with **MoveLast**, the method call is asynchronous.</span></span> <span data-ttu-id="2b7a6-131">Vous pouvez utiliser la propriété **StillExecuting** pour déterminer à quel moment l'enregistrement **Recordset** est rempli entièrement, de même que vous pouvez utiliser la méthode **Cancel** pour terminer l'exécution de l'appel asynchrone de la méthode **MoveLast**.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-131">You can use the **StillExecuting** property to determine when the **Recordset** is fully populated, and you can use the **Cancel** method to terminate execution of the asynchronous **MoveLast** method call.</span></span>

<span data-ttu-id="2b7a6-132">Vous ne pouvez pas utiliser les méthodes **MoveFirst**, **MoveLast**et **MovePrevious** sur un objet **Recordset** de type avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="2b7a6-133">Pour déplacer la position de l'enregistrement actif dans un objet **Recordset** d'un objet d'un nombre d'enregistrements spécifique vers l'avant ou l'arrière, utilisez la méthode **Move**.</span><span class="sxs-lookup"><span data-stu-id="2b7a6-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

