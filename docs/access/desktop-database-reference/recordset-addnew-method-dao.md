---
title: Méthode Recordset.AddNew (DAO)
TOCTitle: AddNew Method
ms:assetid: 18cb35f6-8652-fb20-2460-3d13fae39d23
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845624(v=office.15)
ms:contentKeyID: 48543483
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052883
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8aee4e63959beca98e96d04d14f817b2b6a30e7c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471187"
---
# <a name="recordsetaddnew-method-dao"></a>Méthode Recordset.AddNew (DAO)


**S’applique à**: Access 2013 | Office 2013

Crée un nouvel enregistrement pour un objet **[Recordset](recordset-object-dao.md)** actualisable.

## <a name="syntax"></a>Syntaxe

*expression* . AddNew

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Utilisez la méthode **AddNew** pour créer et ajouter un nouvel enregistrement pour l’objet **Recordset**, nommé en fonction du jeu d’enregistrements. Cette méthode affecte les valeurs par défaut aux champs et, si aucune valeur par défaut n’est spécifiée, elle leur affecte des valeurs Null (valeurs par défaut spécifiées pour un objet **Recordset** de type table).

Après avoir modifié le nouvel enregistrement, utilisez la méthode **[Update](recordset-update-method-dao.md)** pour enregistrer les modifications et ajouter l'enregistrement à l'objet **Recordset**. Aucune modification n'est implémentée dans la base de données tant que vous n'avez pas utilisé la méthode **Update**.


> [!NOTE]
> <P>[!REMARQUE] Si vous exécutez une méthode <STRONG>AddNew</STRONG>, puis que vous accédez à un autre enregistrement à la suite d'une autre opération sans avoir préalablement appelé la méthode <STRONG>Update</STRONG>, vous perdez toutes vos modifications sans avertissement. En outre, si vous fermez l'objet <STRONG>Recordset</STRONG> ou mettez un terme à la procédure qui déclare l'objet <STRONG>Recordset</STRONG> ou son objet <STRONG><A href="database-object-dao.md">Database</A></STRONG>, le nouvel enregistrement est supprimé sans avertissement.</P>




> [!NOTE]
> <P>[!REMARQUE] Lorsque vous utilisez <STRONG>AddNew</STRONG> dans un espace de travail Microsoft Access et que le moteur de base de données doit créer une nouvelle page pour conserver l'enregistrement actif, le verrouillage de page est de type pessimiste. Si le nouvel enregistrement est ajouté à une page existante, le verrouillage de page est de type optimiste.</P>



Si vous n'avez pas accédé au dernier enregistrement de votre objet **Recordset**, les enregistrements ajoutés aux tables de base par d'autres processus peuvent être inclus s'ils sont placés après l'enregistrement actif. Toutefois, si vous ajoutez un enregistrement à votre propre objet **Recordset**, l'enregistrement est visible dans l'objet **Recordset** et inclus dans la table sous-jacente, où il sera visible pour tout nouvel objet **Recordset**.

La position du nouvel enregistrement dépend du type de l'objet **Recordset**:

  - Dans un objet **Recordset** de type feuille de réponse dynamique, les enregistrements sont insérés à la fin de l'objet **Recordset**, indépendamment des règles de tri ou d'ordre en vigueur lors de l'ouverture de l'objet **Recordset**.

  - Dans un objet **Recordset** de type table dont la propriété **[Index](recordset-index-property-dao.md)** a été définie, les enregistrements sont renvoyés à l'emplacement adéquat en fonction de l'ordre de tri. Si vous n'avez pas défini la propriété **Index**, les nouveaux enregistrements sont renvoyés à la fin de l'objet **Recordset**.

L'enregistrement qui était actif avant d'utiliser **AddNew** le reste. Si vous souhaitez faire du nouvel enregistrement l'enregistrement actif, vous pouvez affecter à la propriété **[Bookmark](recordset-bookmark-property-dao.md)** la valeur du signet identifié par le paramètre de la propriété **[LastModified](recordset-lastmodified-property-dao.md)**.


> [!NOTE]
> <P>[!REMARQUE] Pour ajouter, modifier ou supprimer un enregistrement, ce dernier doit être affecté d'un index unique dans la source de données sous-jacente. Si ce n'est pas le cas, une erreur « Autorisation refusée » se produira lors d'un appel à la méthode <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG> ou <STRONG>Edit</STRONG> dans un espace de travail Microsoft Access.</P>



## <a name="example"></a>Exemple

Cet exemple utilise la méthode **AddNew** pour créer un nouvel enregistrement avec le nom spécifié. La fonction AddName est indispensable pour l'exécution de cette procédure.

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
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
