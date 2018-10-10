---
title: Recordset.EditMode Property (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d7c4f6c97e124f5c3019d5ba2f56ea5594ecb8a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470592"
---
# <a name="recordseteditmode-property-dao"></a>Recordset.EditMode Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Renvoie une valeur qui indique l'état de modification de l'enregistrement actif.

## <a name="syntax"></a>Syntaxe

*expression* . EditMode

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

La valeur de retour est une donnée de type **Long** qui indique l'état de modification. La valeur peut être une des constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.

La propriété **EditMode** est utile lorsqu'un processus de modification est interrompu, par une erreur lors de la validation, par exemple. La valeur de la propriété **EditMode** permet de déterminer la meilleure méthode à utiliser entre **[Update](recordset-update-method-dao.md)** et **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.

Vous pouvez également vérifier si le paramètre de propriété **[LockEdits](recordset-lockedits-property-dao.md)** est défini sur **True** et si le paramètre de propriété **EditMode** est **dbEditInProgress** pour déterminer si la page active est verrouillée.

## <a name="example"></a>Exemple

Cet exemple illustre la valeur de la propriété **EditMode** sous différentes conditions. La fonction EditModeOutput est indispensable pour l'exécution de cette procédure.

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
