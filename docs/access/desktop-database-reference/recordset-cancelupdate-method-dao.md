---
title: Recordset. CancelUpdate, méthode (DAO)
TOCTitle: CancelUpdate method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5950154d8896678889af01254104a2ac0dfef4cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300678"
---
# <a name="recordsetcancelupdate-method-dao"></a><span data-ttu-id="26c30-102">Recordset. CancelUpdate, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="26c30-102">Recordset.CancelUpdate method (DAO)</span></span>

<span data-ttu-id="26c30-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26c30-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26c30-104">Annule les mises à jour en attente d'un objet **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="26c30-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c30-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26c30-105">Syntax</span></span>

<span data-ttu-id="26c30-106">*expression* . CancelUpdate (***UpdateType***)</span><span class="sxs-lookup"><span data-stu-id="26c30-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="26c30-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="26c30-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="26c30-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26c30-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26c30-109">Nom</span><span class="sxs-lookup"><span data-stu-id="26c30-109">Name</span></span></p></th>
<th><p><span data-ttu-id="26c30-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="26c30-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="26c30-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="26c30-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="26c30-112">Description</span><span class="sxs-lookup"><span data-stu-id="26c30-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26c30-113"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="26c30-113"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="26c30-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="26c30-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="26c30-115"><strong>Entier long</strong></span><span class="sxs-lookup"><span data-stu-id="26c30-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="26c30-116">Défini sur l'une des valeurs <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="26c30-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p><p><span data-ttu-id="26c30-117"><strong>Remarque</strong>: les valeurs <EM>dbUpdateRegular</EM> et <EM>dbUpdateBatch</EM> ne sont valides que si la mise à jour par lot est activée.</span><span class="sxs-lookup"><span data-stu-id="26c30-117"><strong>NOTE</strong>: The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="26c30-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="26c30-118">Remarks</span></span>

<span data-ttu-id="26c30-p101">Vous pouvez utiliser la méthode **CancelUpdate** pour annuler les mises à jour en attente résultant d'une opération **[Edit](recordset-edit-method-dao.md)** ou **[AddNew](recordset-addnew-method-dao.md)**. Par exemple, si un utilisateur appelle la méthode **Edit** ou **AddNew** alors qu'il n'a pas encore appelé la méthode **Update**, **CancelUpdate** annule les modifications apportées consécutivement à l'appel de **Edit** ou **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="26c30-p101">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** operation. For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="26c30-121">Vérifiez la propriété **[EditMode](recordset-editmode-property-dao.md)** de l'objet **Recordset** pour déterminer s'il existe une opération en attente susceptible d'être annulée.</span><span class="sxs-lookup"><span data-stu-id="26c30-121">Check the **[EditMode](recordset-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="26c30-122">[!REMARQUE] Le fait d'utiliser la méthode **CancelUpdate** revient à atteindre un autre enregistrement sans utiliser la méthode **[Update](recordset-update-method-dao.md)**, à ceci près que l'enregistrement actif ne change pas et que plusieurs propriétés, telles que **[BOF](recordset-bof-property-dao.md)** et **[EOF](recordset-eof-property-dao.md)**, ne sont pas mises à jour.</span><span class="sxs-lookup"><span data-stu-id="26c30-122">Using the **CancelUpdate** method has the same effect as moving to another record without using the **[Update](recordset-update-method-dao.md)** method, except that the current record doesn't change, and various properties, such as **[BOF](recordset-bof-property-dao.md)** and **[EOF](recordset-eof-property-dao.md)**, aren't updated.</span></span>


## <a name="example"></a><span data-ttu-id="26c30-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="26c30-123">Example</span></span>

<span data-ttu-id="26c30-124">Cet exemple de code montre comment utiliser la méthode **CancelUpdate** avec la méthode **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="26c30-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="26c30-125">Cet exemple de code montre comment utiliser la méthode **CancelUpdate** avec la méthode **Edit**.</span><span class="sxs-lookup"><span data-stu-id="26c30-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

