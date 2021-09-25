---
title: Parameter, objet (DAO)
TOCTitle: Parameter Object
ms:assetid: 194efd23-6086-13ac-beb9-c2aec101d6fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845640(v=office.15)
ms:contentKeyID: 48543495
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 78a1b7a497e31e031d15fbccb4181279ddfab67c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568760"
---
# <a name="parameter-object-dao"></a>Parameter, objet (DAO)


**S’applique à** : Access 2013, Office 2013

Un objet **Parameter** représente une valeur fournie à une requête. Le paramètre est associé à un objet **QueryDef** créé à partir d'une requête avec paramètres

## <a name="remarks"></a>Remarques

Grâce aux objets **Parameter**, vous pouvez modifier les arguments d'un objet **QueryDef** exécuté fréquemment sans devoir recompiler la requête.

À l'aide des propriétés d'un objet **Parameter**, vous pouvez définir un paramètre de requête pouvant être modifié avant l'exécution de la requête. Vous pouvez :

  - Utiliser la propriété **Name** pour renvoyer le nom d'un paramètre.

  - Utiliser la propriété **Value** pour définir ou renvoyer les valeurs de paramètre à utiliser dans la requête.

  - Utiliser la propriété **Type** pour renvoyer le type de données de l'objet **Parameter**.

  - Utiliser la propriété **Direction** pour indiquer si le paramètre est un paramètre d'entrée et/ou de sortie.

## <a name="example"></a>Exemple

Cet exemple démontre les objets **Parameter** et la collection **Parameters** en créant un objet **QueryDef** temporaire et en extrayant les données sur la base des modifications apportées aux objets **Parameters** de l'objet **QueryDef**. La procédure ParametersChange est requise pour exécuter cette opération.

```vb
    Sub ParameterX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfReport As QueryDef 
     Dim prmBegin As Parameter 
     Dim prmEnd As Parameter 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create temporary QueryDef object with two 
     ' parameters. 
     Set qdfReport = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS dteBegin DateTime, dteEnd DateTime; " & _ 
     "SELECT EmployeeID, COUNT(OrderID) AS NumOrders " & _ 
     "FROM Orders WHERE ShippedDate BETWEEN " & _ 
     "[dteBegin] AND [dteEnd] GROUP BY EmployeeID " & _ 
     "ORDER BY EmployeeID") 
     Set prmBegin = qdfReport.Parameters!dteBegin 
     Set prmEnd = qdfReport.Parameters!dteEnd 
     
     ' Print report using specified parameter values. 
     ParametersChange qdfReport, prmBegin, #1/1/95#, _ 
     prmEnd, #6/30/95# 
     ParametersChange qdfReport, prmBegin, #7/1/95#, _ 
     prmEnd, #12/31/95# 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub ParametersChange(qdfTemp As QueryDef, _ 
     prmFirst As Parameter, dteFirst As Date, _ 
     prmLast As Parameter, dteLast As Date) 
     ' Report function for ParameterX. 
     
     Dim rstTemp As Recordset 
     Dim fldLoop As Field 
     
     ' Set parameter values and open recordset from 
     ' temporary QueryDef object. 
     prmFirst = dteFirst 
     prmLast = dteLast 
     Set rstTemp = _ 
     qdfTemp.OpenRecordset(dbOpenForwardOnly) 
     Debug.Print "Period " & dteFirst & " to " & dteLast 
     
     ' Enumerate recordset. 
     Do While Not rstTemp.EOF 
     
     ' Enumerate Fields collection of recordset. 
     For Each fldLoop In rstTemp.Fields 
     Debug.Print " - " & fldLoop.Name & " = " & fldLoop; 
     Next fldLoop 
     
     Debug.Print 
     rstTemp.MoveNext 
     Loop 
     
     rstTemp.Close 
     
    End Sub
```
