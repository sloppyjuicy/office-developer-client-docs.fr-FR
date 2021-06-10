---
title: Recordset2.Edit, méthode (DAO)
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
# <a name="recordset2edit-method-dao"></a><span data-ttu-id="0df35-102">Recordset2.Edit, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="0df35-102">Recordset2.Edit method (DAO)</span></span>

<span data-ttu-id="0df35-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0df35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0df35-104">Copie l’enregistrement actif à partir d’un objet **[Recordset](recordset-object-dao.md)** actualisable dans la mémoire tampon de copie à des fins de modification future.</span><span class="sxs-lookup"><span data-stu-id="0df35-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df35-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0df35-105">Syntax</span></span>

<span data-ttu-id="0df35-106">*expression* .Edit</span><span class="sxs-lookup"><span data-stu-id="0df35-106">*expression* .Edit</span></span>

<span data-ttu-id="0df35-107">*expression* Variable qui représente un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="0df35-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0df35-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="0df35-108">Remarks</span></span>

<span data-ttu-id="0df35-p101">Lorsque vous utilisez le **modifier** méthode, les modifications apportées aux champs de l’enregistrement actif est copié dans la mémoire tampon de copie. Après avoir apporté les modifications souhaitées à l’enregistrement, utilisez la **[mise à jour](recordset2-update-method-dao.md)** méthode pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="0df35-p101">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, use the **[Update](recordset2-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="0df35-111">L’enregistrement actif reste actif après avoir utilisé **modifier**.</span><span class="sxs-lookup"><span data-stu-id="0df35-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="0df35-112">Si vous modifiez un enregistrement et puis d’effectuer une opération qui déplace vers un autre enregistrement, mais sans utiliser première **mise à jour**, vos modifications sont perdues sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="0df35-112">If you edit a record and then perform any operation that moves to another record, but without first using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="0df35-113">De plus, si vous fermez l’objet Recordset ou mettez fin à la procédure déclarant l’objet **Recordset**, l’objet parent **[Database](database-object-dao.md)** ou l’objet **[Connection](connection-object-dao.md)**, votre enregistrement modifié est ignoré sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="0df35-113">In addition, if you close recordset or end the procedure which declares the **Recordset** or the parent **[Database](database-object-dao.md)** or **[Connection](connection-object-dao.md)** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="0df35-114">À l’aide de **modifier** génère une erreur si :</span><span class="sxs-lookup"><span data-stu-id="0df35-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="0df35-115">Il n’existe aucun enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="0df35-115">There is no current record.</span></span>

- <span data-ttu-id="0df35-116">Le **connexion**, **base de données**, ou **jeu d’enregistrements** objet a été ouvert en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0df35-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="0df35-117">Aucun les champs dans l’enregistrement ne sont modifiables.</span><span class="sxs-lookup"><span data-stu-id="0df35-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="0df35-118">Le **base de données** ou **jeu d’enregistrements** a été ouvert usage exclusif par un autre utilisateur (espace de travail Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0df35-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="0df35-119">Un autre utilisateur a verrouillé la page contenant votre enregistrement (espace de travail Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0df35-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="0df35-p103">Dans un espace de travail Microsoft Access, lorsque le **jeu d’enregistrements** d’objet **[LockEdits](recordset2-lockedits-property-dao.md)** paramètre de la propriété est **vrai** (verrouillage pessimiste ) dans un environnement multi-utilisateur reste verrouillé de l’heure de l’enregistrement **modifier** sert jusqu'à ce que la mise à jour est terminée. Si le **LockEdits** paramètre de la propriété est **faux** (verrouillage optimiste), l’enregistrement est verrouillé et par rapport à l’enregistrement déjà modifiée juste avant qu’il est mis à jour dans la base de données. Si l’enregistrement a changé, car vous avez utilisé le **modifier** méthode, le **mise à jour** opération échoue avec une erreur d’exécution si vous utilisez **OpenRecordset** sans spécifiant **dbSeeChanges**. Par défaut, base de données Microsoft Access connectées moteur ODBC et bases de données ISAM toujours utilisent le verrouillage optimiste.</span><span class="sxs-lookup"><span data-stu-id="0df35-p103">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete. If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database. If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**. By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="0df35-p104">Pour ajouter, modifier ou supprimer un enregistrement, il doit y avoir un index unique sur l’enregistrement dans la source de données sous-jacentes. Si non, une erreur « Autorisation refusée » doit se produire sur le **[AddNew](recordset2-addnew-method-dao.md)**, **[supprimer](fields-delete-method-dao.md)**, ou **modifier** méthode Appelez dans un espace de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0df35-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="0df35-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="0df35-126">Example</span></span>

<span data-ttu-id="0df35-p105">Cet exemple utilise la **modifier** méthode pour remplacer les données actuelles par le nom spécifié. La procédure EditName est nécessaire pour exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="0df35-p105">This example uses the **Edit** method to replace the current data with the specified name. The EditName procedure is required for this procedure to run.</span></span>

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
