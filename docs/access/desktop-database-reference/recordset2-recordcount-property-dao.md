---
title: Propriété Recordset2.RecordCount (DAO)
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
ms.openlocfilehash: 829804ab6fc2ae3a0e53c782e8d8233cbf1bdc41
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921347"
---
# <a name="recordset2recordcount-property-dao"></a>Propriété Recordset2.RecordCount (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie le nombre d'enregistrements accédés dans un objet **[Recordset](recordset-object-dao.md)** ou le nombre total d'enregistrements dans un objet **Recordset** de type table ou un objet **[TableDef](tabledef-object-dao.md)**. Type **Long** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . RecordCount

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Utilisez la propriété **RecordCount** pour déterminer le nombre d'enregistrements accédés dans un objet **Recordset** ou **TableDef**. La propriété **RecordCount** n’indique pas le nombre d’enregistrements contenu dans un objet **Recordset** de type avant uniquement, instantané ou feuille de réponse dynamique jusqu'à ce que tous les enregistrements ont accédé. Après avoir accédé au dernier enregistrement, la propriété **RecordCount** indique le nombre total d'enregistrements non supprimés dans l'objet **Recordset** ou **TableDef**. Pour forcer l'accès au dernier enregistrement, appelez la méthode **[MoveLast](recordset2-movelast-method-dao.md)** sur l'objet **Recordset**. Vous pouvez également utiliser une fonction SQL **Count** pour déterminer le nombre approximatif d'enregistrements renvoyés par votre requête.


> [!NOTE]
> <P>[!REMARQUE] L'utilisation de la méthode <STRONG>MoveLast</STRONG> pour remplir un objet <STRONG>Recordset</STRONG> récemment ouvert affecte les performances. Sauf s'il est indispensable de connaître précisément la valeur de la propriété <STRONG>RecordCount</STRONG> dès l'ouverture d'un objet <STRONG>Recordset</STRONG>, il est préférable d'attendre que l'objet <STRONG>Recordset</STRONG> soit rempli avec d'autres sections de code avant de vérifier la valeur de la propriété <STRONG>RecordCount</STRONG>.</P>



À mesure que votre application supprime des enregistrements dans un objet **Recordset** de type feuille de réponse dynamique, la valeur de la propriété **RecordCount** diminue. Toutefois, les enregistrements supprimés par d'autres utilisateurs ne sont pas répercutés dans la propriété **RecordCount** tant que l'enregistrement actif est positionné sur un enregistrement supprimé. Si vous exécutez une transaction qui affecte la valeur de la propriété **RecordCount** et que vous annulez par la suite la transaction, la propriété **RecordCount** ne reflètera pas le nombre réel d'enregistrements restants.

La propriété **RecordCount** d’un objet **Recordset** de type instantané ou avant uniquement n’est pas affectée par les modifications apportées aux tables sous-jacentes.

Un objet **Recordset** ou **TableDef** sans enregistrement possède une propriété **RecordCount** égale à 0.

L'appel de la méthode **[Requery](recordset2-requery-method-dao.md)** sur un objet **Recordset** réinitialise la propriété **RecordCount** comme si la requête était réexécutée.

## <a name="example"></a>Exemple

Cet exemple illustre la propriété **RecordCount** avec différents types d'objets **Recordsets** avant et après qu'ils ont été remplis.

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
