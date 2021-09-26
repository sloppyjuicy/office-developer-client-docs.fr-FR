---
title: Fields.Refresh, méthode (DAO)
TOCTitle: Refresh Method
ms:assetid: d08597d8-bad6-523b-a083-d824f85b64bc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834723(v=office.15)
ms:contentKeyID: 48547844
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: cdc12e1be540415cbad942dd2cef64020ad1086c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612133"
---
# <a name="fieldsrefresh-method-dao"></a>Fields.Refresh, méthode (DAO)


**S’applique à** : Access 2013, Office 2013


Met à jour les objets dans la collection spécifiée pour refléter le schéma actuel de la base de données.

## <a name="syntax"></a>Syntaxe

*.* Actualiser

*expression* Variable qui représente un objet **Fields**.

## <a name="remarks"></a>Remarques

Pour déterminer la position utilisée par le moteur de base de données Microsoft Access pour les objets **Field** dans la collection **Fields** d'un objet **QueryDef**, **Recordset** ou **TableDef**, utilisez la propriété **OrdinalPosition** de chaque objet **Field**. La modification de la propriété **OrdinalPosition** d'un objet **Field** ne peut pas modifier l'ordre des objets **Field** dans la collection tant que vous n'utilisez pas la méthode **Refresh**.

Utilisez la méthode **Refresh** dans les environnements multi-utilisateurs dans lesquels les autres utilisateurs peuvent modifier la base de données. Vous avez peut-être besoin également de l'utiliser dans des collections concernées indirectement par les modifications apportées à la base de données. Par exemple, si vous modifiez une collection **Users**, il est peut-être nécessaire d'actualiser une collection **Groups** avant d'utiliser cette collection **Groups**.

Une collection est remplie d'objets la première fois qu'elle est nommée. Elle ne reflète pas automatiquement les modifications suivantes effectuées par d'autres utilisateurs. Si un autre utilisateur est susceptible de modifier une collection, utilisez la méthode Refresh dans la collection immédiatement avant d'effectuer une tâche dans l'application qui considère la présence ou l'absence d'un objet déterminé dans la collection. Cela permet de s'assurer que la collection est aussi à jour que possible. Par ailleurs, l'utilisation de la méthode Refresh peut ralentir inutilement les performances.

## <a name="example"></a>Exemple

Dans cet exemple, la méthode **Refresh** est utilisée pour mettre à jour la collection **Fields** de la table Catégories à l'aide des modifications des données **OrdinalPosition**. L'ordre de la collection **Fields** ne change qu'après utilisation de la méthode **Refresh**.

```vb
    Sub RefreshX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Categories") 
     
     With tdfEmployees 
     ' Display original OrdinalPosition data and store it 
     ' in an array. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldLoop In .Fields 
     fldLoop.OrdinalPosition = _ 
     100 - fldLoop.OrdinalPosition 
     Next fldLoop 
     Set fldLoop = Nothing 
     
     ' Print new data. 
     Debug.Print "New OrdinalPosition data before Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     .Fields.Refresh 
     
     ' Print new data, showing how the field order has been 
     ' changed. 
     Debug.Print "New OrdinalPosition data after Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     ' Restore original OrdinalPosition data. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
