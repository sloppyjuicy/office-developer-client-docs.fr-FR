---
title: Méthode Recordset2.Edit (DAO)
TOCTitle: Edit Method
ms:assetid: 34c51eee-274d-3511-b5e2-cb74e4925ec8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192452(v=office.15)
ms:contentKeyID: 48544137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052869
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8fbbbe147c4c943044123b711ffb3361af5284cf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928235"
---
# <a name="recordset2edit-method-dao"></a>Méthode Recordset2.Edit (DAO)


**S’applique à**: Access 2013, Office 2013

Copie l'enregistrement actif d'un objet **[Recordset](recordset-object-dao.md)** modifiable vers la mémoire tampon de copie pour modification ultérieure.

## <a name="syntax"></a>Syntaxe

*expression* . Modifier

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Dès que vous utilisez la méthode **Edit**, les modifications apportées aux champs de l'enregistrement actif sont copiées vers la mémoire tampon de copie. Après avoir apporté les modifications requises à l'enregistrement, utilisez la méthode **[Update](recordset2-update-method-dao.md)** pour enregistrer vos modifications.

L'enregistrement qui était actif le reste après avoir utilisé **Edit**.


> [!NOTE]
> <P>[!REMARQUE] Si vous modifiez un enregistrement et que vous effectuez ensuite une opération qui atteint un autre enregistrement sans avoir préalablement utilisé <STRONG>Update</STRONG>, vos modifications sont perdues sans avertissement. En outre, si vous fermez l’objet recordset ou mettre fin à la procédure qui déclare le <STRONG>jeu d’enregistrements</STRONG> ou l’objet parent de <STRONG><A href="database-object-dao.md">base de données</A></STRONG> ou de <STRONG><A href="connection-object-dao.md">connexion</A></STRONG> , votre enregistrement modifié est ignoré sans avertissement.</P>



L'utilisation de la méthode **Edit** génère une erreur dans les cas suivants :

  - Il n'existe pas d'enregistrement actif.

  - L'objet **Connection**, **Database** ou **Recordset** a été ouvert en lecture seule.

  - Aucun champ de l'enregistrement n'est modifiable.

  - L'objet **Database** ou **Recordset** a été ouvert en mode exclusif par un autre utilisateur (espace de travail Microsoft Access).

  - Un autre utilisateur a verrouillé la page contenant votre enregistrement (espace de travail Microsoft Access).

Dans un espace de travail Microsoft Access, lorsque le paramètre de la propriété [**LockEdits**](recordset2-lockedits-property-dao.md) de l'objet **Recordset** a la valeur **True** (verrouillage pessimiste) dans un environnement multi-utilisateur, l'enregistrement reste verrouillé entre le moment de l'appel de la méthode **Edit** et la fin de la mise à jour. Si le paramètre de la propriété **LockEdits** a la valeur **False** (verrouillage optimiste), l'enregistrement est verrouillé et comparé à l'enregistrement prémodifié juste avant sa mise à jour dans la base de données. Si l'enregistrement a été modifié depuis l'appel de la méthode **Edit**, l'opération **Update** échoue avec une erreur d'exécution si vous utilisez la méthode **OpenRecordset** sans spécifier **dbSeeChanges**. Par défaut, les bases de données ISAM installables et ODBC connectées au moteur de base de données Microsoft Access utilisent toujours le verrouillage optimiste.


> [!NOTE]
> <P>[!REMARQUE] Pour ajouter, modifier ou supprimer un enregistrement, ce dernier doit être affecté d'un index unique dans la source de données sous-jacente. Si ce n'est pas le cas, une erreur « Autorisation refusée » se produira lors d'un appel à la méthode <STRONG><A href="recordset2-addnew-method-dao.md">AddNew</A></STRONG>, <STRONG><A href="fields-delete-method-dao.md">Delete</A></STRONG> ou <STRONG>Edit</STRONG> dans un espace de travail Microsoft Access.</P>



## <a name="example"></a>Exemple

Cet exemple utilise la méthode **Edit** pour remplacer les données actuelles par le nom spécifié. La fonction EditName est nécessaire à l'exécution de cette procédure.

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
