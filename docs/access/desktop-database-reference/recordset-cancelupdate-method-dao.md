---
title: Recordset.CancelUpdate Method (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0112d094829753f5b012de80245f93fef3a2a472
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880354"
---
# <a name="recordsetcancelupdate-method-dao"></a><span data-ttu-id="15388-102">Recordset.CancelUpdate Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="15388-102">Recordset.CancelUpdate Method (DAO)</span></span>


<span data-ttu-id="15388-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="15388-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="15388-104">Annule toutes les mises à jour en attente d'un objet **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="15388-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="15388-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15388-105">Syntax</span></span>

<span data-ttu-id="15388-106">*expression* . CancelUpdate (***UpdateType***)</span><span class="sxs-lookup"><span data-stu-id="15388-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="15388-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="15388-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="15388-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15388-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15388-109">Name</span><span class="sxs-lookup"><span data-stu-id="15388-109">Name</span></span></p></th>
<th><p><span data-ttu-id="15388-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="15388-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="15388-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="15388-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="15388-112">Description</span><span class="sxs-lookup"><span data-stu-id="15388-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15388-113">UpdateType</span><span class="sxs-lookup"><span data-stu-id="15388-113">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="15388-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="15388-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="15388-115"><strong>Entier long</strong></span><span class="sxs-lookup"><span data-stu-id="15388-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="15388-116">Affectez une des valeurs de <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="15388-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="15388-117">Les <EM>valeurs de dbUpdateRegular</EM> et <EM>dbUpdateBatch ne</EM> sont valides uniquement si la mise à jour par lot est activée.</span><span class="sxs-lookup"><span data-stu-id="15388-117">The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></P>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="15388-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="15388-118">Remarks</span></span>

<span data-ttu-id="15388-p101">Vous pouvez utiliser la méthode **CancelUpdate** pour annuler toutes les mises à jour en attente résultant d'une opération **[Edit](recordset-edit-method-dao.md)** ou **[AddNew](recordset-addnew-method-dao.md)**. Si, par exemple, un utilisateur appelle la méthode **Edit** ou **AddNew** et n'a pas encore appelé la méthode **Update**, **CancelUpdate** annule toutes les modifications apportées après l'appel de **Edit** ou **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="15388-p101">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** operation. For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="15388-121">Vérifiez la propriété **[EditMode](recordset-editmode-property-dao.md)** de l'objet **Recordset** pour déterminer s'il existe une opération en attente qui peut être annulée.</span><span class="sxs-lookup"><span data-stu-id="15388-121">Check the **[EditMode](recordset-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>


> [!NOTE]
> <P><span data-ttu-id="15388-122">[!REMARQUE] L'utilisation de la méthode <STRONG>CancelUpdate</STRONG> revient à accéder à un autre enregistrement sans utiliser la méthode <STRONG><A href="recordset-update-method-dao.md">Update</A></STRONG>, à cette différence près que l'enregistrement actif ne change pas et que plusieurs propriétés, dont <STRONG><A href="recordset-bof-property-dao.md">BOF</A></STRONG> et <STRONG><A href="recordset-eof-property-dao.md">EOF</A></STRONG>, ne sont pas mises à jour.</span><span class="sxs-lookup"><span data-stu-id="15388-122">Using the <STRONG>CancelUpdate</STRONG> method has the same effect as moving to another record without using the <STRONG><A href="recordset-update-method-dao.md">Update</A></STRONG> method, except that the current record doesn't change, and various properties, such as <STRONG><A href="recordset-bof-property-dao.md">BOF</A></STRONG> and <STRONG><A href="recordset-eof-property-dao.md">EOF</A></STRONG>, aren't updated.</span></span></P>



## <a name="example"></a><span data-ttu-id="15388-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="15388-123">Example</span></span>

<span data-ttu-id="15388-124">Cet exemple illustre l'utilisation de la méthode **CancelUpdate** avec la méthode **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="15388-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

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

<span data-ttu-id="15388-125">Cet exemple illustre l'utilisation de la méthode **CancelUpdate** avec la méthode **Edit**.</span><span class="sxs-lookup"><span data-stu-id="15388-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

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

