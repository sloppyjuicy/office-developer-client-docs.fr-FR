---
title: Filtrage des enregistrements mis à jour
TOCTitle: Filtering for Updated Records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 54183ddff6cfb3f3648bc367588aa49dc17a13fe
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867754"
---
# <a name="filtering-for-updated-records"></a><span data-ttu-id="3af73-102">Filtrage des enregistrements mis à jour</span><span class="sxs-lookup"><span data-stu-id="3af73-102">Filtering for Updated Records</span></span>


<span data-ttu-id="3af73-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3af73-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="filtering-for-updated-records"></a><span data-ttu-id="3af73-104">Filtrage des enregistrements mis à jour</span><span class="sxs-lookup"><span data-stu-id="3af73-104">Filtering for Updated Records</span></span>

<span data-ttu-id="3af73-p101">Avant d'invoquer **UpdateBatch**, vous pouvez utiliser la propriété **Recordset** **Filter** pour n'afficher que les enregistrements qui ont subi des modifications depuis l'ouverture du **jeu d'enregistrements** ou la dernière invocation de **UpdateBatch**. Pour ce faire, définissez **Filter** sur **adFilterPendingRecords** pour déterminer le nombre d'enregistrements à mettre à jour, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3af73-p101">Before you call **UpdateBatch**, you can use the **Recordset** **Filter** property to view only those records which have been changed since the **Recordset** was opened or the last call to **UpdateBatch**. To do this, set **Filter** equal to **adFilterPendingRecords** to determine how many records will be updated, as shown below.</span></span>

<span data-ttu-id="3af73-107">Cet exemple développe l'exemple **UpdateBatch** précédent en filtrant le **jeu d'enregistrements** juste avant d'invoquer la méthode **UpdateBatch**, montrant à l'utilisateur les enregistrements qui seront modifiés et lui permettant d'annuler la mise à jour (via la méthode **CancelBatch** ).</span><span class="sxs-lookup"><span data-stu-id="3af73-107">This example extends the previous **UpdateBatch** example by filtering the **Recordset** just before calling the **UpdateBatch**, showing the user which records will change and allowing her to cancel the update (using the **CancelBatch** method).</span></span>

```vb 
 
'BeginFilterAffected 
    objRs1.Filter = adFilterPendingRecords 
    objRs1.MoveFirst 
     
    strMsg = "The following " & objRs1.RecordCount & " values will " & _ 
             "be updated. Do you wish to proceed?" 
    While Not objRs1.EOF 
        strMsg = strMsg & vbCrLf & objRs1(0) & vbTab & objRs1(1) & vbTab & _ 
                 objRs1(2) & vbCrLf 
        objRs1.MoveNext 
    Wend 
     
    blnResp = MsgBox(strMsg, vbYesNo, "Proceed with Update?") 
    If blnResp = True Then 
        objRs1.UpdateBatch 
    Else 
        objRs1.CancelBatch 
    End If 
'EndFilterAffected 
```

