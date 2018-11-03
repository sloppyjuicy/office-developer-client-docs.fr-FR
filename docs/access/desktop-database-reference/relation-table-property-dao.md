---
title: Propriété Relation.Table (DAO)
TOCTitle: Table Property
ms:assetid: cc4f64ef-c4e9-1a14-9263-5f8220d89840
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834423(v=office.15)
ms:contentKeyID: 48547736
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053068
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dd6f1ef3ea1d955f3b17d4cafb7e521c54191d27
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929579"
---
# <a name="relationtable-property-dao"></a><span data-ttu-id="7c4c8-102">Propriété Relation.Table (DAO)</span><span class="sxs-lookup"><span data-stu-id="7c4c8-102">Relation.Table property (DAO)</span></span>


<span data-ttu-id="7c4c8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c4c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c4c8-p101">Indique le nom d'une table primaire d'un objet **[Relation](relation-object-dao.md)**. Ce nom doit correspondre à la valeur de la propriété **[Name](connection-name-property-dao.md)** d'un objet **[TableDef](tabledef-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)** (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7c4c8-p101">Indicates the name of a **[Relation](relation-object-dao.md)** object's primary table. This should be equal to the **[Name](connection-name-property-dao.md)** property setting of a **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7c4c8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c4c8-106">Syntax</span></span>

<span data-ttu-id="7c4c8-107">*expression* . Tableau</span><span class="sxs-lookup"><span data-stu-id="7c4c8-107">*expression* .Table</span></span>

<span data-ttu-id="7c4c8-108">*expression* Variable qui représente un objet **Relation** .</span><span class="sxs-lookup"><span data-stu-id="7c4c8-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c4c8-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="7c4c8-109">Remarks</span></span>

<span data-ttu-id="7c4c8-110">La propriété **Table** est en lecture/écriture pour tout nouvel objet **Relation** non encore ajouté à une collection et en lecture seule pour tout objet **Relation** existant dans une collection **[Relations](relations-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="7c4c8-110">The **Table** property setting is read/write for a new **Relation** object not yet appended to a collection and read-only for an existing **Relation** object in a **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="7c4c8-p102">Utilisez la propriété **Table** avec la propriété **[ForeignTable](relation-foreigntable-property-dao.md)** pour définir un objet **Relation**, qui représente la relation entre des champs dans deux tables ou requêtes. Donnez à la propriété **Table** la valeur de la propriété **Name** de l'objet primaire **TableDef** ou **QueryDef**, et attribuez à la propriété **ForeignTable** la valeur de la propriété **Name** de l'objet étranger (de référence) **TableDef** ou **QueryDef**. La propriété **[Attributes](field-attributes-property-dao.md)** détermine le type de relation entre les deux objets.</span><span class="sxs-lookup"><span data-stu-id="7c4c8-p102">Use the **Table** property with the **[ForeignTable](relation-foreigntable-property-dao.md)** property to define a **Relation** object, which represents the relationship between fields in two tables or queries. Set the **Table** property to the **Name** property setting of the primary **TableDef** or **QueryDef** object, and set the **ForeignTable** property to the **Name** property setting of the foreign (referencing) **TableDef** or **QueryDef** object. The **[Attributes](field-attributes-property-dao.md)** property determines the type of relationship between the two objects.</span></span>

<span data-ttu-id="7c4c8-p103">Par exemple, si vous avez une liste de codes de pièces valide (dans un champ appelé PartNo) stockée dans une table ValidParts, vous pouvez établir une relation un-à-plusieurs avec une table OrderItem de telle façon que si un code de pièce est entré dans la table OrderItem, il doit déjà se trouver dans la table ValidParts. Si le code de pièce n'existe pas dans la table ValidParts et que vous n'avez pas défini la propriété **Attributes** de l'objet **Relation** avec la valeur **dbRelationDontEnforce**, une erreur interceptable se produit.</span><span class="sxs-lookup"><span data-stu-id="7c4c8-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a one-to-many relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **Attributes** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="7c4c8-p104">Dans ce cas, la table ValidParts est la table primaire, de sorte que la propriété **Table** de l'objet **Relation** sont définie sur ValidParts et la propriété **ForeignTable** de l'objet **Relation** sur OrderItem. Les propriétés **Name** et **ForeignName** de l'objet **[Field](field-object-dao.md)** dans la collection [**Fields**](fields-collection-dao.md) de l'objet **Relation** sont définies sur PartNo.</span><span class="sxs-lookup"><span data-stu-id="7c4c8-p104">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **[Field](field-object-dao.md)** object in the **Relation** object's **[Fields](fields-collection-dao.md)** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="7c4c8-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="7c4c8-118">Example</span></span>

<span data-ttu-id="7c4c8-119">Cet exemple montre comment les propriétés **Table**, **ForeignTable** et **ForeignName** définissent les termes d'une **Relation** entre deux tables.</span><span class="sxs-lookup"><span data-stu-id="7c4c8-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

```vb
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
