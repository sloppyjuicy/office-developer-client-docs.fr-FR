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
# <a name="recordsetaddnew-method-dao"></a><span data-ttu-id="02ff4-102">Méthode Recordset.AddNew (DAO)</span><span class="sxs-lookup"><span data-stu-id="02ff4-102">Recordset.AddNew Method (DAO)</span></span>


<span data-ttu-id="02ff4-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="02ff4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="02ff4-104">Crée un nouvel enregistrement pour un objet **[Recordset](recordset-object-dao.md)** actualisable.</span><span class="sxs-lookup"><span data-stu-id="02ff4-104">Creates a new record for an updatable **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="02ff4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02ff4-105">Syntax</span></span>

<span data-ttu-id="02ff4-106">*expression* . AddNew</span><span class="sxs-lookup"><span data-stu-id="02ff4-106">*expression* .AddNew</span></span>

<span data-ttu-id="02ff4-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="02ff4-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="02ff4-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="02ff4-108">Remarks</span></span>

<span data-ttu-id="02ff4-p101">Utilisez la méthode **AddNew** pour créer et ajouter un nouvel enregistrement pour l’objet **Recordset**, nommé en fonction du jeu d’enregistrements. Cette méthode affecte les valeurs par défaut aux champs et, si aucune valeur par défaut n’est spécifiée, elle leur affecte des valeurs Null (valeurs par défaut spécifiées pour un objet **Recordset** de type table).</span><span class="sxs-lookup"><span data-stu-id="02ff4-p101">Use the **AddNew** method to create and add a new record in the **Recordset** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset**).</span></span>

<span data-ttu-id="02ff4-p102">Après avoir modifié le nouvel enregistrement, utilisez la méthode **[Update](recordset-update-method-dao.md)** pour enregistrer les modifications et ajouter l'enregistrement à l'objet **Recordset**. Aucune modification n'est implémentée dans la base de données tant que vous n'avez pas utilisé la méthode **Update**.</span><span class="sxs-lookup"><span data-stu-id="02ff4-p102">After you modify the new record, use the **[Update](recordset-update-method-dao.md)** method to save the changes and add the record to the **Recordset**. No changes occur in the database until you use the **Update** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="02ff4-p103">[!REMARQUE] Si vous exécutez une méthode <STRONG>AddNew</STRONG>, puis que vous accédez à un autre enregistrement à la suite d'une autre opération sans avoir préalablement appelé la méthode <STRONG>Update</STRONG>, vous perdez toutes vos modifications sans avertissement. En outre, si vous fermez l'objet <STRONG>Recordset</STRONG> ou mettez un terme à la procédure qui déclare l'objet <STRONG>Recordset</STRONG> ou son objet <STRONG><A href="database-object-dao.md">Database</A></STRONG>, le nouvel enregistrement est supprimé sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="02ff4-p103">If you issue an <STRONG>AddNew</STRONG> and then perform any operation that moves to another record, but without using <STRONG>Update</STRONG>, your changes are lost without warning. In addition, if you close the <STRONG>Recordset</STRONG> or end the procedure that declares the <STRONG>Recordset</STRONG> or its <STRONG><A href="database-object-dao.md">Database</A></STRONG> object, the new record is discarded without warning.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="02ff4-p104">[!REMARQUE] Lorsque vous utilisez <STRONG>AddNew</STRONG> dans un espace de travail Microsoft Access et que le moteur de base de données doit créer une nouvelle page pour conserver l'enregistrement actif, le verrouillage de page est de type pessimiste. Si le nouvel enregistrement est ajouté à une page existante, le verrouillage de page est de type optimiste.</span><span class="sxs-lookup"><span data-stu-id="02ff4-p104">When you use <STRONG>AddNew</STRONG> in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span></P>



<span data-ttu-id="02ff4-p105">Si vous n'avez pas accédé au dernier enregistrement de votre objet **Recordset**, les enregistrements ajoutés aux tables de base par d'autres processus peuvent être inclus s'ils sont placés après l'enregistrement actif. Toutefois, si vous ajoutez un enregistrement à votre propre objet **Recordset**, l'enregistrement est visible dans l'objet **Recordset** et inclus dans la table sous-jacente, où il sera visible pour tout nouvel objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="02ff4-p105">If you haven't moved to the last record of your **Recordset**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset**, however, the record is visible in the **Recordset** and included in the underlying table where it becomes visible to any new **Recordset** objects.</span></span>

<span data-ttu-id="02ff4-119">La position du nouvel enregistrement dépend du type de l'objet **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="02ff4-119">The position of the new record depends on the type of **Recordset**:</span></span>

  - <span data-ttu-id="02ff4-120">Dans un objet **Recordset** de type feuille de réponse dynamique, les enregistrements sont insérés à la fin de l'objet **Recordset**, indépendamment des règles de tri ou d'ordre en vigueur lors de l'ouverture de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="02ff4-120">In a dynaset-type **Recordset** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

  - <span data-ttu-id="02ff4-p106">Dans un objet **Recordset** de type table dont la propriété **[Index](recordset-index-property-dao.md)** a été définie, les enregistrements sont renvoyés à l'emplacement adéquat en fonction de l'ordre de tri. Si vous n'avez pas défini la propriété **Index**, les nouveaux enregistrements sont renvoyés à la fin de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="02ff4-p106">In a table-type **Recordset** object whose **[Index](recordset-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="02ff4-p107">L'enregistrement qui était actif avant d'utiliser **AddNew** le reste. Si vous souhaitez faire du nouvel enregistrement l'enregistrement actif, vous pouvez affecter à la propriété **[Bookmark](recordset-bookmark-property-dao.md)** la valeur du signet identifié par le paramètre de la propriété **[LastModified](recordset-lastmodified-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="02ff4-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset-lastmodified-property-dao.md)** property setting.</span></span>


> [!NOTE]
> <P><span data-ttu-id="02ff4-p108">[!REMARQUE] Pour ajouter, modifier ou supprimer un enregistrement, ce dernier doit être affecté d'un index unique dans la source de données sous-jacente. Si ce n'est pas le cas, une erreur « Autorisation refusée » se produira lors d'un appel à la méthode <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG> ou <STRONG>Edit</STRONG> dans un espace de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="02ff4-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG>, or <STRONG>Edit</STRONG> method call in a Microsoft Access workspace.</span></span></P>



## <a name="example"></a><span data-ttu-id="02ff4-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="02ff4-127">Example</span></span>

<span data-ttu-id="02ff4-p109">Cet exemple utilise la méthode **AddNew** pour créer un nouvel enregistrement avec le nom spécifié. La fonction AddName est indispensable pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="02ff4-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

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
