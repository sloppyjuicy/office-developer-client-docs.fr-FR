---
title: Field.CreateProperty Method (DAO)
TOCTitle: CreateProperty Method
ms:assetid: b3c1d303-7cab-89c3-8e90-f18a0445d304
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822050(v=office.15)
ms:contentKeyID: 48547202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a5b911e9e02380e9ea6aa85100e2a60b3b086a49
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602999"
---
# <a name="fieldcreateproperty-method-dao"></a><span data-ttu-id="37ced-102">Field.CreateProperty Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="37ced-102">Field.CreateProperty Method (DAO)</span></span>


<span data-ttu-id="37ced-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="37ced-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="37ced-104">Crée un objet utilisateur **[Property](property-object-dao.md)** (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="37ced-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="37ced-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37ced-105">Syntax</span></span>

<span data-ttu-id="37ced-106">*expression* . CreateProperty (***nom***, ***Type***, ***valeur***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="37ced-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="37ced-107">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="37ced-107">*expression* A variable that represents a **Field** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="37ced-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37ced-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37ced-109">Name</span><span class="sxs-lookup"><span data-stu-id="37ced-109">Name</span></span></p></th>
<th><p><span data-ttu-id="37ced-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="37ced-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="37ced-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="37ced-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="37ced-112">Description</span><span class="sxs-lookup"><span data-stu-id="37ced-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37ced-113">Name</span><span class="sxs-lookup"><span data-stu-id="37ced-113">Name</span></span></p></td>
<td><p><span data-ttu-id="37ced-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="37ced-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="37ced-115"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="37ced-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="37ced-p101">Type <strong>String</strong> qui identifie de façon unique le nouvel objet <strong>Property</strong>. Consultez la propriété <strong>Name</strong> pour plus d'informations sur les noms d'objets <strong>Property</strong> valides.</span><span class="sxs-lookup"><span data-stu-id="37ced-p101">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ced-118">Type</span><span class="sxs-lookup"><span data-stu-id="37ced-118">Type</span></span></p></td>
<td><p><span data-ttu-id="37ced-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="37ced-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="37ced-120"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="37ced-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="37ced-p102">Constante qui définit le type de données du nouvel objet <strong>Property</strong>. Pour plus d’informations sur les types de données valides, consultez la propriété <strong><a href="field-type-property-dao.md">Type</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="37ced-p102">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37ced-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="37ced-123">Value</span></span></p></td>
<td><p><span data-ttu-id="37ced-124">Facultatif</span><span class="sxs-lookup"><span data-stu-id="37ced-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="37ced-125"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="37ced-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="37ced-p103"><strong>Variant</strong> contenant la valeur de propriété initiale. Pour plus d’informations, consultez la propriété <strong><a href="field-value-property-dao.md">Value</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="37ced-p103">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37ced-128">DDL</span><span class="sxs-lookup"><span data-stu-id="37ced-128">DDL</span></span></p></td>
<td><p><span data-ttu-id="37ced-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="37ced-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="37ced-130"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="37ced-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="37ced-131"><strong>Variant</strong> (sous-type<strong>Boolean</strong> ) qui indique si la <strong>propriété</strong> est un objet DDL.</span><span class="sxs-lookup"><span data-stu-id="37ced-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="37ced-132">La valeur par défaut est <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="37ced-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="37ced-133">Est <strong>True</strong>, les utilisateurs ne peuvent pas modifier ou supprimer cet objet <strong>Property</strong> sauf si la <strong>valeur par défaut</strong> .</span><span class="sxs-lookup"><span data-stu-id="37ced-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37ced-134"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="37ced-134"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="37ced-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="37ced-135">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="37ced-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="37ced-136">Return value</span></span>
>>>>>>> <span data-ttu-id="37ced-137">master</span><span class="sxs-lookup"><span data-stu-id="37ced-137">master</span></span>

<span data-ttu-id="37ced-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="37ced-138">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="37ced-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="37ced-139">Remarks</span></span>

<span data-ttu-id="37ced-140">Vous pouvez créer un objet utilisateur **Property** uniquement dans la collection **[Properties](properties-collection-dao.md)** d'un objet qui est persistant.</span><span class="sxs-lookup"><span data-stu-id="37ced-140">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="37ced-p105">Si vous omettez une ou plusieurs parties facultatives lors de l'utilisation de **CreateProperty**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou réinitialiser la propriété correspondante avant d'ajouter le nouvel objet à une collection. Une fois l'objet ajouté, vous pouvez modifier certains paramètres de la propriété mais pas tous. Voir les rubriques traitant des propriétés **Name**, **Type** et **Value** pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="37ced-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="37ced-144">Si le nom fait référence à un objet qui est déjà membre de la collection, une erreur d’exécution se produit lorsque vous utilisez la méthode **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="37ced-144">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="37ced-p106">Pour supprimer un objet utilisateur **Property** de la collection, utilisez la méthode **[Delete](fields-delete-method-dao.md)** de la collection **Properties**. Vous ne pouvez pas supprimer de propriétés intégrées.</span><span class="sxs-lookup"><span data-stu-id="37ced-p106">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection. You can't delete built-in properties.</span></span>


> [!NOTE]
> <P><span data-ttu-id="37ced-147">Si vous omettez l’argument DDL, la valeur par défaut est False (non DDL).</span><span class="sxs-lookup"><span data-stu-id="37ced-147">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="37ced-148">Aucune propriété DDL correspondante n'étant exposée, vous devez supprimer et recréer un objet <STRONG>Property</STRONG> pour en faire un objet non DDL.</span><span class="sxs-lookup"><span data-stu-id="37ced-148">Because no corresponding DDL property is exposed, you must delete and re-create a <STRONG>Property</STRONG> object you want to change from DDL to non-DDL.</span></span></P>


