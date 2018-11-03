---
title: Suppression d’enregistrements à l’aide de la méthode Delete
TOCTitle: Deleting records using the Delete method
ms:assetid: 22917c33-4d14-ebab-d85c-2cbe7f68c560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249003(v=office.15)
ms:contentKeyID: 48543708
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8f9097f791596f45f574749d98919b61f67cb4f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944493"
---
# <a name="deleting-records-using-the-delete-method"></a><span data-ttu-id="228ed-102">Suppression d’enregistrements à l’aide de la méthode Delete</span><span class="sxs-lookup"><span data-stu-id="228ed-102">Deleting records using the Delete method</span></span>


<span data-ttu-id="228ed-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="228ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="228ed-p101">L'utilisation de la méthode **Delete** marque l'enregistrement actif ou un groupe d'enregistrements d'un objet **Recordset** pour suppression. Si l'objet **Recordset** interdit la suppression des enregistrements, une erreur se produit. Si vous êtes en mode de mise à jour immédiate, les suppressions sont effectuées immédiatement dans la base de données. Si la suppression d'un enregistrement échoue (suite à des violations d'intégrité relatives à la base de données, par exemple), l'enregistrement reste en mode de modification après l'appel de la méthode **Update**. En d'autres termes, vous devez annuler la mise à jour à l'aide de la méthode [CancelUpdate](cancelupdate-method-ado.md) avant de quitter l'enregistrement actif (par exemple, en utilisant [Close](close-method-ado.md), [Move](move-method-ado.md) ou [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="228ed-p101">Using the **Delete** method marks the current record or a group of records in a **Recordset** object for deletion. If the **Recordset** object does not allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**. This means that you must cancel the update using [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, using [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="228ed-p102">Si vous êtes en mode de mise à jour par lot, les enregistrements sont marqués pour suppression à partir du cache et la suppression effective intervient lorsque vous appelez la méthode **UpdateBatch**. (Pour consulter les enregistrements supprimés, affectez à la propriété **Filter** la valeur **adFilterAffectedRecords** après l'appel de la méthode **Delete**.)</span><span class="sxs-lookup"><span data-stu-id="228ed-p102">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the **UpdateBatch** method. (To view the deleted records, set the **Filter** property to **adFilterAffectedRecords** after **Delete** is called.)</span></span>

<span data-ttu-id="228ed-p103">Si vous essayez de récupérer des valeurs de champ d'un enregistrement supprimé, une erreur se produit. Après la suppression de l'enregistrement actif, ce dernier reste actif tant que vous n'accédez pas à un autre. Une fois que vous l'avez quitté, il n'est plus accessible.</span><span class="sxs-lookup"><span data-stu-id="228ed-p103">Attempting to retrieve field values from the deleted record generates an error. After deleting the current record, the deleted record remains current until you move to a different record. Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="228ed-p104">Si vous imbriquez des suppressions dans une transaction, vous pouvez récupérer des enregistrements supprimés en utilisant la méthode **RollbackTrans**. Si vous êtes en mode de mise à jour par lot, vous pouvez annuler une suppression ou un groupe de suppressions en attente en utilisant la méthode **CancelBatch**.</span><span class="sxs-lookup"><span data-stu-id="228ed-p104">If you nest deletions in a transaction, you can recover deleted records by using the **RollbackTrans** method. If you are in batch update mode, you can cancel a pending deletion or group of pending deletions by using the **CancelBatch** method.</span></span>

<span data-ttu-id="228ed-p105">Si la tentative de suppression des enregistrements échoue en raison d'un conflit avec les données sous-jacentes (par exemple, si un autre utilisateur a déjà supprimé un enregistrement), le fournisseur retourne des avertissements dans la collection **Errors** sans pour autant interrompre l'exécution du programme. Une erreur d'exécution se produit uniquement en cas de conflits sur tous les enregistrements demandés.</span><span class="sxs-lookup"><span data-stu-id="228ed-p105">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the **Errors** collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="228ed-118">Si la propriété dynamique **Unique Table** est définie et que l'objet **Recordset** résulte de l'exécution d'une opération JOIN sur plusieurs tables, la méthode **Delete** supprime uniquement les lignes de la table nommée dans la propriété **Unique Table**.</span><span class="sxs-lookup"><span data-stu-id="228ed-118">If the **Unique Table** dynamic property is set and the **Recordset** is the result of executing a JOIN operation on multiple tables, the **Delete** method will delete rows only from the table named in the **Unique Table** property.</span></span>

<span data-ttu-id="228ed-p106">La méthode **Delete** prend un argument facultatif qui permet de spécifier les enregistrements affectés par la méthode **Delete**. Les seules valeurs valides pour cet argument sont l'une des deux constantes énumérées **AffectEnum** ADO suivantes :</span><span class="sxs-lookup"><span data-stu-id="228ed-p106">The **Delete** method takes an optional argument that allows you to specify which records are affected by the **Delete** operation. The only valid values for this argument are either of the following ADO **AffectEnum** enumerated constants:</span></span>

  - <span data-ttu-id="228ed-121">**adAffectCurrent** Affecte uniquement l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="228ed-121">**adAffectCurrent**Affects only the current record.</span></span>

  - <span data-ttu-id="228ed-122">**adAffectGroup** Affecte uniquement les enregistrements qui répondent à la valeur de propriété de **filtre** actuelle.</span><span class="sxs-lookup"><span data-stu-id="228ed-122">**adAffectGroup**Affects only records that satisfy the current **Filter** property setting.</span></span> <span data-ttu-id="228ed-123">La propriété **Filter** doit avoir une valeur **FilterGroupEnum** ou un tableau de **signets** pour utiliser cette option.</span><span class="sxs-lookup"><span data-stu-id="228ed-123">The **Filter** property must be set to a **FilterGroupEnum** value or an array of **Bookmarks** to use this option.</span></span>

<span data-ttu-id="228ed-p108">Le code suivant illustre un exemple qui spécifie **adAffectGroup** lors de l'appel de la méthode **Delete**. Cet exemple ajoute quelques enregistrements à l'exemple d'objet **Recordset** et met à jour la base de données. Il filtre ensuite l'objet **Recordset** à l'aide de la constante énumérée de filtre **adFilterAffectedRecords**, qui permet de n'afficher que les enregistrements récemment ajoutés dans l'objet **Recordset**. Enfin, il appelle la méthode **Delete** et spécifie que tous les enregistrements correspondant au au paramètre actuel de la propriété **Filter** (les nouveaux enregistrements) doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="228ed-p108">The following code shows an example of specifying **adAffectGroup** when calling the **Delete** method. This example adds some records to the sample **Recordset** and updates the database. Then it filters the **Recordset** using the **adFilterAffectedRecords** filter enumerated constant, which leaves only the newly added records visible in the **Recordset**. Finally, it calls the **Delete** method and specifies that all of the records that satisfy the current **Filter** property setting (the new records) should be deleted.</span></span>

```vb 
 
'BeginDeleteGroup 
 'add some bogus records 
 With objRs1 
 For i = 0 To 8 
 .AddNew 
 .Fields("CompanyName") = "Shipper Number " & i + 1 
 .Fields("Phone") = "(425) 555-000" & (i + 1) 
 .Update 
 Next i 
 
 're-connect & update 
 .ActiveConnection = GetNewConnection 
 .UpdateBatch 
 
 'filter on newly added records 
 .Filter = adFilterAffectedRecords 
 Debug.Print "Deleting the " & .RecordCount & _ 
 " records you just added." 
 
 'delete the newly added bogus records 
 .Delete adAffectGroup 
 .Filter = adFilterNone 
 Debug.Print .RecordCount & " records remain." 
 
 .Close 
 End With 
'EndDeleteGroup 
```

