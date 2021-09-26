---
title: Recordset2.AddNew, méthode (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9a8368247e1a0dbaa524f3adab4d534c1c0cc7e7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631789"
---
# <a name="recordset2addnew-method-dao"></a>Recordset2.AddNew, méthode (DAO)

**S’applique à** : Access 2013, Office 2013
 
Crée un enregistrement pour un objet **Recordset2** modifiable.

## <a name="syntax"></a>Syntaxe

*expression* .AddNew

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

La méthode **AddNew** permet de créer et d'ajouter un nouvel enregistrement dans l'objet **Recordset2** nommé par le jeu d'enregistrements. Cette méthode attribue aux champs les valeurs par défaut ; si aucune valeur par défaut n'est spécifiée, elle leur attribue la valeur Null (valeur par défaut spécifiée pour un objet **Recordset2** de type table).

Après avoir modifié le nouvel enregistrement, utilisez la méthode **[Update](recordset2-update-method-dao.md)** pour enregistrer les modifications et ajouter l'enregistrement à l'objet **Recordset2**. Aucune modification n'intervient dans la base de données tant que vous n'exécutez pas la méthode **Update**.

> [!NOTE]
> [!REMARQUE] Si vous émettez une méthode **AddNew** puis que vous effectuez une opération qui atteint un autre enregistrement, mais sans utiliser **Update**, vos modifications sont perdues sans avertissement. Par ailleurs, si vous fermez l'objet **Recordset2** ou que vous terminez la procédure qui déclare l'objet **Recordset2** ou son objet **[Database](database-object-dao.md)**, le nouvel enregistrement est ignoré sans avertissement.

> [!NOTE]
> Lorsque vous utilisez **AddNew** dans un espace de travail Microsoft Access et que le moteur de base de données doit créer une nouvelle page pour conserver l'enregistrement actif, le verrouillage de page est de type pessimiste. Si le nouvel enregistrement est ajouté à une page existante, le verrouillage de page est de type optimiste.

Si vous n'avez pas atteint le dernier enregistrement de votre objet **Recordset2**, les enregistrements ajoutés aux tables de base par d'autres processus peuvent être inclus s'ils se trouvent après l'enregistrement actif. Toutefois, si vous ajoutez un enregistrement à votre propre objet **Recordset2**, l'enregistrement est visible dans l'objet **Recordset2** et est inclus dans la table sous-jacente où il devient visible pour les nouveaux objets **Recordset2**.

La position du nouvel enregistrement dépend du type de l'objet **Recordset2**:

- Dans un objet **Recordset2** de type feuille de réponse dynamique, les enregistrements sont insérés à la fin de l'objet **Recordset**, quelles que soient les règles de tri ou de classement qui étaient actives au moment de l'ouverture de l'objet **Recordset**.

- Dans un objet **Recordset2** de type table dont la propriété **[Index](recordset2-index-property-dao.md)** a été définie, les enregistrements sont renvoyés à leur propre emplacement en fonction de l'ordre de tri. Si vous n'avez pas défini la propriété **Index**, les nouveaux enregistrements sont renvoyés à la fin de l'objet **Recordset**.

L'enregistrement qui était actif avant d'utiliser **AddNew** le reste. Si vous souhaitez faire du nouvel enregistrement l'enregistrement actif, vous pouvez affecter à la propriété **[Bookmark](recordset2-bookmark-property-dao.md)** la valeur du signet identifié par le paramètre de la propriété **[LastModified](recordset2-lastmodified-property-dao.md)**.

> [!NOTE]
> Pour ajouter, modifier ou supprimer un enregistrement, ce dernier doit être affecté d'un index unique dans la source de données sous-jacente. Si ce n'est pas le cas, une erreur « Autorisation refusée » se produira lors d'un appel à la méthode **AddNew**, **Delete** ou **Edit** dans un espace de travail Microsoft Access.

## <a name="example"></a>Exemple

Cet exemple utilise la méthode **AddNew** pour créer un nouvel enregistrement portant le nom spécifié. La fonction AddName est nécessaire à l'exécution de cette procédure.

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
