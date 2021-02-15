---
title: Recordset2.RecordCount, propriété (DAO)
TOCTitle: RecordCount Property
ms:assetid: 77852966-11e9-1773-6e58-53927b84c03b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196071(v=office.15)
ms:contentKeyID: 48545728
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052890
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c23de433f26b5a54b3fee5cc69f67a07b53f8a3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309155"
---
# <a name="recordset2recordcount-property-dao"></a>Recordset2.RecordCount, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Renvoie le nombre d'enregistrements accédés dans un objet **[Recordset](recordset-object-dao.md)** ou le nombre total d'enregistrements dans un objet **Recordset** de type table ou un objet **[TableDef](tabledef-object-dao.md)**. Type **Long** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* .RecordCount

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

Utilisez le **RecordCount** propriété pour déterminer le nombre d’enregistrements dans une **jeu d’enregistrements** ou **TableDef** objet aient été accédé. Le **RecordCount** propriété n’indique pas combien enregistrements sont contenus dans un type vers l’avant uniquement, instantané – ou feuille de réponse dynamique **jeu d’enregistrements** objet jusqu'à ce que tous les enregistrements ont été consultés. Une fois le dernier enregistrement a été accédé, le **RecordCount** propriété indique le nombre total d’enregistrements non supprimés dans la **jeu d’enregistrements** ou **TableDef** objet. Pour forcer le dernier enregistrement pour pouvoir y accéder, utilisez la **[MoveLast](recordset2-movelast-method-dao.md)** méthode sur le **jeu d’enregistrements** objet. Vous pouvez également utiliser une SQL **Count** fonction pour déterminer le nombre d’enregistrements votre requête renverra approximatif.

> [!NOTE]
> À l’aide de la **MoveLast** méthode pour renseigner nouvellement ouverte **jeu d’enregistrements** négatif affecte les performances. Sauf s’il est nécessaire de disposer d’un précises **RecordCount** dès que vous ouvrez un **jeu d’enregistrements**, il est préférable de Patientez jusqu'à ce que vous renseigner le **jeu d’enregistrements** avec d’autres certaines parties du code avant de les chercher la **RecordCount** propriété.

Comme votre application supprime les enregistrements dans un type de feuille de réponse dynamique **jeu d’enregistrements** objet, la valeur de la **RecordCount** propriété diminue. Toutefois, les enregistrements supprimés par d’autres utilisateurs ne sont pas répercutées par le **RecordCount** propriété jusqu'à ce que l’enregistrement actif est positionné à un enregistrement supprimé. Si vous exécutez une transaction qui affecte la **RecordCount** paramètre de la propriété et vous lambda restaurez la transaction le **RecordCount** propriété ne reflète pas le nombre actuel de enregistrements restants.

Le **RecordCount** propriété d’un instantané – ou transférer – uniquement – type **jeu d’enregistrements** objet n’est pas affecté par les modifications apportées dans les tables sous-jacentes.

A **jeu d’enregistrements** ou **TableDef** de l’objet sans enregistrement contient un **RecordCount** paramètre de la propriété de 0.

À l’aide de la **[interroger à nouveau](recordset2-requery-method-dao.md)** méthode sur un **jeu d’enregistrements** objet réinitialisation le **RecordCount** propriété simplement comme si la requête nouveau exécutée.

## <a name="example"></a>Exemple

Cet exemple illustre la **RecordCount** propriété avec différents types de **jeux d’enregistrements** qui précèdent et suivent qu’ils sont remplis.

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
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
