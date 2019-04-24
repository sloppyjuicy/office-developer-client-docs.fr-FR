---
title: QueryDef. CreateProperty, méthode (DAO)
TOCTitle: CreateProperty Method
ms:assetid: e107b7d0-5556-7b87-f131-95f518893e4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835663(v=office.15)
ms:contentKeyID: 48548250
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f33198ac13b6695bfa592e2015aaed84d57f3b2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303030"
---
# <a name="querydefcreateproperty-method-dao"></a><span data-ttu-id="83cbe-102">QueryDef. CreateProperty, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="83cbe-102">QueryDef.CreateProperty method (DAO)</span></span>

<span data-ttu-id="83cbe-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="83cbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83cbe-104">Crée un objet utilisateur **[Property](property-object-dao.md)** (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="83cbe-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="83cbe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83cbe-105">Syntax</span></span>

<span data-ttu-id="83cbe-106">*expression* . CreateProperty (***nom***, ***type***, ***valeur***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="83cbe-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="83cbe-107">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="83cbe-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="83cbe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83cbe-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="83cbe-109">Nom</span><span class="sxs-lookup"><span data-stu-id="83cbe-109">Name</span></span></p></th>
<th><p><span data-ttu-id="83cbe-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="83cbe-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="83cbe-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="83cbe-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="83cbe-112">Description</span><span class="sxs-lookup"><span data-stu-id="83cbe-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83cbe-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="83cbe-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="83cbe-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="83cbe-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="83cbe-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="83cbe-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="83cbe-116">Valeur de type <strong>String</strong> qui nomme de façon unique le nouvel objet <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="83cbe-116">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="83cbe-117">Voir la propriété <strong>Name</strong> pour plus d'informations sur les noms <strong>Property</strong> valides.</span><span class="sxs-lookup"><span data-stu-id="83cbe-117">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83cbe-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="83cbe-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="83cbe-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="83cbe-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="83cbe-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="83cbe-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="83cbe-121">Constante qui définit le type de données du nouvel objet <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="83cbe-121">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="83cbe-122">Pour connaître les types de données valides, reportez-vous à la propriété <strong><a href="field-type-property-dao.md">Type</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="83cbe-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83cbe-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="83cbe-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="83cbe-124">Facultatif</span><span class="sxs-lookup"><span data-stu-id="83cbe-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="83cbe-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="83cbe-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="83cbe-126"><strong>Variant</strong> contenant la valeur initiale de la propriété.</span><span class="sxs-lookup"><span data-stu-id="83cbe-126">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="83cbe-127">Pour plus d'informations, voir la propriété <strong><a href="field-value-property-dao.md">value</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="83cbe-127">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83cbe-128"><em>Definition</em></span><span class="sxs-lookup"><span data-stu-id="83cbe-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="83cbe-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="83cbe-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="83cbe-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="83cbe-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="83cbe-131">Valeur de type <strong>Variant</strong> (sous-type <strong>Boolean</strong>) indiquant si l'objet <strong>Property</strong> est ou non un objet DDL.</span><span class="sxs-lookup"><span data-stu-id="83cbe-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="83cbe-132">La valeur par défaut est <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="83cbe-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="83cbe-133">Si DDL a la valeur <strong>True</strong>, les utilisateurs ne peuvent pas modifier ou supprimer cet objet <strong>Property</strong> sauf s'ils détiennent une autorisation <strong>dbSecWriteDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="83cbe-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="83cbe-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="83cbe-134">Return value</span></span>

<span data-ttu-id="83cbe-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="83cbe-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="83cbe-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="83cbe-136">Remarks</span></span>

<span data-ttu-id="83cbe-137">Vous pouvez créer un objet utilisateur **Property** uniquement dans la collection **[Properties](properties-collection-dao.md)** d'un objet qui est persistant.</span><span class="sxs-lookup"><span data-stu-id="83cbe-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="83cbe-p105">Si vous omettez une ou plusieurs parties facultatives lorsque vous utilisez **CreateProperty**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou réinitialiser la propriété correspondante avant d'ajouter le nouvel objet à une collection. Une fois que vous ajoutez l'objet, vous pouvez modifier certains de ses paramètres de propriété mais pas tous. Pour plus d'informations, reportez-vous aux rubriques des propriétés **Name**, **Type** et **Value**.</span><span class="sxs-lookup"><span data-stu-id="83cbe-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="83cbe-141">Si name fait référence à un objet qui est déjà membre de la collection, une erreur d'exécution se produit lorsque vous utilisez la méthode **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="83cbe-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="83cbe-142">Pour supprimer un objet utilisateur **Property** de la collection, utilisez la méthode **[Delete](fields-delete-method-dao.md)** de la collection **[Properties](properties-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="83cbe-142">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **[Properties](properties-collection-dao.md)** collection.</span></span> <span data-ttu-id="83cbe-143">Vous ne pouvez pas supprimer de propriétés intégrées.</span><span class="sxs-lookup"><span data-stu-id="83cbe-143">You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="83cbe-144">Si vous omettez l'argument DDL, sa valeur par défaut est false (non DDL).</span><span class="sxs-lookup"><span data-stu-id="83cbe-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="83cbe-145">Étant donné qu'aucune propriété DDL correspondante n'est exposée, vous devez supprimer et recréer un objet **Property** dont vous souhaitez modifier la DDL en non DDL.</span><span class="sxs-lookup"><span data-stu-id="83cbe-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object that you want to change from DDL to non-DDL.</span></span>


