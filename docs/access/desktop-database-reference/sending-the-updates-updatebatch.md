---
title: 'Envoi des mises à jour : UpdateBatch'
TOCTitle: 'Sending the Updates: UpdateBatch'
ms:assetid: a840b9a7-7ccd-9c31-7951-8921dadf381e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249778(v=office.15)
ms:contentKeyID: 48546898
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 432c54c16984135bb5492854e2a9e9ac1ca94336
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883364"
---
# <a name="sending-the-updates-updatebatch"></a><span data-ttu-id="930fb-102">Envoi des mises à jour : UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="930fb-102">Sending the Updates: UpdateBatch</span></span>


<span data-ttu-id="930fb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="930fb-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="sending-the-updates-updatebatch-method"></a><span data-ttu-id="930fb-104">Envoi des mises à jour : méthode UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="930fb-104">Sending the Updates: UpdateBatch Method</span></span>

<span data-ttu-id="930fb-p101">Le code suivant permet d'ouvrir un objet **Recordset** en mode de traitement par lot, en affectant à la propriété **LockType** la valeur **adLockBatchOptimistic** et à la propriété **CursorLocation** la valeur **adUseClient**. Il ajoute deux nouveaux enregistrements et modifie les valeurs d'un champ dans un enregistrement existant, en enregistrant les valeurs initiales, puis appelle la méthode **UpdateBatch** pour renvoyer les modifications à la source de données.</span><span class="sxs-lookup"><span data-stu-id="930fb-p101">The following code opens a **Recordset** in batch mode by setting the **LockType** property to **adLockBatchOptimistic** and the **CursorLocation** to **adUseClient**. It adds two new records and changes the value of a field in an existing record, saving the original values, and then calls **UpdateBatch** to send the changes back to the data source.</span></span>

```vb 
 
'BeginBatchUpdate 
    strSQL = "SELECT ShipperId, CompanyName, Phone FROM Shippers" 
                  
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
     
    ' Change value of Phone field for first record in Recordset, saving value 
    ' for later restoration. 
    intId = objRs1("ShipperId") 
    strPhone = objRs1("Phone") 
     
    objRs1("Phone") = "(111) 555-1111" 
     
    'Add two new records 
    For i = 0 To 1 
        objRs1.AddNew 
        objRs1(1) = "New Shipper #" & CStr((i + 1)) 
        objRs1(2) = "(nnn) 555-" & i & i & i & i 
    Next i 
     
    ' Send the updates 
    objRs1.UpdateBatch 
'EndBatchUpdate 
```

<span data-ttu-id="930fb-107">Si vous modifiez l'enregistrement actif ou si vous ajoutez un nouvel enregistrement lorsque vous appelez la méthode **UpdateBatch**, ADO appelle automatiquement la méthode **Update** pour sauvegarder toutes les modifications en cours de l'enregistrement actif avant de transmettre les modifications par lot au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="930fb-107">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

