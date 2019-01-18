---
title: Propriété sur Recordset.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9bdc243aae48bd928468362cb86ca077f4abe52
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707611"
---
# <a name="recordsetrecordcount-property-dao"></a>Propriété sur Recordset.RecordCount (DAO)

**S’applique à**: Access 2013, Office 2013

Renvoie le nombre d'enregistrements accédés dans un objet **[Recordset](recordset-object-dao.md)** ou le nombre total d'enregistrements dans un objet **Recordset** de type table ou un objet **[TableDef](tabledef-object-dao.md)**. Type **Long** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . RecordCount

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Utilisez la propriété **RecordCount** pour déterminer le nombre d'enregistrements accédés dans un objet **Recordset** ou **TableDef**. La propriété **RecordCount** n’indique pas le nombre d’enregistrements contenu dans un objet **Recordset** de type avant uniquement, instantané ou feuille de réponse dynamique jusqu'à ce que tous les enregistrements ont accédé. Après avoir accédé au dernier enregistrement, la propriété **RecordCount** indique le nombre total d'enregistrements non supprimés dans l'objet **Recordset** ou **TableDef**. Pour forcer l'accès au dernier enregistrement, appelez la méthode **[MoveLast](recordset-movelast-method-dao.md)** sur l'objet **Recordset**. Vous pouvez également utiliser une fonction SQL **Count** pour déterminer le nombre approximatif d'enregistrements renvoyés par votre requête.

> [!NOTE]
> [!REMARQUE] L'utilisation de la méthode **MoveLast** pour remplir un objet **Recordset** récemment ouvert affecte les performances. Sauf s'il est indispensable de connaître précisément la valeur de la propriété **RecordCount** dès l'ouverture d'un objet **Recordset**, il est préférable d'attendre que l'objet **Recordset** soit rempli avec d'autres sections de code avant de vérifier la valeur de la propriété **RecordCount**.

À mesure que votre application supprime des enregistrements dans un objet **Recordset** de type feuille de réponse dynamique, la valeur de la propriété **RecordCount** diminue. Toutefois, les enregistrements supprimés par d'autres utilisateurs ne sont pas répercutés dans la propriété **RecordCount** tant que l'enregistrement actif est positionné sur un enregistrement supprimé. Si vous exécutez une transaction qui affecte la valeur de la propriété **RecordCount** et que vous annulez par la suite la transaction, la propriété **RecordCount** ne reflètera pas le nombre réel d'enregistrements restants.

La propriété **RecordCount** d’un objet **Recordset** de type instantané ou avant uniquement n’est pas affectée par les modifications apportées aux tables sous-jacentes.

Un objet **Recordset** ou **TableDef** sans enregistrement possède une propriété **RecordCount** égale à 0.

L'appel de la méthode **[Requery](recordset-requery-method-dao.md)** sur un objet **Recordset** réinitialise la propriété **RecordCount** comme si la requête était réexécutée.

## <a name="example"></a>Exemple

Cet exemple illustre la propriété **RecordCount** avec différents types d'objets **Recordsets** avant et après qu'ils ont été remplis.

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
