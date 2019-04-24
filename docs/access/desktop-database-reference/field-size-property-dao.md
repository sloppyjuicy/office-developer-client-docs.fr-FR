---
title: Field. Size, propriété (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 16ce8a9e63c18ded2738035f23e9a1baeff4cc8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293014"
---
# <a name="fieldsize-property-dao"></a><span data-ttu-id="05b02-102">Field. Size, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="05b02-102">Field.Size property (DAO)</span></span>


<span data-ttu-id="05b02-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05b02-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="05b02-104">Définit ou renvoie une valeur indiquant la taille maximale, en octets, d'un objet **[Field](field-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="05b02-104">Sets or returns a value that indicates the maximum size, in bytes, of a **[Field](field-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05b02-105">Syntax</span></span>

<span data-ttu-id="05b02-106">*expression* . Longueur</span><span class="sxs-lookup"><span data-stu-id="05b02-106">*expression* .Size</span></span>

<span data-ttu-id="05b02-107">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="05b02-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="05b02-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="05b02-108">Remarks</span></span>

<span data-ttu-id="05b02-109">Pour un objet pas encore ajouté à la collection **[Fields](fields-collection-dao.md)**, cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="05b02-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="05b02-p101">Pour les champs (autres que les champs de type Mémo) qui contiennent des caractères, la propriété **Size** indique le nombre maximal de caractères que le champ peut contenir. Dans le cas de champs numériques, la propriété **Size** indique le nombre d'octets de stockage requis.</span><span class="sxs-lookup"><span data-stu-id="05b02-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="05b02-112">L'utilisation de la propriété **Size** dépend de l'objet qui contient la collection **Fields** à laquelle l'objet **Field** est ajouté, comme l'illustre le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="05b02-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05b02-113">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="05b02-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="05b02-114">Utilisation</span><span class="sxs-lookup"><span data-stu-id="05b02-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05b02-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="05b02-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="05b02-116">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="05b02-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05b02-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="05b02-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="05b02-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05b02-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05b02-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="05b02-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="05b02-120">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05b02-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05b02-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="05b02-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="05b02-122">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="05b02-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05b02-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="05b02-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="05b02-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="05b02-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="05b02-p102">Lorsque vous créez un objet **Field** avec un type de données autre que Texte, le paramètre de la propriété **[Type](field-type-property-dao.md)** détermine automatiquement le paramètre de la propriété **Size**; vous n'avez pas besoin de la définir. Dans le cas d'un objet **Field** de type Texte, en revanche, vous pouvez définir pour la propriété **Size** un entier dont la valeur maximale correspond à la taille de texte maximale (255 pour les bases de données Microsoft Access). Si vous ne définissez pas la taille, le champ sera aussi grand que ne l'autorise la base de données.</span><span class="sxs-lookup"><span data-stu-id="05b02-p102">When you create a **Field** object with a data type other than Text, the **[Type](field-type-property-dao.md)** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access databases). If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="05b02-p103">Pour les objets **Field** de type Binaire long et Mémo, **Size** a toujours la valeur 0. Utilisez la propriété **[FieldSize](field-fieldsize-property-dao.md)** de l'objet **Field** pour déterminer la taille des données dans un enregistrement spécifique. La taille maximale d'un champ de type Binaire long et Mémo est uniquement limitée par vos ressources système ou la taille maximale autorisée par la base de données.</span><span class="sxs-lookup"><span data-stu-id="05b02-p103">For Long Binary and Memo **Field** objects, **Size** is always set to 0. Use the **[FieldSize](field-fieldsize-property-dao.md)** property of the **Field** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="05b02-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="05b02-131">Example</span></span>

<span data-ttu-id="05b02-132">Cet exemple illustre la propriété **Size** en énumérant les noms et les tailles des objets **Field** dans la table Employees (Employés).</span><span class="sxs-lookup"><span data-stu-id="05b02-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
