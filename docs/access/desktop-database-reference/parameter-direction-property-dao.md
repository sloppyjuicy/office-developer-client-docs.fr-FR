---
title: Propriété Parameter.Direction (DAO)
TOCTitle: Direction Property
ms:assetid: b78c87ff-1181-21ef-7126-92d309751005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822422(v=office.15)
ms:contentKeyID: 48547300
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053586
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3260fd3f01e8ca22d5be4f8d14f6376c31e2735a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712259"
---
# <a name="parameterdirection-property-dao"></a>Propriété Parameter.Direction (DAO)


**S’applique à**: Access 2013, Office 2013


## <a name="syntax"></a>Syntaxe

*expression* . Direction

*expression* Variable qui représente un objet **Parameter** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est une valeur longue pouvant être définie sur l'une des constantes **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)**.

La propriété **Direction** permet de déterminer si le paramètre est un paramètre d'entrée, de sortie, ou les deux, ou la valeur de retour de la procédure. Certains pilotes ODBC ne fournissent aucune information sur la direction des paramètres vers une instruction SELECT ou une invocation de procédure. Dans ce cas, il convient de définir la direction avant d'exécuter la requête.

Par exemple, la procédure suivante renvoie une valeur à partir d’une procédure stockée appelée « obtenir\_employés » :

{? = appel get\_employés}

Cet appel produit un paramètre : la valeur de retour. Vous devez définir la direction de ce paramètre sur **dbParamOutput** ou **dbParamReturnValue** avant d'exécuter l'objet **[QueryDef](querydef-object-dao.md)**.

Vous devez définir toutes les directions de paramètre sauf **dbParamInput** avant d'accéder aux valeurs des paramètres ou de les définir et avant d'exécuter l'objet **QueryDef**.

Utilisez **dbParamReturnValue** pour les valeurs de retour, mais dans les cas où cette option n'est pas prise en charge par le pilote ou le serveur, utilisez plutôt **dbParamOutput**.

Le pilote Microsoft SQL Server définit automatiquement la propriété **Direction** pour tous les paramètres de procédure. Certains pilotes ODBC ne peuvent pas déterminer la direction d'un paramètre de requête. Dans ce cas, il convient de définir la direction avant d'exécuter la requête.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **Direction** pour configurer les paramètres d'une requête sur une source de données ODBC.

```vb 
Sub DirectionX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim strSQL As String 
 Dim intLoop As Integer 
 
 ' Create ODBC workspace and open a connection to a 
 ' Microsoft SQL Server database. 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Set SQL string to call the stored procedure 
 ' getempsperjob. 
 strSQL = "{ call getempsperjob (?, ?) }" 
 
 Set qdfTemp = conMain.CreateQueryDef("", strSQL) 
 
 With qdfTemp 
 ' Indicate that the two query parameters will only 
 ' pass information to the stored procedure. 
 .Parameters(0).Direction = dbParamInput 
 .Parameters(1).Direction = dbParamInput 
 
 ' Assign initial parameter values. 
 .Parameters(0) = "0877" 
 .Parameters(1) = 0 
 
 Set rstTemp = .OpenRecordset() 
 
 With rstTemp 
 ' Loop through all valid values for the second 
 ' parameter. For each value, requery the recordset 
 ' to obtain the correct results and then print out 
 ' the contents of the recordset. 
 For intLoop = 1 To 14 
 qdfTemp.Parameters(1) = intLoop 
 .Requery 
 Debug.Print "Publisher = " & _ 
 qdfTemp.Parameters(0) & _ 
 ", job = " & intLoop 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 Next intLoop 
 .Close 
 End With 
 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

