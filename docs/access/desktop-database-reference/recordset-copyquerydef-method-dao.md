---
title: Recordset. CopyQueryDef, méthode (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: fee8c2fe-500e-dfb3-21ce-211e54ff334b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837296(v=office.15)
ms:contentKeyID: 48548950
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa6c5aab5f357eef8c62c63c6fca873e64031411
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300559"
---
# <a name="recordsetcopyquerydef-method-dao"></a><span data-ttu-id="eb22d-102">Recordset. CopyQueryDef, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="eb22d-102">Recordset.CopyQueryDef method (DAO)</span></span>


<span data-ttu-id="eb22d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb22d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eb22d-104">Renvoie un objet **[QueryDef](querydef-object-dao.md)** qui est une copie de l'objet **QueryDef** utilisé pour créer l'objet **[Recordset](recordset-object-dao.md)** représenté par l'espace réservé Recordset (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="eb22d-104">Returns a **[QueryDef](querydef-object-dao.md)** object that is a copy of the **QueryDef** used to create the **[Recordset](recordset-object-dao.md)** object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="eb22d-105">.</span><span class="sxs-lookup"><span data-stu-id="eb22d-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="eb22d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb22d-106">Syntax</span></span>

<span data-ttu-id="eb22d-107">*expression* . CopyQueryDef</span><span class="sxs-lookup"><span data-stu-id="eb22d-107">*expression* .CopyQueryDef</span></span>

<span data-ttu-id="eb22d-108">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="eb22d-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb22d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eb22d-109">Return value</span></span>

<span data-ttu-id="eb22d-110">QueryDef</span><span class="sxs-lookup"><span data-stu-id="eb22d-110">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="eb22d-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb22d-111">Remarks</span></span>

<span data-ttu-id="eb22d-112">Vous pouvez utiliser la méthode **CopyQueryDef** pour créer un nouvel objet **QueryDef** qui est un doublon de l'objet **QueryDef** ayant servi à créer l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="eb22d-112">You can use the **CopyQueryDef** method to create a new **QueryDef** that is a duplicate of the **QueryDef** used to create the **Recordset**.</span></span>

<span data-ttu-id="eb22d-p102">Si aucun objet **QueryDef** n'a servi à créer cet objet **Recordset**, une erreur se produit. Vous devez d'abord ouvrir un objet **Recordset** par le biais de la méthode **OpenRecordset** avant d'utiliser la méthode **CopyQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="eb22d-p102">If a **QueryDef** wasn't used to create this **Recordset**, an error occurs. You must first open a **Recordset** with the **OpenRecordset** method before using the **CopyQueryDef** method.</span></span>

<span data-ttu-id="eb22d-115">Cette méthode s'avère utile pour créer un objet **Recordset** à partir d'un objet **QueryDef**, et transmettre cet objet **Recordset** à une fonction ; la fonction doit recréer l'équivalent SQL de la requête, par exemple, pour la modifier d'une certaine manière.</span><span class="sxs-lookup"><span data-stu-id="eb22d-115">This method is useful when you create a **Recordset** object from a **QueryDef**, and pass the **Recordset** to a function, and the function must re-create the SQL equivalent of the query, for example, to modify it in some way.</span></span>

## <a name="example"></a><span data-ttu-id="eb22d-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb22d-116">Example</span></span>

<span data-ttu-id="eb22d-p103">Cet exemple de code montre comment utiliser la méthode **CopyQueryDef** pour créer une copie d'un objet **QueryDef** à partir d'un objet **Recordset** existant et comment modifier cette copie en ajoutant une clause à la propriété SQL. Lorsque vous créez un objet **QueryDef** permanent, il se peut que des espaces, des points-virgules ou des sauts de ligne soient ajoutés à la propriété SQL ; ces caractères supplémentaires doivent être supprimés pour pouvoir joindre de nouvelles clauses à l'instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="eb22d-p103">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the SQL property. When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the SQL property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
     strAdd As String) As QueryDef 
     
     Dim strSQL As String 
     Dim strRightSQL As String 
     
     Set CopyQueryNew = rstTemp.CopyQueryDef 
     With CopyQueryNew 
     ' Strip extra characters. 
     strSQL = .SQL 
     strRightSQL = Right(strSQL, 1) 
     Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
     strRightSQL = Chr(10) Or strRightSQL = vbCr 
     strSQL = Left(strSQL, Len(strSQL) - 1) 
     strRightSQL = Right(strSQL, 1) 
     Loop 
     .SQL = strSQL & strAdd 
     End With 
     
    End Function 
```

<br/>

<span data-ttu-id="eb22d-119">Cet exemple de code illustre une utilisation possible de CopyQueryNew().</span><span class="sxs-lookup"><span data-stu-id="eb22d-119">This example shows a possible use of CopyQueryNew().</span></span>

```vb 
Sub CopyQueryDefX() 
 
 Dim dbsNorthwind As Database 
 Dim qdfEmployees As QueryDef 
 Dim rstEmployees As Recordset 
 Dim intCommand As Integer 
 Dim strOrderBy As String 
 Dim qdfCopy As QueryDef 
 Dim rstCopy As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
 "NewQueryDef", "SELECT FirstName, LastName, " & _ 
 "BirthDate FROM Employees") 
 Set rstEmployees = qdfEmployees.OpenRecordset( _ 
 dbOpenForwardOnly) 
 
 Do While True 
 intCommand = Val(InputBox( _ 
 "Choose field on which to order a new " & _ 
 "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
 "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
 "[Cancel - exit]")) 
 Select Case intCommand 
 Case 1 
 strOrderBy = " ORDER BY FirstName" 
 Case 2 
 strOrderBy = " ORDER BY LastName" 
 Case 3 
 strOrderBy = " ORDER BY BirthDate" 
 Case Else 
 Exit Do 
 End Select 
 Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
 Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
 dbForwardOnly) 
 With rstCopy 
 Do While Not .EOF 
 Debug.Print !LastName & ", " & !FirstName & _ 
 " - " & !BirthDate 
 .MoveNext 
 Loop 
 .Close 
 End With 
 Exit Do 
 Loop 
 
 rstEmployees.Close 
 ' Delete new QueryDef because this is a demonstration. 
 dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

