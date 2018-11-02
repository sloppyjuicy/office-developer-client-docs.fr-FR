---
title: Propriété Relation.ForeignTable (DAO)
TOCTitle: ForeignTable Property
ms:assetid: 3f896433-2962-1c7c-f5a2-4e030ba8d4a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192853(v=office.15)
ms:contentKeyID: 48544401
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052989
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dcd454bc1c570e119cc8948acb8077a54649db84
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921711"
---
# <a name="relationforeigntable-property-dao"></a><span data-ttu-id="b0bc0-102">Propriété Relation.ForeignTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="b0bc0-102">Relation.ForeignTable property (DAO)</span></span>


<span data-ttu-id="b0bc0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0bc0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0bc0-p101">Définit ou renvoie le nom de la table étrangère d'une relation (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="b0bc0-p101">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="b0bc0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0bc0-106">Syntax</span></span>

<span data-ttu-id="b0bc0-107">*expression* . ForeignTable</span><span class="sxs-lookup"><span data-stu-id="b0bc0-107">*expression* .ForeignTable</span></span>

<span data-ttu-id="b0bc0-108">*expression* Variable qui représente un objet **Relation** .</span><span class="sxs-lookup"><span data-stu-id="b0bc0-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0bc0-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="b0bc0-109">Remarks</span></span>

<span data-ttu-id="b0bc0-110">Cette propriété est en lecture/écriture pour un nouvel objet **[Relation](relation-object-dao.md)** pas encore ajouté à une collection et en lecture seule pour un objet **Relation** existant de la collection **[Relations](relations-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="b0bc0-110">This property is read/write for a new **[Relation](relation-object-dao.md)** object not yet appended to a collection and read-only for an existing **Relation** object in the **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="b0bc0-111">Le paramètre de propriété **ForeignTable** d'un objet **Relation** est le paramètre de propriété **[Name](connection-name-property-dao.md)** de l'objet **[TableDef](tabledef-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)** qui représente la table étrangère ou la requête ; le paramètre de propriété **[Table](relation-table-property-dao.md)** est le paramètre de propriété **Name** de l'objet **TableDef** ou **QueryDef** qui représente la table primaire ou la requête.</span><span class="sxs-lookup"><span data-stu-id="b0bc0-111">The **ForeignTable** property setting of a **Relation** object is the **[Name](connection-name-property-dao.md)** property setting of the **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object that represents the foreign table or query; the **[Table](relation-table-property-dao.md)** property setting is the **Name** property setting of the **TableDef** or **QueryDef** object that represents the primary table or query.</span></span>

<span data-ttu-id="b0bc0-p102">Par exemple, prenons une liste de numéros de pièce valides (dans un champ appelé PartNo) stockée dans une table ValidParts. Vous pourriez établir une relation avec une table OrderItem de sorte que si un numéro de pièce était entré dans la table OrderItem, il devrait déjà exister dans la table ValidParts. Si le numéro de pièce n'existait pas dans la table ValidParts et si vous n'aviez pas défini la propriété **[Attributes](field-attributes-property-dao.md)** de l'objet **Relation** sur **dbRelationDontEnforce**, une erreur capturable surviendrait.</span><span class="sxs-lookup"><span data-stu-id="b0bc0-p102">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="b0bc0-p103">Dans ce cas, la table ValidParts est la table primaire, la propriété **Table** de l'objet **Relation** est donc définie sur ValidParts et la propriété **ForeignTable** de l'objet **Relation** sur OrderItem. Les propriétés **Name** et **ForeignName** de l'objet **Field** de la collection **Fields** de l'objet **Relation** sont alors définies sur PartNo.</span><span class="sxs-lookup"><span data-stu-id="b0bc0-p103">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="b0bc0-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="b0bc0-116">Example</span></span>

<span data-ttu-id="b0bc0-117">Cet exemple montre comment les propriétés **Table**, **ForeignTable** et **ForeignName** définissent les termes d'une **Relation** entre deux tables.</span><span class="sxs-lookup"><span data-stu-id="b0bc0-117">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
