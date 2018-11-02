---
title: Propriété Relation.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: db19d2ad-5965-214c-211d-9a8eb9c3c522
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835337(v=office.15)
ms:contentKeyID: 48548098
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 01b9a49b5b8ec9b702b3fd5beb8b03e3b2365788
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919828"
---
# <a name="relationattributes-property-dao"></a><span data-ttu-id="4d5fb-102">Propriété Relation.Attributes (DAO)</span><span class="sxs-lookup"><span data-stu-id="4d5fb-102">Relation.Attributes property (DAO)</span></span>


<span data-ttu-id="4d5fb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d5fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d5fb-p101">Définit ou renvoie une valeur spécifiant une ou plusieurs caractéristiques d'un objet **Relation**. Type **Long** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="4d5fb-p101">Sets or returns a value that indicates one or more characteristics of a **Relation** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d5fb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d5fb-106">Syntax</span></span>

<span data-ttu-id="4d5fb-107">*expression* . Attributs</span><span class="sxs-lookup"><span data-stu-id="4d5fb-107">*expression* .Attributes</span></span>

<span data-ttu-id="4d5fb-108">*expression* Variable qui représente un objet **Relation** .</span><span class="sxs-lookup"><span data-stu-id="4d5fb-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d5fb-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d5fb-109">Remarks</span></span>

<span data-ttu-id="4d5fb-110">Cette propriété est en lecture/écriture pour les objets non encore ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="4d5fb-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="4d5fb-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="4d5fb-111">Example</span></span>

<span data-ttu-id="4d5fb-112">Cet exemple affiche la propriété **Attributes** des objets **Field**, **Relation** et **TableDef** dans la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="4d5fb-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

