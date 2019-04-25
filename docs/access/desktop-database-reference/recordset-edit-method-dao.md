---
title: Recordset.Edit, méthode (DAO)
TOCTitle: Edit Method
ms:assetid: a64d601b-f446-da40-0020-b99110a72872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821175(v=office.15)
ms:contentKeyID: 48546850
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 82dc6e175c7168d5c1b042e85dce7b77aa96b575
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300538"
---
# <a name="recordsetedit-method-dao"></a>Recordset.Edit, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Copie l’enregistrement actif à partir d’un objet**[Recordset](recordset-object-dao.md)** actualisable dans la mémoire tampon de copie à des fins de modification future.

## <a name="syntax"></a>Syntaxe

*expression* .Edit

*expression* Variable représentant un objet **Recordset**.

## <a name="remarks"></a>Remarques

Lorsque vous utilisez le **modifier** méthode, les modifications apportées aux champs de l’enregistrement actif est copié dans la mémoire tampon de copie. Après avoir apporté les modifications souhaitées à l’enregistrement, utilisez la ** [mise à jour](recordset-update-method-dao.md) ** méthode pour enregistrer vos modifications.

L’enregistrement actif reste actif après avoir utilisé **modifier**.

> [!NOTE]
> Si vous modifiez un enregistrement et puis d’effectuer une opération qui déplace vers un autre enregistrement, mais sans utiliser première **mise à jour**, vos modifications sont perdues sans avertissement. De plus, si vous fermez l’objet Recordset ou mettez fin à la procédure déclarant l’objet **Recordset**, l’objet parent **[Database](database-object-dao.md)** ou l’objet **[Connection](connection-object-dao.md)**, votre enregistrement modifié est ignoré sans avertissement.

À l’aide de **modifier** génère une erreur si :

- Il n’existe aucun enregistrement actif.

- Le **connexion**, **base de données**, ou **jeu d’enregistrements** objet a été ouvert en lecture seule.

- Aucun les champs dans l’enregistrement ne sont modifiables.

- Le **base de données** ou **jeu d’enregistrements** a été ouvert usage exclusif par un autre utilisateur (espace de travail Microsoft Access).

- Un autre utilisateur a verrouillé la page contenant votre enregistrement (espace de travail Microsoft Access).

Dans un espace de travail Microsoft Access, lorsque le **jeu d’enregistrements** d’objet ** [LockEdits](recordset-lockedits-property-dao.md) ** paramètre de la propriété est **vrai** (verrouillage pessimiste ) dans un environnement multi-utilisateur reste verrouillé de l’heure de l’enregistrement **modifier** sert jusqu'à ce que la mise à jour est terminée. Si le **LockEdits** paramètre de la propriété est **faux** (verrouillage optimiste), l’enregistrement est verrouillé et par rapport à l’enregistrement déjà modifiée juste avant qu’il est mis à jour dans la base de données. Si l’enregistrement a changé, car vous avez utilisé le **modifier** méthode, le **mise à jour** opération échoue avec une erreur d’exécution si vous utilisez **OpenRecordset** sans spécifiant **dbSeeChanges**. Par défaut, base de données Microsoft Access connectées moteur ODBC et bases de données ISAM toujours utilisent le verrouillage optimiste.

> [!NOTE]
> Pour ajouter, modifier ou supprimer un enregistrement, il doit y avoir un index unique sur l’enregistrement dans la source de données sous-jacentes. Si non, une erreur « Autorisation refusée » doit se produire sur le ** [AddNew](recordset-addnew-method-dao.md)**, ** [supprimer](fields-delete-method-dao.md)**, ou **modifier** méthode Appelez dans un espace de travail Microsoft Access.

## <a name="example"></a>Exemple

Cet exemple utilise la **modifier** méthode pour remplacer les données actuelles par le nom spécifié. La procédure EditName est nécessaire pour exécuter cette procédure.

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Sub EditName(rstTemp As Recordset, _ 
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
