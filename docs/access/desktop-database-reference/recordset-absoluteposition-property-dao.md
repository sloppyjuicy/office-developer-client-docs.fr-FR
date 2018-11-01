---
title: Recordset.AbsolutePosition Property (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c13dc234fc70d8cf5e9b14958b5336c39a6a4d7a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886507"
---
# <a name="recordsetabsoluteposition-property-dao"></a>Recordset.AbsolutePosition Property (DAO)

**S’applique à**: Access 2013, Office 2013

Définit ou renvoie le numéro d’enregistrement relatif de l’enregistrement actif d’un objet **Recordset**.

## <a name="syntax"></a>Syntaxe

*expression* . AbsolutePosition

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Vous pouvez utiliser la propriété **AbsolutePosition** pour positionner le pointeur de l'enregistrement actif sur un enregistrement spécifique en fonction de sa position ordinale dans un objet **Recordset** de type feuille de réponse dynamique ou instantané. En outre, vous pouvez déterminer le numéro de l'enregistrement actif en consultant le paramétrage de la propriété **AbsolutePosition**.

La valeur de la propriété **AbsolutePosition** est basée sur zéro, c'est-à-dire que la valeur 0 fait référence au premier enregistrement de l'objet **Recordset**. Par conséquent, il est impossible de la définir sur une valeur supérieure ou égale au nombre d'enregistrements renseignés, sinon vous obtenez une erreur interceptable. Pour connaître le nombre d'enregistrements renseignés dans l'objet **Recordset**, consultez le paramétrage de la propriété **RecordCount**. La valeur maximale autorisée de la propriété **AbsolutePosition** correspond à la valeur de la propriété **RecordCount** moins 1.

Si aucun enregistrement actif, en tant que lorsqu’il n’y a aucun enregistrement dans l’objet **Recordset** , **la propriété AbsolutePosition** renvoie -1. Si l'enregistrement actif est supprimé, la valeur de la propriété **AbsolutePosition** n'est pas définie et une erreur interceptable se produit s'il est référencé. Les nouveaux enregistrements sont ajoutés à la fin de la séquence.

N'utilisez pas cette propriété en tant que numéro d'enregistrement de substitution. Pour conserver une position donnée et y revenir, il est toujours recommandé d'utiliser des signets. En outre, il s'agit de la seule manière de positionner l'enregistrement actif sur tous les types d'objets **Recordset**. Plus particulièrement, la position d'un enregistrement change lors de la suppression d'un ou plusieurs enregistrements qui le précèdent. En outre, il n'est pas certain qu'un enregistrement aura la même position absolue si l'objet **Recordset** est recréé, car l'ordre des enregistrements d'un objet **Recordset** n'est garanti que s'il est créé avec une instruction SQL à l'aide d'une clause ORDER BY.

> [!NOTE]
> - Si vous définissez la propriété **AbsolutePosition** sur une valeur supérieure à zéro pour un nouvel objet **Recordset** ouvert mais non renseigné, vous obtenez une erreur interceptable. Renseignez d'abord l'objet **Recordset** à l'aide de la méthode **MoveLast**.
> - La propriété **AbsolutePosition** n’est pas disponible pour les objets **Recordset** de type avant uniquement ou les objets **Recordset** ouverts à partir de requêtes directes sur des bases de données ODBC connectées au moteur de base de données Microsoft Access.

## <a name="example"></a>Exemple

L'exemple ci-dessous utilise la propriété **AbsolutePosition** pour effectuer le suivi de la progression d'une boucle qui énumère tous les enregistrements d'un objet **Recordset**.

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
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
