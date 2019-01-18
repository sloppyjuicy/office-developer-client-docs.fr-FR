---
title: Propriété Field.ForeignName (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7c340eee9972e8247654ec863ba0ef4588ef65f8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708465"
---
# <a name="fieldforeignname-property-dao"></a><span data-ttu-id="d9d95-102">Propriété Field.ForeignName (DAO)</span><span class="sxs-lookup"><span data-stu-id="d9d95-102">Field.ForeignName property (DAO)</span></span>


<span data-ttu-id="d9d95-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9d95-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d9d95-104">Définit ou renvoie une valeur qui spécifie le nom de l'objet **[Field](field-object-dao.md)** d'une table étrangère correspondant à un champ d'une table primaire d'une relation (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="d9d95-104">Sets or returns a value that specifies the name of the **[Field](field-object-dao.md)** object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d95-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9d95-105">Syntax</span></span>

<span data-ttu-id="d9d95-106">*expression* . ForeignName</span><span class="sxs-lookup"><span data-stu-id="d9d95-106">*expression* .ForeignName</span></span>

<span data-ttu-id="d9d95-107">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="d9d95-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d95-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9d95-108">Remarks</span></span>

<span data-ttu-id="d9d95-p101">Si l'objet **[Relation](relation-object-dao.md)** n'est pas ajouté à l'objet **[Database](database-object-dao.md)**, mais que l'objet **Field** est ajouté à l'objet **Relation**, la propriété **ForeignName** est en lecture/écriture. Une fois que l'objet **Relation** est ajouté à la base de données, la propriété **ForeignName** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d9d95-p101">If the **[Relation](relation-object-dao.md)** object isn't appended to the **[Database](database-object-dao.md)**, but the **Field** is appended to the **Relation** object, the **ForeignName** property is read/write. Once the **Relation** object is appended to the database, the **ForeignName** property is read-only.</span></span>

<span data-ttu-id="d9d95-111">Seul un objet **Field** appartenant à la collection **Fields** d'un objet **Relation** peut prendre en charge la propriété **ForeignName**.</span><span class="sxs-lookup"><span data-stu-id="d9d95-111">Only a **Field** object that belongs to the **Fields** collection of a **Relation** object can support the **ForeignName** property.</span></span>

<span data-ttu-id="d9d95-p102">Les paramètres de propriété **[Name](connection-name-property-dao.md)** et **ForeignName** d'un objet **Field** spécifient les noms des champs correspondants dans les tables primaires et étrangères d'une relation. Les paramètres de propriété **[Table](relation-table-property-dao.md)** et **[ForeignTable](relation-foreigntable-property-dao.md)** d'un objet **Relation** déterminent les tables primaires et étrangères d'une relation.</span><span class="sxs-lookup"><span data-stu-id="d9d95-p102">The **[Name](connection-name-property-dao.md)** and **ForeignName** property settings for a **Field** object specify the names of the corresponding fields in the primary and foreign tables of a relationship. The **[Table](relation-table-property-dao.md)** and **[ForeignTable](relation-foreigntable-property-dao.md)** property settings for a **Relation** object determine the primary and foreign tables of a relationship.</span></span>

<span data-ttu-id="d9d95-p103">Par exemple, prenons une liste de numéros de pièce valides (dans un champ appelé PartNo) stockée dans une table ValidParts. Vous pourriez établir une relation avec une table OrderItem de sorte que si un numéro de pièce était entré dans la table OrderItem, il devrait déjà exister dans la table ValidParts. Si le numéro de pièce n'existait pas dans la table ValidParts et si vous n'aviez pas défini la propriété **[Attributes](field-attributes-property-dao.md)** de l'objet **Relation** sur **dbRelationDontEnforce**, une erreur capturable surviendrait.</span><span class="sxs-lookup"><span data-stu-id="d9d95-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already exist in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="d9d95-p104">Dans ce cas, la table ValidParts est la table étrangère, la propriété **ForeignTable** de l'objet **Relation** est donc définie sur ValidParts et la propriété **Table** de l'objet **Relation** sur OrderItem. Les propriétés **Name** et **ForeignName** de l'objet **Field** de la collection **Fields** de l'objet **Relation** sont alors définies sur PartNo.</span><span class="sxs-lookup"><span data-stu-id="d9d95-p104">In this case, the ValidParts table is the foreign table, so the **ForeignTable** property of the **Relation** object would be set to ValidParts and the **Table** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="d9d95-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="d9d95-118">Example</span></span>

<span data-ttu-id="d9d95-119">Cet exemple montre comment les propriétés **Table**, **ForeignTable** et **ForeignName** définissent les termes d'une **Relation** entre deux tables.</span><span class="sxs-lookup"><span data-stu-id="d9d95-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
