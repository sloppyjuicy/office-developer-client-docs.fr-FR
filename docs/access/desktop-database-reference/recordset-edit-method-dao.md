---
title: Méthode Recordset.Edit (DAO)
TOCTitle: Edit Method
ms:assetid: a64d601b-f446-da40-0020-b99110a72872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821175(v=office.15)
ms:contentKeyID: 48546850
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1221129ee7aaa7d53ada51f7a92dc5e91bc4afee
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925325"
---
# <a name="recordsetedit-method-dao"></a><span data-ttu-id="fa4d6-102">Méthode Recordset.Edit (DAO)</span><span class="sxs-lookup"><span data-stu-id="fa4d6-102">Recordset.Edit method (DAO)</span></span>


<span data-ttu-id="fa4d6-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa4d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa4d6-104">Copie l'enregistrement actif d'un objet **[Recordset](recordset-object-dao.md)** modifiable vers la mémoire tampon de copie pour modification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa4d6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa4d6-105">Syntax</span></span>

<span data-ttu-id="fa4d6-106">*expression* . Modifier</span><span class="sxs-lookup"><span data-stu-id="fa4d6-106">*expression* .Edit</span></span>

<span data-ttu-id="fa4d6-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="fa4d6-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa4d6-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa4d6-108">Remarks</span></span>

<span data-ttu-id="fa4d6-p101">Dès que vous utilisez la méthode **Edit**, les modifications apportées aux champs de l'enregistrement actif sont copiées vers la mémoire tampon de copie. Après avoir apporté les modifications requises à l'enregistrement, utilisez la méthode **[Update](recordset-update-method-dao.md)** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-p101">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, use the **[Update](recordset-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="fa4d6-111">L'enregistrement qui était actif le reste après avoir utilisé **Edit**.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-111">The current record remains current after you use **Edit**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fa4d6-112">[!REMARQUE] Si vous modifiez un enregistrement et que vous effectuez ensuite une opération qui atteint un autre enregistrement sans avoir préalablement utilisé <STRONG>Update</STRONG>, vos modifications sont perdues sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-112">If you edit a record and then perform any operation that moves to another record, but without first using <STRONG>Update</STRONG>, your changes are lost without warning.</span></span> <span data-ttu-id="fa4d6-113">En outre, si vous fermez l’objet recordset ou mettre fin à la procédure qui déclare le <STRONG>jeu d’enregistrements</STRONG> ou l’objet parent de <STRONG><A href="database-object-dao.md">base de données</A></STRONG> ou de <STRONG><A href="connection-object-dao.md">connexion</A></STRONG> , votre enregistrement modifié est ignoré sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-113">In addition, if you close recordset or end the procedure which declares the <STRONG>Recordset</STRONG> or the parent <STRONG><A href="database-object-dao.md">Database</A></STRONG> or <STRONG><A href="connection-object-dao.md">Connection</A></STRONG> object, your edited record is discarded without warning.</span></span></P>



<span data-ttu-id="fa4d6-114">L'utilisation de la méthode **Edit** génère une erreur dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="fa4d6-114">Using **Edit** produces an error if:</span></span>

  - <span data-ttu-id="fa4d6-115">Il n'existe pas d'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-115">There is no current record.</span></span>

  - <span data-ttu-id="fa4d6-116">L'objet **Connection**, **Database** ou **Recordset** a été ouvert en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

  - <span data-ttu-id="fa4d6-117">Aucun champ de l'enregistrement n'est modifiable.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-117">No fields in the record are updatable.</span></span>

  - <span data-ttu-id="fa4d6-118">L'objet **Database** ou **Recordset** a été ouvert en mode exclusif par un autre utilisateur (espace de travail Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fa4d6-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

  - <span data-ttu-id="fa4d6-119">Un autre utilisateur a verrouillé la page contenant votre enregistrement (espace de travail Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fa4d6-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="fa4d6-p103">Dans un espace de travail Microsoft Access, lorsque le paramètre de la propriété [**LockEdits**](recordset-lockedits-property-dao.md) de l'objet **Recordset** a la valeur **True** (verrouillage pessimiste) dans un environnement multi-utilisateur, l'enregistrement reste verrouillé entre le moment de l'appel de la méthode **Edit** et la fin de la mise à jour. Si le paramètre de la propriété **LockEdits** a la valeur **False** (verrouillage optimiste), l'enregistrement est verrouillé et comparé à l'enregistrement prémodifié juste avant sa mise à jour dans la base de données. Si l'enregistrement a été modifié depuis l'appel de la méthode **Edit**, l'opération **Update** échoue avec une erreur d'exécution si vous utilisez la méthode **OpenRecordset** sans spécifier **dbSeeChanges**. Par défaut, les bases de données ISAM installables et ODBC connectées au moteur de base de données Microsoft Access utilisent toujours le verrouillage optimiste.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-p103">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete. If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database. If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**. By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fa4d6-p104">[!REMARQUE] Pour ajouter, modifier ou supprimer un enregistrement, ce dernier doit être affecté d'un index unique dans la source de données sous-jacente. Si ce n'est pas le cas, une erreur « Autorisation refusée » se produira lors d'un appel à la méthode <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG>, <STRONG><A href="fields-delete-method-dao.md">Delete</A></STRONG> ou <STRONG>Edit</STRONG> dans un espace de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG>, <STRONG><A href="fields-delete-method-dao.md">Delete</A></STRONG>, or <STRONG>Edit</STRONG> method call in a Microsoft Access workspace.</span></span></P>



## <a name="example"></a><span data-ttu-id="fa4d6-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="fa4d6-126">Example</span></span>

<span data-ttu-id="fa4d6-p105">Cet exemple utilise la méthode **Edit** pour remplacer les données actuelles par le nom spécifié. La fonction EditName est nécessaire à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="fa4d6-p105">This example uses the **Edit** method to replace the current data with the specified name. The EditName procedure is required for this procedure to run.</span></span>

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
