---
title: Propriété Recordset.PercentPosition (DAO)
TOCTitle: PercentPosition Property
ms:assetid: aebbda44-ed72-7a6c-0cd5-28c8997d4d96
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821751(v=office.15)
ms:contentKeyID: 48547077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 31f1cbf1f6bbc2f2c7ce855cccb667e71638b1b8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929568"
---
# <a name="recordsetpercentposition-property-dao"></a>Propriété Recordset.PercentPosition (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur indiquant l'emplacement approximatif de l'enregistrement actif dans l'objet **[Recordset](recordset-object-dao.md)** en fonction du pourcentage d'enregistrements dans cet objet **Recordset**.

## <a name="syntax"></a>Syntaxe

*expression* . PercentPosition

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Pour indiquer ou modifier la position approximative de l'enregistrement actif dans un objet **Recordset**, vous pouvez vérifier ou définir la propriété **PercentPosition**. Lorsque vous manipulez un objet **Recordset** de type feuille de réponse dynamique ou instantané, ouvert directement à partir d'une table de base, commencez par remplir l'objet **Recordset** en accédant au dernier enregistrement avant de définir ou vérifier la propriété **PercentPosition**. Si vous utilisez la propriété **PercentPosition** avant d'avoir entièrement rempli l'objet **Recordset**, le volume de déplacements est relatif au nombre d'enregistrements accédés, tel qu'il est spécifié dans le paramètre de la propriété **[RecordCount](recordset-recordcount-property-dao.md)**. Vous pouvez accéder au dernier enregistrement à l'aide de la méthode **[MoveLast](recordset-movelast-method-dao.md)**.


> [!NOTE]
> <P>[!REMARQUE] Il est déconseillé d'utiliser la propriété <STRONG>PercentPosition</STRONG> si votre intention est de faire d'un enregistrement spécifique de l'objet <STRONG>Recordset</STRONG> l'enregistrement actif. La propriété <STRONG><A href="recordset-bookmark-property-dao.md">Bookmark</A></STRONG> est plus adaptée pour cela.</P>



Dès que vous définissez une valeur pour la propriété **PercentPosition**, l'enregistrement qui occupe la position approximative correspondant à cette valeur devient l'enregistrement actif et la propriété **PercentPosition** est réinitialisée avec une valeur qui reflète la position approximative de l'enregistrement actif. Par exemple, si votre objet **Recordset** contient seulement cinq enregistrements et que vous définissez la valeur 77 pour la propriété **PercentPosition**, la valeur renvoyée par la propriété **PercentPosition** sera vraisemblablement 80 et non 77.

La propriété **PercentPosition** s’applique à tous les types d’objets **Recordset** à l’exception des objets **Recordset** de type avant uniquement ou les objets **Recordset** ouverts à partir de requêtes directes sur des bases de données distantes.

Vous pouvez utiliser la propriété **PercentPosition** avec une barre de défilement dans un formulaire ou une zone de texte pour indiquer l'emplacement de l'enregistrement actif dans un objet **Recordset**.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **PercentPosition** pour indiquer la position du pointeur d'enregistrement actif par rapport au début de l'objet **Recordset**.

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim strFind As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' PercentPosition only works with dynasets or snapshots. 
     Set rstProducts = dbsNorthwind.OpenRecordset( _ 
     "SELECT ProductName FROM Products " & _ 
     "ORDER BY ProductName", dbOpenSnapshot) 
     
     With rstProducts 
     ' Populate the Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show current record information and ask user 
     ' for input. 
     strMessage = "Product: " & !ProductName & vbCr & _ 
     "The record pointer is " & _ 
     Format(.PercentPosition, "##0.0") & _ 
     "% from the " & vbCr & _ 
     "beginning of the Recordset." & vbCr & _ 
     "Please enter a character search string " & _ 
     "for a product name." 
     strFind = Trim(InputBox(strMessage)) 
     If strFind = "" Then Exit Do 
     
     ' Try to find a record matching the search string. 
     .FindFirst "ProductName >= '" & strFind & "'" 
     If .NoMatch Then .MoveLast 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
