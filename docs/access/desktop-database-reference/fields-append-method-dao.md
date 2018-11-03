---
title: Méthode Fields.Append (DAO)
TOCTitle: Append Method
ms:assetid: a0e553ba-6a57-09af-3436-4f6ca3cbe561
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820791(v=office.15)
ms:contentKeyID: 48546719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 70fa0aba5385157453a1e9b009a167f036dc874b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929117"
---
# <a name="fieldsappend-method-dao"></a><span data-ttu-id="60505-102">Méthode Fields.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="60505-102">Fields.Append method (DAO)</span></span>


<span data-ttu-id="60505-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60505-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="60505-104">Ajoute un objet **[Field](field-object-dao.md)** dans la collection **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="60505-104">Adds a new **[Field](field-object-dao.md)** to the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="60505-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60505-105">Syntax</span></span>

<span data-ttu-id="60505-106">*expression* . Append (***objet***)</span><span class="sxs-lookup"><span data-stu-id="60505-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="60505-107">*expression* Variable qui représente un objet **Fields** .</span><span class="sxs-lookup"><span data-stu-id="60505-107">*expression* A variable that represents a **Fields** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="60505-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60505-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60505-109">Name</span><span class="sxs-lookup"><span data-stu-id="60505-109">Name</span></span></p></th>
<th><p><span data-ttu-id="60505-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="60505-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="60505-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="60505-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="60505-112">Description</span><span class="sxs-lookup"><span data-stu-id="60505-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60505-113">Objet</span><span class="sxs-lookup"><span data-stu-id="60505-113">Object</span></span></p></td>
<td><p><span data-ttu-id="60505-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="60505-114">Required</span></span></p></td>
<td><p><span data-ttu-id="60505-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="60505-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="60505-116">Variable d'objet représentant le champ qui est ajouté à la collection.</span><span class="sxs-lookup"><span data-stu-id="60505-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="60505-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="60505-117">Remarks</span></span>

<span data-ttu-id="60505-118">Vous pouvez utiliser la méthode **Append** pour ajouter une table à une base de données, ajouter un champ à une table ou à un index.</span><span class="sxs-lookup"><span data-stu-id="60505-118">You can use the **Append** method to add a new table to a database, add a field to a table, and add a field to an index.</span></span>

<span data-ttu-id="60505-119">L'objet ajouté devient un objet persistant, stocké sur le disque, tant que vous ne le supprimez pas à l'aide de la méthode **Delete**.</span><span class="sxs-lookup"><span data-stu-id="60505-119">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="60505-120">L'ajout d'un nouvel objet a lieu immédiatement, mais vous devez utiliser la méthode **Refresh** dans toutes les autres collections qui peuvent être affectées par les modifications apportées à la structure de la base de données.</span><span class="sxs-lookup"><span data-stu-id="60505-120">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="60505-121">Si l'objet que vous ajoutez n'est pas complet (par exemple, si vous n'avez pas ajouté d'objets **Field** à une collection **Fields** d'un objet **Index** avant qu'il soit ajouté à une collection **Indexes**) ou si les propriétés définies dans un ou plusieurs objets subordonnés sont incorrectes, l'utilisation de la méthode **Append** entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="60505-121">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="60505-122">Par exemple, si vous n’avez pas spécifié un type de champ, puis essayez d’ajouter l’objet **Field** à la collection **Fields** d’un objet **TableDef** , à l’aide de la méthode **Append** déclenche une erreur d’exécution.</span><span class="sxs-lookup"><span data-stu-id="60505-122">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="60505-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="60505-123">Example</span></span>

<span data-ttu-id="60505-p102">Cet exemple utilise la méthode **Append** ou la méthode **Delete** pour modifier la collection **Fields** d'une **TableDef**. La procédure AppendDeleteField est nécessaire à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="60505-p102">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**. The AppendDeleteField procedure is required for this procedure to run.</span></span>

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
