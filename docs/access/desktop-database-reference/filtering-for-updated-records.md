---
title: Filtrage des enregistrements mis à jour
TOCTitle: Filtering for updated records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7d65ae6765cc5bf3ddf5b6fefcdf6b2b5e295fba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602618"
---
# <a name="filtering-for-updated-records"></a>Filtrage des enregistrements mis à jour

**S’applique à** : Access 2013, Office 2013

## <a name="filtering-for-updated-records"></a>Filtrage des enregistrements mis à jour

Avant d'invoquer **UpdateBatch**, vous pouvez utiliser la propriété **Recordset** **Filter** pour n'afficher que les enregistrements qui ont subi des modifications depuis l'ouverture du **jeu d'enregistrements** ou la dernière invocation de **UpdateBatch**. Pour ce faire, définissez **Filter** sur **adFilterPendingRecords** pour déterminer le nombre d'enregistrements à mettre à jour, comme illustré ci-dessous.

Cet exemple développe l'exemple **UpdateBatch** précédent en filtrant le **jeu d'enregistrements** juste avant d'invoquer la méthode **UpdateBatch**, montrant à l'utilisateur les enregistrements qui seront modifiés et lui permettant d'annuler la mise à jour (via la méthode **CancelBatch** ).

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

