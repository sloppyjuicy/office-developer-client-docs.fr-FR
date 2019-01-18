---
title: Propriété Recordset.LastModified (DAO)
TOCTitle: LastModified Property
ms:assetid: 7386f25b-bde1-a446-e980-640696a3bfec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195859(v=office.15)
ms:contentKeyID: 48545640
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052898
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 232a87b1d34cacccaeb7c380ec522f5ba1def028
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725930"
---
# <a name="recordsetlastmodified-property-dao"></a><span data-ttu-id="ed82b-102">Propriété Recordset.LastModified (DAO)</span><span class="sxs-lookup"><span data-stu-id="ed82b-102">Recordset.LastModified property (DAO)</span></span>


<span data-ttu-id="ed82b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed82b-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="ed82b-104">Renvoie un signet indiquant le plus récemment enregistrement ajouté ou modifié.</span><span class="sxs-lookup"><span data-stu-id="ed82b-104">Returns a bookmark indicating the most recently added or changed record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed82b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed82b-105">Syntax</span></span>

<span data-ttu-id="ed82b-106">*expression* . LastModified</span><span class="sxs-lookup"><span data-stu-id="ed82b-106">*expression* .LastModified</span></span>

<span data-ttu-id="ed82b-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="ed82b-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed82b-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="ed82b-108">Remarks</span></span>

<span data-ttu-id="ed82b-p101">La propriété **LastModified** permet de déplacer le dernier enregistrement ajouté ou modifié. Utilisez la propriété **LastModified** avec des objets **[Recordset](recordset-object-dao.md)** de type table ou feuille de réponse dynamique. L'enregistrement doit être ajouté ou modifié dans l'objet **Recordset** lui-même pour que la propriété **LastModified** ait une valeur.</span><span class="sxs-lookup"><span data-stu-id="ed82b-p101">You can use the **LastModified** property to move to the most recently added or updated record. Use the **LastModified** property with table- and dynaset-type **[Recordset](recordset-object-dao.md)** objects. A record must be added or modified in the **Recordset** object itself in order for the **LastModified** property to have a value.</span></span>

## <a name="example"></a><span data-ttu-id="ed82b-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="ed82b-112">Example</span></span>

<span data-ttu-id="ed82b-113">Cet exemple utilise la propriété **LastModified** pour déplacer le pointeur d'enregistrement courant sur un enregistrement ayant été modifié et sur un enregistrement nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="ed82b-113">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="ed82b-p102">Cet exemple utilise la méthode **AddNew** pour créer un nouvel enregistrement avec le nom spécifié. La fonction AddName est indispensable pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="ed82b-p102">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
