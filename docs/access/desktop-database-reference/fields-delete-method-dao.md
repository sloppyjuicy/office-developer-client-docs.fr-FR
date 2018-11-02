---
title: Méthode Fields.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: a8e249e7-7526-3eff-a5cf-70cab2081970
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821417(v=office.15)
ms:contentKeyID: 48546913
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052868
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4faa23fa2b7bdedc85bba5151c04a804a560155e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923671"
---
# <a name="fieldsdelete-method-dao"></a><span data-ttu-id="47141-102">Méthode Fields.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="47141-102">Fields.Delete method (DAO)</span></span>


<span data-ttu-id="47141-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47141-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47141-104">Supprime un objet **[Field](field-object-dao.md)** de la collection **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="47141-104">Deletes a **[Field](field-object-dao.md)** from the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="47141-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47141-105">Syntax</span></span>

<span data-ttu-id="47141-106">*expression* . Supprimer (***nom***)</span><span class="sxs-lookup"><span data-stu-id="47141-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="47141-107">*expression* Variable qui représente un objet **Fields** .</span><span class="sxs-lookup"><span data-stu-id="47141-107">*expression* A variable that represents a **Fields** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="47141-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47141-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47141-109">Name</span><span class="sxs-lookup"><span data-stu-id="47141-109">Name</span></span></p></th>
<th><p><span data-ttu-id="47141-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="47141-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="47141-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="47141-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="47141-112">Description</span><span class="sxs-lookup"><span data-stu-id="47141-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47141-113">Name</span><span class="sxs-lookup"><span data-stu-id="47141-113">Name</span></span></p></td>
<td><p><span data-ttu-id="47141-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="47141-114">Required</span></span></p></td>
<td><p><span data-ttu-id="47141-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="47141-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="47141-116">Champ à supprimer.</span><span class="sxs-lookup"><span data-stu-id="47141-116">The field to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="47141-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="47141-117">Remarks</span></span>

<span data-ttu-id="47141-118">La suppression d'un objet stocké a lieu immédiatement, mais vous devez utiliser la méthode **Refresh** dans toutes les autres collections qui peuvent être affectées par les modifications apportées à la structure de la base de données.</span><span class="sxs-lookup"><span data-stu-id="47141-118">The deletion of a stored object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

## <a name="example"></a><span data-ttu-id="47141-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="47141-119">Example</span></span>

<span data-ttu-id="47141-p101">Cet exemple utilise la méthode **Append** ou la méthode **Delete** pour modifier la collection **Fields** d'une **TableDef**. La procédure AppendDeleteField est nécessaire à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="47141-p101">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**. The AppendDeleteField procedure is required for this procedure to run.</span></span>

```vb
    Sub AppendX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Add three new fields. 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "E-mail", dbText, 50 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Http", dbText, 80 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Quota", dbInteger, 5 
     
     Debug.Print "Fields after Append" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show the new fields. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     ' Delete the newly added fields. 
     AppendDeleteField tdfEmployees, "DELETE", "E-mail" 
     AppendDeleteField tdfEmployees, "DELETE", "Http" 
     AppendDeleteField tdfEmployees, "DELETE", "Quota" 
     
     Debug.Print "Fields after Delete" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show that the new 
     ' fields have been deleted. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub AppendDeleteField(tdfTemp As TableDef, _ 
     strCommand As String, strName As String, _ 
     Optional varType, Optional varSize) 
     
     With tdfTemp 
     
     ' Check first to see if the TableDef object is 
     ' updatable. If it isn't, control is passed back to 
     ' the calling procedure. 
     If .Updatable = False Then 
     MsgBox "TableDef not Updatable! " & _ 
     "Unable to complete task." 
     Exit Sub 
     End If 
     
     ' Depending on the passed data, append or delete a 
     ' field to the Fields collection of the specified 
     ' TableDef object. 
     If strCommand = "APPEND" Then 
     .Fields.Append .CreateField(strName, _ 
     varType, varSize) 
     Else 
     If strCommand = "DELETE" Then .Fields.Delete _ 
     strName 
     End If 
     
     End With 
     
    End Sub
```
