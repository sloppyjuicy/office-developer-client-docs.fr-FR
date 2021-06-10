---
title: Field2.CreateProperty method (DAO)
TOCTitle: CreateProperty Method
ms:assetid: bdbd6bec-216f-138e-78df-9c3221692aa4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822737(v=office.15)
ms:contentKeyID: 48547446
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf35138a4782e1f16d230ba120bf5482a9a8ce40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292845"
---
# <a name="field2createproperty-method-dao"></a><span data-ttu-id="7d5c6-102">Field2.CreateProperty method (DAO)</span><span class="sxs-lookup"><span data-stu-id="7d5c6-102">Field2.CreateProperty method (DAO)</span></span>

<span data-ttu-id="7d5c6-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d5c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d5c6-104">Crée un objet utilisateur **[Property](property-object-dao.md)** (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7d5c6-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d5c6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d5c6-105">Syntax</span></span>

<span data-ttu-id="7d5c6-106">*.* CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="7d5c6-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="7d5c6-107">*expression* une variable qui représente une **champ2** objet.</span><span class="sxs-lookup"><span data-stu-id="7d5c6-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d5c6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d5c6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d5c6-109">Nom</span><span class="sxs-lookup"><span data-stu-id="7d5c6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7d5c6-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="7d5c6-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7d5c6-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="7d5c6-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7d5c6-112">Description</span><span class="sxs-lookup"><span data-stu-id="7d5c6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d5c6-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="7d5c6-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="7d5c6-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7d5c6-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="7d5c6-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7d5c6-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7d5c6-p101">Valeur de type <strong>String</strong> qui nomme de façon unique le nouvel objet <strong>Property</strong>. Voir la propriété <strong>Name</strong> pour plus d'informations sur les noms <strong>Property</strong> valides.</span><span class="sxs-lookup"><span data-stu-id="7d5c6-p101">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d5c6-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="7d5c6-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="7d5c6-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7d5c6-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="7d5c6-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7d5c6-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7d5c6-p102">Constante qui définit le type de données du nouvel objet <strong>Property</strong>. Pour connaître les types de données valides, reportez-vous à la propriété <strong><a href="field-type-property-dao.md">Type</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="7d5c6-p102">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d5c6-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="7d5c6-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="7d5c6-124">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7d5c6-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="7d5c6-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7d5c6-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7d5c6-p103"><strong>Variant</strong> contenant la valeur initiale de la propriété. Pour plus d’informations, reportez-vous à la méthode <strong><a href="field-value-property-dao.md">Value</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="7d5c6-p103">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d5c6-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="7d5c6-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="7d5c6-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7d5c6-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="7d5c6-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7d5c6-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7d5c6-p104">Valeur de type <strong>Variant</strong> (sous-type <strong>Boolean</strong>) indiquant si l'objet <strong>Property</strong> est ou non un objet DDL. La valeur par défaut est <strong>False</strong>. Si DDL a la valeur <strong>True</strong>, les utilisateurs ne peuvent pas modifier ou supprimer cet objet <strong>Property</strong> sauf s'ils détiennent une autorisation <strong>dbSecWriteDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="7d5c6-p104">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object. The default is <strong>False</strong>. If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="7d5c6-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7d5c6-134">Return value</span></span>

<span data-ttu-id="7d5c6-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="7d5c6-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="7d5c6-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="7d5c6-136">Remarks</span></span>

<span data-ttu-id="7d5c6-137">Vous pouvez créer un objet utilisateur **Property** uniquement dans la collection **[Properties](properties-collection-dao.md)** d'un objet qui est persistant.</span><span class="sxs-lookup"><span data-stu-id="7d5c6-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="7d5c6-p105">Si vous omettez une ou plusieurs parties facultatives lorsque vous utilisez **CreateProperty**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou réinitialiser la propriété correspondante avant d'ajouter le nouvel objet à une collection. Une fois que vous ajoutez l'objet, vous pouvez modifier certains de ses paramètres de propriété mais pas tous. Pour plus d'informations, reportez-vous aux rubriques des propriétés **Name**, **Type** et **Value**.</span><span class="sxs-lookup"><span data-stu-id="7d5c6-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="7d5c6-141">Si le nom fait référence à un objet qui est déjà membre de la collection, une erreur d’utilisation se produit lorsque vous utilisez **[la méthode Append.](fields-append-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="7d5c6-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="7d5c6-p106">Pour supprimer un objet utilisateur **Property** de la collection, utilisez la méthode **[Delete](fields-delete-method-dao.md)** de la collection **[Properties](properties-collection-dao.md)**. Vous ne pouvez pas supprimer de propriétés intégrées.</span><span class="sxs-lookup"><span data-stu-id="7d5c6-p106">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **[Properties](properties-collection-dao.md)** collection. You can't delete built-in properties.</span></span>


> [!NOTE]
> <span data-ttu-id="7d5c6-144">Si vous omettez l’argument DDL, sa valeur par défaut est False (non DDL).</span><span class="sxs-lookup"><span data-stu-id="7d5c6-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="7d5c6-145">Dans la mesure où la propriété DDL correspondante est exposée, vous devez supprimer et recréer l'objet **Property** pour passer de DDL à non DDL.</span><span class="sxs-lookup"><span data-stu-id="7d5c6-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


