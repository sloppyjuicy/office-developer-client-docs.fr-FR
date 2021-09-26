---
title: Recordset2.AbsolutePosition, propriété (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: 91ca203f-0c80-67f4-e180-415b6af05030
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197637(v=office.15)
ms:contentKeyID: 48546358
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053074
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 98a401552dfeda9a456a09a144cdd10246a0bc8a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611776"
---
# <a name="recordset2absoluteposition-property-dao"></a>Recordset2.AbsolutePosition, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie le nombre d’enregistrements relatif de l’enregistrement actif d’un objet **Recordset2**.

## <a name="syntax"></a>Syntaxe

*expression* .AbsolutePosition

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

Vous pouvez utiliser la propriété **AbsolutePosition** pour placer le pointeur d'enregistrement actif sur un enregistrement spécifique en fonction de sa position ordinale dans un objet **Recordset2** de type instantané ou feuille de réponse dynamique. Vous pouvez également déterminer le numéro de l'enregistrement actif en vérifiant le paramètre de la propriété **AbsolutePosition**.

Dans la mesure où la valeur de la propriété **AbsolutePosition** est en base zéro (c'est-à-dire que la valeur 0 référence le premier enregistrement de l'objet **Recordset2**), vous ne pouvez pas lui affecter une valeur supérieure ou égale au nombre d'enregistrements remplis. Si c'est le cas, une erreur piégeable se produit. Vous pouvez déterminer le nombre d'enregistrements remplis dans l'objet **Recordset2** en vérifiant la valeur de la propriété **RecordCount**. La valeur maximale autorisée de la propriété **AbsolutePosition** correspond à la valeur de la propriété **RecordCount** moins 1.

S’il n’existe aucun enregistrement en cours, comme s’il n’y avait aucun enregistrement dans l’objet **Recordset2,** **AbsolutePosition** renvoie –1. Si l'enregistrement actif est supprimé, la valeur de la propriété **AbsolutePosition** n'est pas définie et une erreur piégeable se produit si elle est référencée. Les nouveaux enregistrements sont ajoutés à la fin de la séquence.

Vous ne devez pas utiliser cette propriété comme numéro d'enregistrement de substitution. La meilleure façon de conserver et revenir à une position donnée consiste à utiliser les signets. Ils constituent la seule possibilité de positionner l'enregistrement actif dans tous les types d'objets **Recordset2**. La position d'un enregistrement varie lorsqu'un ou plusieurs enregistrements qui le précèdent sont supprimés. Il n'existe aucune assurance qu'un enregistrement conservera la même position absolue si l'objet **Recordset2** est recréé car l'ordre des enregistrements individuels dans un objet **Recordset** n'est jamais garanti sauf s'il est créé avec une instruction SQL comportant une clause ORDER BY.

> [!NOTE]
> - Si vous affectez une valeur supérieure à zéro à la propriété **AbsolutePosition** d'un objet **Recordset2** récemment ouvert mais toujours vide, une erreur piégeable se produit. Remplissez d'abord l'objet **Recordset2** avec la méthode **MoveLast**.
> - La propriété **AbsolutePosition** n’est pas disponible sur les objets **Recordset2** de type avant uniquement ou sur les objets **Recordset2** ouverts à partir de requêtes pass-through sur des bases de données ODBC connectées au moteur de base de données Microsoft Access.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **AbsolutePosition** pour suivre la progression d'une boucle qui énumère tous les enregistrements d'un objet **Recordset2**.

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
