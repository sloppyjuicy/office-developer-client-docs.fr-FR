---
title: Recordset2.EditMode, propriété (DAO)
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
ms.localizationpriority: medium
ms.openlocfilehash: aadb8c331e34b1552f584fd8d63f0958f341dcfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626126"
---
# <a name="recordset2editmode-property-dao"></a>Recordset2.EditMode, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie une valeur indiquant l’état de modification de l’enregistrement actif.

## <a name="syntax"></a>Syntaxe

*.* EditMode

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

La valeur renvoyée est un type **Long** spécifiant l'état de modification. La valeur peut être l'une des constantes **[EditModeEnum](editmodeenum-enumeration-dao.md)**.

La propriété **EditMode** est utile lorsqu'un processus d'édition est interrompu, par exemple en raison d'une erreur au cours de la validation. Vous pouvez utiliser la valeur de la propriété **EditMode** pour déterminer si vous devez utiliser la méthode **[Update](recordset2-update-method-dao.md)** ou **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.

Vous pouvez aussi vérifier si le paramètre de la propriété **[LockEdits](recordset2-lockedits-property-dao.md)** est **True** et celui de la propriété **EditMode** a la valeur **dbEditInProgress** afin de déterminer si la page active est verrouillée.

## <a name="example"></a>Exemple

Cet exemple illustre la valeur de la propriété **EditMode** sous diverses conditions. La fonction EditModeOutput est nécessaire à l'exécution de la procédure.

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
