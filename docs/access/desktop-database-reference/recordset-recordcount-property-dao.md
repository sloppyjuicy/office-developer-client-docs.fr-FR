---
title: Recordset.RecordCount, propriété (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 6c857c0723b4efdc14189192c7bdb9dc2b860fe6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611818"
---
# <a name="recordsetrecordcount-property-dao"></a>Recordset.RecordCount, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Renvoie le nombre d'enregistrements accédés dans un objet **[Recordset](recordset-object-dao.md)** ou le nombre total d'enregistrements dans un objet **Recordset** de type table ou un objet **[TableDef](tabledef-object-dao.md)**. Type **Long** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* .RecordCount

*expression* Variable représentant un objet **Recordset**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **RecordCount** pour déterminer le nombre d'enregistrements accédés dans un objet **Recordset** ou **TableDef**. La propriété **RecordCount** n'indique pas le nombre d'enregistrements contenus dans un objet **Recordset** de type avant uniquement, instantané ou feuille de réponse dynamique avant que tous les enregistrements aient été accédés. Après avoir accédé au dernier enregistrement, la propriété **RecordCount** indique le nombre total d'enregistrements non supprimés dans l'objet **Recordset** ou **TableDef**. Pour forcer l'accès au dernier enregistrement, appelez la méthode **[MoveLast](recordset-movelast-method-dao.md)** sur l'objet **Recordset**. Vous pouvez également utiliser une fonction SQL **Count** pour déterminer le nombre approximatif d'enregistrements renvoyés par votre requête.

> [!NOTE]
> À l’aide de la **MoveLast** méthode pour renseigner nouvellement ouverte **jeu d’enregistrements** négatif affecte les performances. Sauf s’il est nécessaire de disposer d’un précises **RecordCount** dès que vous ouvrez un **jeu d’enregistrements**, il est préférable de Patientez jusqu'à ce que vous renseigner le **jeu d’enregistrements** avec d’autres certaines parties du code avant de les chercher la **RecordCount** propriété.

Comme votre application supprime les enregistrements dans un type de feuille de réponse dynamique **jeu d’enregistrements** objet, la valeur de la **RecordCount** propriété diminue. Toutefois, les enregistrements supprimés par d’autres utilisateurs ne sont pas répercutées par le **RecordCount** propriété jusqu'à ce que l’enregistrement actif est positionné à un enregistrement supprimé. Si vous exécutez une transaction qui affecte la **RecordCount** paramètre de la propriété et vous lambda restaurez la transaction le **RecordCount** propriété ne reflète pas le nombre actuel de enregistrements restants.

Le **RecordCount** propriété d’un instantané – ou transférer – uniquement – type **jeu d’enregistrements** objet n’est pas affecté par les modifications apportées dans les tables sous-jacentes.

A **jeu d’enregistrements** ou **TableDef** de l’objet sans enregistrement contient un **RecordCount** paramètre de la propriété de 0.

À l’aide de la **[interroger à nouveau](recordset-requery-method-dao.md)** méthode sur un **jeu d’enregistrements** objet réinitialisation le **RecordCount** propriété simplement comme si la requête nouveau exécutée.

## <a name="example"></a>Exemple

Cet exemple illustre la **RecordCount** propriété avec différents types de **jeux d’enregistrements** qui précèdent et suivent qu’ils sont remplis.

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```
