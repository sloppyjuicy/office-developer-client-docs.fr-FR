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
# <a name="recordset2edit-method-dao"></a><span data-ttu-id="e4cbe-102">Recordset2. Edit, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="e4cbe-102">Recordset2.Edit method (DAO)</span></span>

<span data-ttu-id="e4cbe-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4cbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4cbe-104">Copie l'enregistrement actif d'un objet **[Recordset](recordset-object-dao.md)** modifiable dans la mémoire tampon de la copie en vue d'une modification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e4cbe-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4cbe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4cbe-105">Syntax</span></span>

<span data-ttu-id="e4cbe-106">*expression* . Édition</span><span class="sxs-lookup"><span data-stu-id="e4cbe-106">*expression* .Edit</span></span>

<span data-ttu-id="e4cbe-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="e4cbe-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4cbe-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="e4cbe-108">Remarks</span></span>

<span data-ttu-id="e4cbe-p101">Dès lors que vous utilisez la méthode **Edit**, les modifications apportées aux champs de l'enregistrement actif sont copiées dans la mémoire tampon de la copie. Après avoir apporté les modifications souhaitées à l'enregistrement, utilisez la méthode **[Update](recordset2-update-method-dao.md)** pour enregistrer vos modifications</span><span class="sxs-lookup"><span data-stu-id="e4cbe-p101">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, use the **[Update](recordset2-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="e4cbe-111">L'enregistrement actif demeure actif après l'utilisation de la méthode **Edit**.</span><span class="sxs-lookup"><span data-stu-id="e4cbe-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="e4cbe-112">[!REMARQUE] Si vous modifiez un enregistrement et que vous effectuez ensuite une opération qui atteint un autre enregistrement sans avoir préalablement utilisé **Update**, vos modifications sont perdues sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="e4cbe-112">If you edit a record and then perform any operation that moves to another record, but without first using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="e4cbe-113">De plus, si vous fermez Recordset ou que vous terminez la procédure qui \*\*\*\* déclare l'objet Recordset ou la **[base de données](database-object-dao.md)** parent ou l'objet **[Connection](connection-object-dao.md)** , votre enregistrement modifié est ignoré sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="e4cbe-113">In addition, if you close recordset or end the procedure which declares the **Recordset** or the parent **[Database](database-object-dao.md)** or **[Connection](connection-object-dao.md)** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="e4cbe-114">L'utilisation de la méthode **Edit** génère une erreur dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="e4cbe-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="e4cbe-115">absence d'enregistrement actif ;</span><span class="sxs-lookup"><span data-stu-id="e4cbe-115">There is no current record.</span></span>

- <span data-ttu-id="e4cbe-116">l'objet **Connection**, **Database** ou **Recordset** a été ouvert en lecture seule ;</span><span class="sxs-lookup"><span data-stu-id="e4cbe-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="e4cbe-117">les champs de l'enregistrement ne sont pas modifiables ;</span><span class="sxs-lookup"><span data-stu-id="e4cbe-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="e4cbe-118">l'objet **Database** ou **Recordset** a été ouvert en mode exclusif par un autre utilisateur (espace de travail Microsoft Access) ;</span><span class="sxs-lookup"><span data-stu-id="e4cbe-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="e4cbe-119">un autre utilisateur a verrouillé la page contenant votre enregistrement (espace de travail Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e4cbe-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="e4cbe-p103">Dans un espace de travail Microsoft Access, lorsque la propriété [**LockEdits**](recordset2-lockedits-property-dao.md) de l'objet **Recordset** a la valeur **True** (verrouillage pessimiste) dans un environnement multi-utilisateur, l'enregistrement reste verrouillé du moment où vous utilisez **Edit** jusqu'à la fin de la mise à jour. Si la propriété **LockEdits** a la valeur **False** (verrouillage optimiste), l'enregistrement est verrouillé et comparé à l'enregistrement tel qu'il était avant sa modification juste avant sa mise à jour dans la base de données. Si l'enregistrement a changé depuis l'utilisation de la méthode **Edit**, l'opération **Update** échoue avec une erreur d'exécution si vous utilisez **OpenRecordset** sans spécifier **dbSeeChanges**. Par défaut, les bases de données ODBC et ISAM installables connectées au moteur de base de données Microsoft Access utilisent toujours un verrouillage optimiste.</span><span class="sxs-lookup"><span data-stu-id="e4cbe-p103">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete. If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database. If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**. By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="e4cbe-p104">[!REMARQUE] Pour ajouter, modifier ou supprimer un enregistrement, ce dernier doit être affecté d'un index unique dans la source de données sous-jacente. Si ce n'est pas le cas, une erreur « Autorisation refusée » se produira lors d'un appel à la méthode **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** ou **Edit** dans un espace de travail espace de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e4cbe-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="e4cbe-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4cbe-126">Example</span></span>

<span data-ttu-id="e4cbe-p105">Cet exemple de code montre comment utiliser la méthode **Edit** pour remplacer les données actuelles par le nom spécifié. La procédure EditName est nécessaire à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="e4cbe-p105">This example uses the **Edit** method to replace the current data with the specified name. The EditName procedure is required for this procedure to run.</span></span>

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
