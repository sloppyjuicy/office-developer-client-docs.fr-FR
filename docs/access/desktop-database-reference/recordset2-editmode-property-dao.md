---
title: Propriété Recordset2.EditMode (DAO)
TOCTitle: EditMode Property
ms:assetid: fd61ea2b-e7d7-195f-4114-87e54eba2451
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837240(v=office.15)
ms:contentKeyID: 48548914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053080
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d4043a442bec8c5ce421d85de6256eb9c5cb353f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716746"
---
# <a name="recordset2editmode-property-dao"></a>Propriété Recordset2.EditMode (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie une valeur qui indique l'état de modification de l'enregistrement actif.

## <a name="syntax"></a>Syntaxe

*expression* . EditMode

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

La valeur de retour est une donnée de type **Long** qui indique l'état de modification. La valeur peut être une des constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.

La propriété **EditMode** est utile lorsqu'un processus de modification est interrompu, par une erreur lors de la validation, par exemple. La valeur de la propriété **EditMode** permet de déterminer la meilleure méthode à utiliser entre **[Update](recordset2-update-method-dao.md)** et **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.

Vous pouvez également vérifier si le paramètre de propriété **[LockEdits](recordset2-lockedits-property-dao.md)** est défini sur **True** et si le paramètre de propriété **EditMode** est **dbEditInProgress** pour déterminer si la page active est verrouillée.

## <a name="example"></a>Exemple

Cet exemple illustre la valeur de la propriété **EditMode** sous différentes conditions. La fonction EditModeOutput est indispensable pour l'exécution de cette procédure.

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
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
