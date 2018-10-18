---
title: Index.CreateField Method (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c4c8c4d897e58655aa986ba2a0c28b7eece235a7
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605897"
---
# <a name="indexcreatefield-method-dao"></a><span data-ttu-id="89887-102">Index.CreateField Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="89887-102">Index.CreateField Method (DAO)</span></span>


<span data-ttu-id="89887-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="89887-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="89887-104">Crée un objet **[Field](field-object-dao.md)** (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="89887-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="89887-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89887-105">Syntax</span></span>

<span data-ttu-id="89887-106">*expression* . CreateField (***nom***, ***Type***, ***taille***)</span><span class="sxs-lookup"><span data-stu-id="89887-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="89887-107">*expression* Variable qui représente un objet **Index** .</span><span class="sxs-lookup"><span data-stu-id="89887-107">*expression* A variable that represents an **Index** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="89887-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89887-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89887-109">Name</span><span class="sxs-lookup"><span data-stu-id="89887-109">Name</span></span></p></th>
<th><p><span data-ttu-id="89887-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="89887-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="89887-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="89887-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="89887-112">Description</span><span class="sxs-lookup"><span data-stu-id="89887-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89887-113">Name</span><span class="sxs-lookup"><span data-stu-id="89887-113">Name</span></span></p></td>
<td><p><span data-ttu-id="89887-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="89887-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="89887-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="89887-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="89887-p101">Chaîne qui identifie de manière unique le nouvel objet <strong>Field</strong>. Reportez-vous à la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> pour plus d'informations sur les noms valides pour l'objet <strong>Field</strong>.  </span><span class="sxs-lookup"><span data-stu-id="89887-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89887-118">Type</span><span class="sxs-lookup"><span data-stu-id="89887-118">Type</span></span></p></td>
<td><p><span data-ttu-id="89887-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="89887-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="89887-120"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="89887-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="89887-121">Argument non pris en charge pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="89887-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89887-122">Size</span><span class="sxs-lookup"><span data-stu-id="89887-122">Size</span></span></p></td>
<td><p><span data-ttu-id="89887-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="89887-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="89887-124"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="89887-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="89887-125">Argument non pris en charge pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="89887-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89887-126"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="89887-126"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="89887-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="89887-127">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="89887-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="89887-128">Return value</span></span>
>>>>>>> <span data-ttu-id="89887-129">master</span><span class="sxs-lookup"><span data-stu-id="89887-129">master</span></span>

<span data-ttu-id="89887-130">Champ</span><span class="sxs-lookup"><span data-stu-id="89887-130">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="89887-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="89887-131">Remarks</span></span>

<span data-ttu-id="89887-p102">Vous pouvez utiliser la méthode **CreateField** pour créer un champ, spécifier le nom, le type de données et la taille du champ. Si vous omettez une ou plusieurs des parties facultatives lorsque vous utilisez la méthode **CreateField**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou réinitialiser la propriété correspondante avant d'ajouter le nouvel objet à la collection. Une fois que vous avez ajouté le nouvel objet, vous pouvez modifier une partie de ses paramètres de propriété, mais pas tous. Pour plus d'informations, reportez-vous aux rubriques concernant cette propriété.</span><span class="sxs-lookup"><span data-stu-id="89887-p102">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="89887-136">Les arguments de type et la taille s’appliquent uniquement aux objets **Field** dans un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="89887-136">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="89887-137">Ces arguments sont ignorés lorsqu'un objet **Field** est associé à un objet **Index** ou **Relation**.</span><span class="sxs-lookup"><span data-stu-id="89887-137">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="89887-138">Si le nom fait référence à un objet qui est déjà membre de la collection, une erreur d’exécution se produit lorsque vous utilisez la méthode **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="89887-138">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="89887-p104">Pour supprimer un objet **Field** d'une collection **Fields**, utilisez la méthode **[Delete](fields-delete-method-dao.md)** dans la collection. Vous ne pouvez pas supprimer un objet **Field** dans la collection **Fields** d'un objet **TableDef** une fois que vous avez créé un index qui renvoie à ce champ.</span><span class="sxs-lookup"><span data-stu-id="89887-p104">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

