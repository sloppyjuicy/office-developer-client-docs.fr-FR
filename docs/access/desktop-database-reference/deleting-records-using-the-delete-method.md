---
title: Suppression des enregistrements à l’aide de la méthode Delete
TOCTitle: Deleting records using the Delete method
ms:assetid: 22917c33-4d14-ebab-d85c-2cbe7f68c560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249003(v=office.15)
ms:contentKeyID: 48543708
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a476e9bc57224b0e46afb31bf092450c26de0a17
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699064"
---
# <a name="deleting-records-using-the-delete-method"></a>Suppression des enregistrements à l’aide de la méthode Delete


**S’applique à**: Access 2013, Office 2013

L'utilisation de la méthode **Delete** marque l'enregistrement actif ou un groupe d'enregistrements d'un objet **Recordset** pour suppression. Si l'objet **Recordset** interdit la suppression des enregistrements, une erreur se produit. Si vous êtes en mode de mise à jour immédiate, les suppressions sont effectuées immédiatement dans la base de données. Si la suppression d'un enregistrement échoue (suite à des violations d'intégrité relatives à la base de données, par exemple), l'enregistrement reste en mode de modification après l'appel de la méthode **Update**. En d'autres termes, vous devez annuler la mise à jour à l'aide de la méthode [CancelUpdate](cancelupdate-method-ado.md) avant de quitter l'enregistrement actif (par exemple, en utilisant [Close](close-method-ado.md), [Move](move-method-ado.md) ou [NextRecordset](nextrecordset-method-ado.md)).

Si vous êtes en mode de mise à jour par lot, les enregistrements sont marqués pour suppression à partir du cache et la suppression effective intervient lorsque vous appelez la méthode **UpdateBatch**. (Pour consulter les enregistrements supprimés, affectez à la propriété **Filter** la valeur **adFilterAffectedRecords** après l'appel de la méthode **Delete**.)

Si vous essayez de récupérer des valeurs de champ d'un enregistrement supprimé, une erreur se produit. Après la suppression de l'enregistrement actif, ce dernier reste actif tant que vous n'accédez pas à un autre. Une fois que vous l'avez quitté, il n'est plus accessible.

Si vous imbriquez des suppressions dans une transaction, vous pouvez récupérer des enregistrements supprimés en utilisant la méthode **RollbackTrans**. Si vous êtes en mode de mise à jour par lot, vous pouvez annuler une suppression ou un groupe de suppressions en attente en utilisant la méthode **CancelBatch**.

Si la tentative de suppression des enregistrements échoue en raison d'un conflit avec les données sous-jacentes (par exemple, si un autre utilisateur a déjà supprimé un enregistrement), le fournisseur retourne des avertissements dans la collection **Errors** sans pour autant interrompre l'exécution du programme. Une erreur d'exécution se produit uniquement en cas de conflits sur tous les enregistrements demandés.

Si la propriété dynamique **Unique Table** est définie et que l'objet **Recordset** résulte de l'exécution d'une opération JOIN sur plusieurs tables, la méthode **Delete** supprime uniquement les lignes de la table nommée dans la propriété **Unique Table**.

La méthode **Delete** prend un argument facultatif qui permet de spécifier les enregistrements affectés par la méthode **Delete**. Les seules valeurs valides pour cet argument sont l'une des deux constantes énumérées **AffectEnum** ADO suivantes :

  - **adAffectCurrent** Affecte uniquement l’enregistrement actif.

  - **adAffectGroup** Affecte uniquement les enregistrements qui répondent à la valeur de propriété de **filtre** actuelle. La propriété **Filter** doit avoir une valeur **FilterGroupEnum** ou un tableau de **signets** pour utiliser cette option.

Le code suivant illustre un exemple qui spécifie **adAffectGroup** lors de l'appel de la méthode **Delete**. Cet exemple ajoute quelques enregistrements à l'exemple d'objet **Recordset** et met à jour la base de données. Il filtre ensuite l'objet **Recordset** à l'aide de la constante énumérée de filtre **adFilterAffectedRecords**, qui permet de n'afficher que les enregistrements récemment ajoutés dans l'objet **Recordset**. Enfin, il appelle la méthode **Delete** et spécifie que tous les enregistrements correspondant au au paramètre actuel de la propriété **Filter** (les nouveaux enregistrements) doivent être supprimés.

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

