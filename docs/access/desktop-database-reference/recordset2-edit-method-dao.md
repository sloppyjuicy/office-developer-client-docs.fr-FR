---
title: Recordset2. Edit, méthode (DAO)
TOCTitle: Edit method
ms:assetid: 34c51eee-274d-3511-b5e2-cb74e4925ec8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192452(v=office.15)
ms:contentKeyID: 48544137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052869
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2742b6558c555673937666ea7d27cae1a54fdf73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309435"
---
# <a name="recordset2edit-method-dao"></a>Recordset2. Edit, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Copie l'enregistrement actif d'un objet **[Recordset](recordset-object-dao.md)** modifiable dans la mémoire tampon de la copie en vue d'une modification ultérieure.

## <a name="syntax"></a>Syntaxe

*expression* . Édition

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Dès lors que vous utilisez la méthode **Edit**, les modifications apportées aux champs de l'enregistrement actif sont copiées dans la mémoire tampon de la copie. Après avoir apporté les modifications souhaitées à l'enregistrement, utilisez la méthode **[Update](recordset2-update-method-dao.md)** pour enregistrer vos modifications

L'enregistrement actif demeure actif après l'utilisation de la méthode **Edit**.

> [!NOTE]
> [!REMARQUE] Si vous modifiez un enregistrement et que vous effectuez ensuite une opération qui atteint un autre enregistrement sans avoir préalablement utilisé **Update**, vos modifications sont perdues sans avertissement. De plus, si vous fermez Recordset ou que vous terminez la procédure qui **** déclare l'objet Recordset ou la **[base de données](database-object-dao.md)** parent ou l'objet **[Connection](connection-object-dao.md)** , votre enregistrement modifié est ignoré sans avertissement.

L'utilisation de la méthode **Edit** génère une erreur dans les cas suivants :

- absence d'enregistrement actif ;

- l'objet **Connection**, **Database** ou **Recordset** a été ouvert en lecture seule ;

- les champs de l'enregistrement ne sont pas modifiables ;

- l'objet **Database** ou **Recordset** a été ouvert en mode exclusif par un autre utilisateur (espace de travail Microsoft Access) ;

- un autre utilisateur a verrouillé la page contenant votre enregistrement (espace de travail Microsoft Access).

Dans un espace de travail Microsoft Access, lorsque la propriété [**LockEdits**](recordset2-lockedits-property-dao.md) de l'objet **Recordset** a la valeur **True** (verrouillage pessimiste) dans un environnement multi-utilisateur, l'enregistrement reste verrouillé du moment où vous utilisez **Edit** jusqu'à la fin de la mise à jour. Si la propriété **LockEdits** a la valeur **False** (verrouillage optimiste), l'enregistrement est verrouillé et comparé à l'enregistrement tel qu'il était avant sa modification juste avant sa mise à jour dans la base de données. Si l'enregistrement a changé depuis l'utilisation de la méthode **Edit**, l'opération **Update** échoue avec une erreur d'exécution si vous utilisez **OpenRecordset** sans spécifier **dbSeeChanges**. Par défaut, les bases de données ODBC et ISAM installables connectées au moteur de base de données Microsoft Access utilisent toujours un verrouillage optimiste.

> [!NOTE]
> [!REMARQUE] Pour ajouter, modifier ou supprimer un enregistrement, ce dernier doit être affecté d'un index unique dans la source de données sous-jacente. Si ce n'est pas le cas, une erreur « Autorisation refusée » se produira lors d'un appel à la méthode **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** ou **Edit** dans un espace de travail espace de travail Microsoft Access.

## <a name="example"></a>Exemple

Cet exemple de code montre comment utiliser la méthode **Edit** pour remplacer les données actuelles par le nom spécifié. La procédure EditName est nécessaire à l'exécution de cette procédure.

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Store original data. 
     strOldFirst = rstEmployees!FirstName 
     strOldLast = rstEmployees!LastName 
     
     ' Get new data for record. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed if the user entered something for both fields. 
     If strFirstName <> "" and strLastName <> "" Then 
     ' Update record with new data. 
     EditName rstEmployees, strFirstName, strLastName 
     
     With rstEmployees 
     ' Show old and new data. 
     Debug.Print "Old data: " & strOldFirst & _ 
     " " & strOldLast 
     Debug.Print "New data: " & !FirstName & _ 
     " " & !LastName 
     ' Restore original data because this is a 
     ' demonstration. 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub EditName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Make changes to record and set the bookmark to keep 
     ' the same record current. 
     With rstTemp 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Sub
```
