---
title: 'Étape 3 : remplir la zone de liste Fields'
TOCTitle: 'Step 3: Populate the Fields List Box'
ms:assetid: b304d3a1-2237-d6f5-6e32-c6e5b9946e10
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249855(v=office.15)
ms:contentKeyID: 48547187
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ae1513c47c79da4f4df7fee2f3f3d7b3507ac1c7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876658"
---
# <a name="step-3-populate-the-fields-list-box"></a>Étape 3 : remplir la zone de liste Fields


**S’applique à**: Access 2013, Office 2013

## <a name="step-3-populate-the-fields-list-box"></a>Étape 3 : Remplir la zone de liste de champs

**Pour remplir la zone de liste Fields**

Insérez le code suivant dans le gestionnaire d'événements Click de lstMain :

```vb 
 
Private Sub lstMain_Click() 
    Dim rec As Record 
    Dim rs As Recordset 
    Set rec = New Record 
    Set rs = New Recordset 
    grs.MoveFirst 
    grs.Move lstMain.ListIndex 
    lstDetails.Clear 
    rec.Open grs 
    Select Case rec.RecordType 
        Case adCollectionRecord: 
            Set rs = rec.GetChildren 
            While Not rs.EOF 
                lstDetails.AddItem rs(0) 
                rs.MoveNext 
            Wend 
        Case adSimpleRecord: 
            recFields rec, lstDetails, txtDetails 
             
        Case adStructDoc: 
    End Select 
     
End Sub 
```

Ce code déclare et instancie local **enregistrement** , enregistrement et les objets **Recordset** et et rs, respectivement.

La ligne correspondant à la ressource sélectionnée dans lstMain devient la ligne active de grs. Zone de liste **Details** est ensuite effacée et enregistrement est ouvert avec la ligne active de. Zone de liste **Details** est ensuite effacée et enregistrement est ouvert avec la ligne active de grs comme source.

Si la ressource est un enregistrement de collection (comme spécifié par **RecordType**), le local **Recordset**, r, est ouvert sur les enfants de l’enregistrement. LstDetails est ensuite rempli avec les valeurs des lignes d’est ouvert sur les enfants de l’enregistrement. LstDetails est ensuite rempli avec les valeurs des lignes de rs.

Si la ressource est un enregistrement simple, recFields est appelé. Pour plus d'informations sur recFields, consultez l'étape suivante.

Si la ressource est un document structuré, aucun code n'est implémenté.

