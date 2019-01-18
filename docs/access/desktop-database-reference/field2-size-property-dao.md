---
title: Propriété Field2.Size (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f1467414729f4ea82bc2779eeb2bd162465b5ccd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699036"
---
# <a name="field2size-property-dao"></a><span data-ttu-id="2a946-102">Propriété Field2.Size (DAO)</span><span class="sxs-lookup"><span data-stu-id="2a946-102">Field2.Size property (DAO)</span></span>


<span data-ttu-id="2a946-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a946-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="2a946-104">Définit ou renvoie une valeur qui indique la taille maximale, en octets, d'un objet **Field2**.</span><span class="sxs-lookup"><span data-stu-id="2a946-104">Sets or returns a value that indicates the maximum size, in bytes, of a **Field2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a946-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a946-105">Syntax</span></span>

<span data-ttu-id="2a946-106">*expression* . Taille</span><span class="sxs-lookup"><span data-stu-id="2a946-106">*expression* .Size</span></span>

<span data-ttu-id="2a946-107">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="2a946-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a946-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a946-108">Remarks</span></span>

<span data-ttu-id="2a946-109">Pour un objet pas encore ajouté à la collection **[Fields](fields-collection-dao.md)**, cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2a946-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="2a946-p101">Pour les champs (autres que Mémo) contenant des chaînes de caractères, la propriété **Size** indique le nombre de caractères maximal du champ. Pour les champs numériques, la propriété **Size** indique le nombre d'octets de stockage requis.</span><span class="sxs-lookup"><span data-stu-id="2a946-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="2a946-112">L'utilisation de la propriété **Size** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field2** est ajouté, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2a946-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a946-113">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="2a946-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="2a946-114">Utilisation</span><span class="sxs-lookup"><span data-stu-id="2a946-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a946-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="2a946-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="2a946-116">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a946-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a946-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="2a946-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="2a946-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a946-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a946-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="2a946-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="2a946-120">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a946-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a946-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="2a946-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="2a946-122">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a946-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a946-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="2a946-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="2a946-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a946-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a946-p102">Lorsque vous créez un objet **Field2** contenant un type de données autre que Texte, le paramètre de propriété **Type** détermine automatiquement le paramètre de propriété **Size**; vous n'avez pas besoin de le définir. En revanche, pour un objet **Field2** contenant des données de type Texte, vous pouvez définir **Size** sur tout entier jusqu'à la taille de texte maximum (255 pour les bases de données de moteur de base de données Microsoft Access). Si vous ne définissez aucune taille, le champ est aussi grand que le permet la base de données.</span><span class="sxs-lookup"><span data-stu-id="2a946-p102">When you create a **Field2** object with a data type other than Text, the **Type** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field2** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access database engine databases). If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="2a946-p103">Pour les objets **Field2** de type Mémo et Binaire long, **Size** est toujours définie sur 0. Utilisez la propriété **FieldSize** de l'objet **Field2** pour déterminer la taille des données d'un enregistrement spécifique. La taille maximale d'un champ Mémo ou Binaire long est limitée uniquement par les ressources de votre système ou la taille maximale autorisée par la base de données.</span><span class="sxs-lookup"><span data-stu-id="2a946-p103">For Long Binary and Memo **Field2** objects, **Size** is always set to 0. Use the **FieldSize** property of the **Field2** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="2a946-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="2a946-131">Example</span></span>

<span data-ttu-id="2a946-132">Cet exemple illustre la propriété **Size** en énumérant les noms et tailles des objets **Field2** de la table Employees.</span><span class="sxs-lookup"><span data-stu-id="2a946-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field2** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
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
