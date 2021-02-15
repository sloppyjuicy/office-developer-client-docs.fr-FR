---
title: Recordset.EditMode, propriété (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 326f23f95f9ccf8763f76b21df8955c39198a88c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307650"
---
# <a name="recordseteditmode-property-dao"></a><span data-ttu-id="f9642-102">Recordset.EditMode, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="f9642-102">Recordset.EditMode property (DAO)</span></span>


<span data-ttu-id="f9642-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9642-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9642-104">Renvoie une valeur indiquant l’état de modification de l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="f9642-104">Returns a value that indicates the state of editing for the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9642-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9642-105">Syntax</span></span>

<span data-ttu-id="f9642-106">*.* EditMode</span><span class="sxs-lookup"><span data-stu-id="f9642-106">*expression* .EditMode</span></span>

<span data-ttu-id="f9642-107">*expression* Variable qui représente un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f9642-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9642-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9642-108">Remarks</span></span>

<span data-ttu-id="f9642-p101">La valeur renvoyée est un type **Long** spécifiant l'état de modification. La valeur peut être l'une des constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="f9642-p101">The return value is a **Long** that indicates the state of editing. The value can be one of the **[EditModeEnum](editmodeenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="f9642-p102">La propriété **EditMode** est utile lorsqu'un processus d'édition est interrompu, par exemple en raison d'une erreur au cours de la validation. Vous pouvez utiliser la valeur de la propriété **EditMode** pour déterminer si vous devez utiliser la méthode **[Update](recordset-update-method-dao.md)** ou **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="f9642-p102">The **EditMode** property is useful when an editing process is interrupted, for example, by an error during validation. You can use the value of the **EditMode** property to determine whether you should use the **[Update](recordset-update-method-dao.md)** or **[CancelUpdate](recordset-cancelupdate-method-dao.md)** method.</span></span>

<span data-ttu-id="f9642-113">Vous pouvez aussi vérifier si le paramètre de la propriété **[LockEdits](recordset-lockedits-property-dao.md)** est **True** et celui de la propriété **EditMode** a la valeur **dbEditInProgress** afin de déterminer si la page active est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="f9642-113">You can also check to see if the **[LockEdits](recordset-lockedits-property-dao.md)** property setting is **True** and the **EditMode** property setting is **dbEditInProgress** to determine whether the current page is locked.</span></span>

## <a name="example"></a><span data-ttu-id="f9642-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="f9642-114">Example</span></span>

<span data-ttu-id="f9642-p103">Cet exemple illustre la valeur de la propriété **EditMode** sous diverses conditions. La fonction EditModeOutput est nécessaire à l'exécution de la procédure.</span><span class="sxs-lookup"><span data-stu-id="f9642-p103">This example shows the value of the **EditMode** property under various conditions. The EditModeOutput function is required for this procedure to run.</span></span>

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Show the EditMode property under different editing 
     ' states. 
     With rstEmployees 
     EditModeOutput "Before any Edit or AddNew:", .EditMode 
     .Edit 
     EditModeOutput "After Edit:", .EditMode 
     .Update 
     EditModeOutput "After Update:", .EditMode 
     .AddNew 
     EditModeOutput "After AddNew:", .EditMode 
     .CancelUpdate 
     EditModeOutput "After CancelUpdate:", .EditMode 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function EditModeOutput(strTemp As String, _ 
     intEditMode As Integer) 
     
     ' Print report based on the value of the EditMode 
     ' property. 
     Debug.Print strTemp 
     Debug.Print " EditMode = "; 
     
     Select Case intEditMode 
     Case dbEditNone 
     Debug.Print "dbEditNone" 
     Case dbEditInProgress 
     Debug.Print "dbEditInProgress" 
     Case dbEditAdd 
     Debug.Print "dbEditAdd" 
     End Select 
     
    End Function
```
