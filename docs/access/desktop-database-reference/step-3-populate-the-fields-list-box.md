---
title: 'Étape 3 : remplir la zone de liste Fields'
TOCTitle: 'Step 3: Populate the Fields List Box'
ms:assetid: b304d3a1-2237-d6f5-6e32-c6e5b9946e10
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249855(v=office.15)
ms:contentKeyID: 48547187
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca764e2339d0c866922be2982a168afc03d84c1d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469747"
---
# <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="f2069-102">Étape 3 : remplir la zone de liste Fields</span><span class="sxs-lookup"><span data-stu-id="f2069-102">Step 3: Populate the Fields List Box</span></span>


<span data-ttu-id="f2069-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2069-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="f2069-104">Étape 3 : remplir la zone de liste Fields</span><span class="sxs-lookup"><span data-stu-id="f2069-104">Step 3: Populate the Fields List Box</span></span>

<span data-ttu-id="f2069-105">**Pour remplir la zone de liste Fields**</span><span class="sxs-lookup"><span data-stu-id="f2069-105">**To populate the Fields list box**</span></span>

<span data-ttu-id="f2069-106">Insérez le code suivant dans le gestionnaire d'événements Click de lstMain :</span><span class="sxs-lookup"><span data-stu-id="f2069-106">Insert the following code into the Click event handler of lstMain:</span></span>

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

<span data-ttu-id="f2069-107">Ce code déclare et instancie local **enregistrement** , enregistrement et les objets **Recordset** et et rs, respectivement.</span><span class="sxs-lookup"><span data-stu-id="f2069-107">This code declares and instantiates local **Record** and **Recordset** objects, rec and and rs, respectively.</span></span>

<span data-ttu-id="f2069-108">La ligne correspondant à la ressource sélectionnée dans lstMain devient la ligne active de grs.</span><span class="sxs-lookup"><span data-stu-id="f2069-108">The row corresponding to the resource selected in lstMain is made the current row of grs.</span></span> <span data-ttu-id="f2069-109">Zone de liste **Details** est ensuite effacée et enregistrement est ouvert avec la ligne active de.</span><span class="sxs-lookup"><span data-stu-id="f2069-109">Then the **Details** list box is cleared and rec is opened with the current row of .</span></span> <span data-ttu-id="f2069-110">Zone de liste **Details** est ensuite effacée et enregistrement est ouvert avec la ligne active de grs comme source.</span><span class="sxs-lookup"><span data-stu-id="f2069-110">Then the **Details** list box is cleared and rec is opened with the current row of grs as the source.</span></span>

<span data-ttu-id="f2069-111">Si la ressource est un enregistrement de collection (comme spécifié par **RecordType**), le local **Recordset**, r, est ouvert sur les enfants de l’enregistrement. LstDetails est ensuite rempli avec les valeurs des lignes d’est ouvert sur les enfants de l’enregistrement. LstDetails est ensuite rempli avec les valeurs des lignes de rs.</span><span class="sxs-lookup"><span data-stu-id="f2069-111">If the resource is a collection record (as specified by **RecordType**), the local **Recordset**, rs, is opened on the children of rec. Then lstDetails is filled with the values from the rows of is opened on the children of rec. Then lstDetails is filled with the values from the rows of rs.</span></span>

<span data-ttu-id="f2069-p102">Si la ressource est un enregistrement simple, recFields est appelé. Pour plus d'informations sur recFields, consultez l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="f2069-p102">If the resource is a simple record, recFields is called. For more information about recFields, see the next step.</span></span>

<span data-ttu-id="f2069-114">Si la ressource est un document structuré, aucun code n'est implémenté.</span><span class="sxs-lookup"><span data-stu-id="f2069-114">No code is implemented if the resource is a structured document.</span></span>

