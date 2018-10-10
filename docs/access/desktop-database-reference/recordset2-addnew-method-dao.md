---
title: Recordset2.AddNew Method (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e8123fc67d8b41b892f92b19605a26384af68b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470624"
---
# <a name="recordset2addnew-method-dao"></a><span data-ttu-id="da459-102">Recordset2.AddNew Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="da459-102">Recordset2.AddNew Method (DAO)</span></span>


<span data-ttu-id="da459-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="da459-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="da459-104">Crée un enregistrement pour un objet **Recordset2** modifiable.</span><span class="sxs-lookup"><span data-stu-id="da459-104">Creates a new record for an updatable **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="da459-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da459-105">Syntax</span></span>

<span data-ttu-id="da459-106">*expression* . AddNew</span><span class="sxs-lookup"><span data-stu-id="da459-106">*expression* .AddNew</span></span>

<span data-ttu-id="da459-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="da459-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="da459-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="da459-108">Remarks</span></span>

<span data-ttu-id="da459-p101">La méthode **AddNew** permet de créer et d'ajouter un nouvel enregistrement dans l'objet **Recordset2** nommé par le jeu d'enregistrements. Cette méthode attribue aux champs les valeurs par défaut ; si aucune valeur par défaut n'est spécifiée, elle leur attribue la valeur Null (valeur par défaut spécifiée pour un objet **Recordset2** de type table).</span><span class="sxs-lookup"><span data-stu-id="da459-p101">Use the **AddNew** method to create and add a new record in the **Recordset2** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset2**).</span></span>

<span data-ttu-id="da459-p102">Après avoir modifié le nouvel enregistrement, utilisez la méthode **[Update](recordset2-update-method-dao.md)** pour enregistrer les modifications et ajouter l'enregistrement à l'objet **Recordset2**. Aucune modification n'intervient dans la base de données tant que vous n'exécutez pas la méthode **Update**.</span><span class="sxs-lookup"><span data-stu-id="da459-p102">After you modify the new record, use the **[Update](recordset2-update-method-dao.md)** method to save the changes and add the record to the **Recordset2**. No changes occur in the database until you use the **Update** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="da459-p103">[!REMARQUE] Si vous émettez une méthode <STRONG>AddNew</STRONG> puis que vous effectuez une opération qui atteint un autre enregistrement, mais sans utiliser <STRONG>Update</STRONG>, vos modifications sont perdues sans avertissement. Par ailleurs, si vous fermez l'objet <STRONG>Recordset2</STRONG> ou que vous terminez la procédure qui déclare l'objet <STRONG>Recordset2</STRONG> ou son objet <STRONG><A href="database-object-dao.md">Database</A></STRONG>, le nouvel enregistrement est ignoré sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="da459-p103">If you issue an <STRONG>AddNew</STRONG> and then perform any operation that moves to another record, but without using <STRONG>Update</STRONG>, your changes are lost without warning. In addition, if you close the <STRONG>Recordset2</STRONG> or end the procedure that declares the <STRONG>Recordset2</STRONG> or its <STRONG><A href="database-object-dao.md">Database</A></STRONG> object, the new record is discarded without warning.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="da459-p104">[!REMARQUE] Lorsque vous utilisez <STRONG>AddNew</STRONG> dans un espace de travail Microsoft Access et que le moteur de base de données doit créer une page pour y stocker l'enregistrement actif, le verrouillage de page est pessimiste. Si le nouvel enregistrement peut être casé dans une page existante, le verrouillage de page est optimiste.</span><span class="sxs-lookup"><span data-stu-id="da459-p104">When you use <STRONG>AddNew</STRONG> in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span></P>



<span data-ttu-id="da459-p105">Si vous n'avez pas atteint le dernier enregistrement de votre objet **Recordset2**, les enregistrements ajoutés aux tables de base par d'autres processus peuvent être inclus s'ils se trouvent après l'enregistrement actif. Toutefois, si vous ajoutez un enregistrement à votre propre objet **Recordset2**, l'enregistrement est visible dans l'objet **Recordset2** et est inclus dans la table sous-jacente où il devient visible pour les nouveaux objets **Recordset2**.</span><span class="sxs-lookup"><span data-stu-id="da459-p105">If you haven't moved to the last record of your **Recordset2**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset2**, however, the record is visible in the **Recordset2** and included in the underlying table where it becomes visible to any new **Recordset2** objects.</span></span>

<span data-ttu-id="da459-119">La position du nouvel enregistrement dépend du type de l'objet **Recordset2**:</span><span class="sxs-lookup"><span data-stu-id="da459-119">The position of the new record depends on the type of **Recordset2**:</span></span>

  - <span data-ttu-id="da459-120">Dans un objet **Recordset2** de type feuille de réponse dynamique, les enregistrements sont insérés à la fin de l'objet **Recordset**, quelles que soient les règles de tri ou de classement qui étaient actives au moment de l'ouverture de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="da459-120">In a dynaset-type **Recordset2** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

  - <span data-ttu-id="da459-p106">Dans un objet **Recordset2** de type table dont la propriété **[Index](recordset2-index-property-dao.md)** a été définie, les enregistrements sont renvoyés à leur propre emplacement en fonction de l'ordre de tri. Si vous n'avez pas défini la propriété **Index**, les nouveaux enregistrements sont renvoyés à la fin de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="da459-p106">In a table-type **Recordset2** object whose **[Index](recordset2-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="da459-p107">L'enregistrement qui était actif avant que vous n'utilisiez **AddNew** reste actif. Si vous voulez que le nouvel enregistrement devienne actif, vous pouvez définir la propriété **[Bookmark](recordset2-bookmark-property-dao.md)** de sorte qu'elle indique le signet identifié par la propriété **[LastModified](recordset2-lastmodified-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="da459-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset2-lastmodified-property-dao.md)** property setting.</span></span>


> [!NOTE]
> <P><span data-ttu-id="da459-p108">[!REMARQUE] Pour ajouter, modifier ou supprimer un enregistrement, ce dernier doit être affecté d'un index unique dans la source de données sous-jacente. Si ce n'est pas le cas, une erreur « Autorisation refusée » se produira lors d'un appel à la méthode <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG> ou <STRONG>Edit</STRONG> dans un espace de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="da459-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG>, or <STRONG>Edit</STRONG> method call in a Microsoft Access workspace.</span></span></P>



## <a name="example"></a><span data-ttu-id="da459-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="da459-127">Example</span></span>

<span data-ttu-id="da459-p109">Cet exemple utilise la méthode **AddNew** pour créer un nouvel enregistrement avec le nom spécifié. La fonction AddName est indispensable pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="da459-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

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
