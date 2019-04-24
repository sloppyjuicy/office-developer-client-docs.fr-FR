---
title: Recordset2. Move, méthode (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d57e73c52ca515f13d613ed3aeb9cf361054396e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307265"
---
# <a name="recordset2move-method-dao"></a><span data-ttu-id="6f5df-102">Recordset2. Move, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="6f5df-102">Recordset2.Move method (DAO)</span></span>

<span data-ttu-id="6f5df-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f5df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f5df-104">Déplace l'enregistrement actif dans un objet **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="6f5df-104">Moves the position of the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f5df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f5df-105">Syntax</span></span>

<span data-ttu-id="6f5df-106">*expression* . Move (***lignes***, ***signetdébut***)</span><span class="sxs-lookup"><span data-stu-id="6f5df-106">*expression* .Move(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="6f5df-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="6f5df-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f5df-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f5df-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f5df-109">Nom</span><span class="sxs-lookup"><span data-stu-id="6f5df-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6f5df-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="6f5df-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6f5df-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="6f5df-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="6f5df-112">Description</span><span class="sxs-lookup"><span data-stu-id="6f5df-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f5df-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="6f5df-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="6f5df-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6f5df-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6f5df-115"><strong>Entier long</strong></span><span class="sxs-lookup"><span data-stu-id="6f5df-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="6f5df-p101">Nombre de lignes en fonction duquel l'enregistrement est déplacé. Si l'argument rows a une valeur supérieure à 0, l'enregistrement avance (vers la fin du fichier). Si l'argument rows a une valeur inférieure à 0, l'enregistrement recule (vers le début du fichier).</span><span class="sxs-lookup"><span data-stu-id="6f5df-p101">The number of rows the position will move. If rows is greater than 0, the position is moved forward (toward the end of the file). If rows is less than 0, the position is moved backward (toward the beginning of the file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f5df-119"><em>Signetdébut</em></span><span class="sxs-lookup"><span data-stu-id="6f5df-119"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="6f5df-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="6f5df-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="6f5df-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6f5df-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6f5df-p102">Valeur identifiant un signet. Si vous spécifiez l'argument startbookmark, le déplacement s'opère par rapport à ce signet. Sinon, l'opération Move part de l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="6f5df-p102">A value identifying a bookmark. If you specify startbookmark, the move begins relative to this bookmark. Otherwise, Move begins from the current record.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6f5df-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f5df-125">Remarks</span></span>

<span data-ttu-id="6f5df-p103">Si vous utilisez **Move** pour positionner le pointeur d'enregistrement actif avant le premier enregistrement, le pointeur d'enregistrement actif se déplace au début du fichier. Si l'objet **Recordset** ne contient pas d'enregistrements et que sa propriété **[BOF](recordset2-bof-property-dao.md)** a la valeur **True**, le recours à cette méthode pour faire reculer un enregistrement entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="6f5df-p103">If you use **Move** to position the current record pointer before the first record, the current record pointer moves to the beginning of the file. If the **Recordset** contains no records and its **[BOF](recordset2-bof-property-dao.md)** property is **True**, using this method to move backward causes an error.</span></span>

<span data-ttu-id="6f5df-p104">Si vous utilisez **Move** pour positionner le pointeur d'enregistrement actif après le dernier enregistrement, le pointeur d'enregistrement actif se déplace à la fin du fichier. Si l'objet **Recordset** ne contient pas d'enregistrements et que sa propriété **[EOF](recordset2-eof-property-dao.md)** a la valeur **True**, le recours à cette méthode pour faire avancer un enregistrement entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="6f5df-p104">If you use **Move** to position the current record pointer after the last record, the current record pointer position moves to the end of the file. If the **Recordset** contains no records and its **[EOF](recordset2-eof-property-dao.md)** property is **True**, then using this method to move forward causes an error.</span></span>

<span data-ttu-id="6f5df-130">Si la propriété **BOF** ou **EOF** a la valeur **True** et que vous tentez d'utiliser la méthode **Move** sans un signet valide, une erreur d'exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="6f5df-130">If either the **BOF** or **EOF** property is **True** and you attempt to use the **Move** method without a valid bookmark, a run-time error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="6f5df-p105">Lorsque vous appliquez la méthode **Move** à un objet **Recordset** de type avant uniquement, la valeur de l'argument « rows » doit être un entier positif et les signets ne sont pas autorisés. Cela signifie que vous pouvez uniquement faire avancer un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6f5df-p105">When you use **Move** on a forward-only-type **Recordset** object, the rows argument must be a positive integer and bookmarks aren't allowed. This means you can only move forward.</span></span>
> - <span data-ttu-id="6f5df-133">Pour faire de l'enregistrement actif le premier enregistrement, le dernier, le suivant ou le précédent dans un objet **Recordset**, utilisez la méthode **MoveFirst**, **MoveLast**, **MoveNext** ou **MovePrevious**.</span><span class="sxs-lookup"><span data-stu-id="6f5df-133">To make the first, last, next, or previous record in a **Recordset** the current record, use either the **MoveFirst**, **MoveLast**, **MoveNext**, or **MovePrevious** method.</span></span>
> - <span data-ttu-id="6f5df-p106">Le fait d'utiliser la méthode **Move** en attribuant la valeur 0 à l'argument « rows » permet d'extraire facilement les données sous-jacentes de l'enregistrement actif. Cela peut vous être utile si vous souhaitez vous assurer que l'enregistrement actif comporte les données les plus récentes des tables de base. Cela permet également d'annuler les appels **[Edit](recordset2-edit-method-dao.md)** ou **[AddNew](recordset-addnew-method-dao.md)** en cours.</span><span class="sxs-lookup"><span data-stu-id="6f5df-p106">Using **Move** with rows equal to 0 is an easy way to retrieve the underlying data for the current record. This is useful if you want to make sure that the current record has the most recent data from the base tables. It will also cancel any pending **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** calls.</span></span>


## <a name="example"></a><span data-ttu-id="6f5df-137">Exemple</span><span class="sxs-lookup"><span data-stu-id="6f5df-137">Example</span></span>

<span data-ttu-id="6f5df-138">Cet exemple de code montre comment utiliser la méthode **Move** pour positionner le pointeur d’enregistrement en fonction de l’entrée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6f5df-138">This example uses the **Move** method to position the record pointer based on user input.</span></span>

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset2 
       Dim varBookmark As Variant 
       Dim strCommand As String 
       Dim lngMove As Long 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstSuppliers = _ 
          dbsNorthwind.OpenRecordset("SELECT CompanyName, " & _ 
          "City, Country FROM Suppliers ORDER BY CompanyName", _ 
          dbOpenDynaset) 
     
       With rstSuppliers 
          ' Populate recordset. 
          .MoveLast 
          .MoveFirst 
     
          Do While True 
             ' Display information about current record and ask  
             ' how many records to move. 
             strCommand = InputBox( _ 
                "Record " & (.AbsolutePosition + 1) & " of " & _ 
                .RecordCount & vbCr & "Company: " & _ 
                !CompanyName & vbCr & "Location: " & !City & _ 
                ", " & !Country & vbCr & vbCr & _ 
                "Enter number of records to Move " & _ 
                "(positive or negative).") 
     
             If strCommand = "" Then Exit Do 
     
             ' Store bookmark in case the Move doesn't work. 
             varBookmark = .Bookmark 
     
             ' Move method requires parameter of data type Long. 
             lngMove = CLng(strCommand) 
             .Move lngMove 
     
             ' Trap for BOF or EOF. 
             If .BOF Then 
                MsgBox "Too far backward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
             If .EOF Then 
                MsgBox "Too far forward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
          Loop 
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
