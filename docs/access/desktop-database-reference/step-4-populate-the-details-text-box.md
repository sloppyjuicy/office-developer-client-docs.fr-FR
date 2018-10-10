---
title: 'Étape 4 : remplir la zone de texte Details'
TOCTitle: 'Step 4: Populate the Details Text Box'
ms:assetid: fa5e4482-8986-0c03-1e46-7b7fefb5fb58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250278(v=office.15)
ms:contentKeyID: 48548839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e0f04d52edc55c7ccc5163bc9a858d7bc8845702
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470931"
---
# <a name="step-4-populate-the-details-text-box"></a>Étape 4 : remplir la zone de texte Details


**S’applique à**: Access 2013 | Office 2013

## <a name="step-4-populate-the-details-text-box"></a>Étape 4 : remplir la zone de texte Details

**Pour remplir la zone de texte Details**

Créez une nouvelle sous-routine nommée recFields et insérez-y le code suivant :

```vb 
 
Sub recFields(r As Record, l As ListBox, t As TextBox) 
    Dim f As Field 
    Dim s As Stream 
    Set s = New Stream 
    Dim str As String 
     
    For Each f In r.Fields 
        l.AddItem f.Name & ": " & f.Value 
    Next 
    t.Text = "" 
    If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
        s.Open r, adModeRead, adOpenStreamFromRecord 
        str = s.ReadText(1) 
        s.Position = 0 
        If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
            s.Charset = "ascii" 
            s.Type = adTypeText 
        End If 
        t.Text = s.ReadText(adReadAll) 
    End If 
End Sub 
```

Ce code remplit lstDetails avec les champs et les valeurs de l'enregistrement simple transmis à recFields. Si la ressource est un fichier texte, un objet **Stream** de type texte est ouvert à partir de l'enregistrement de la ressource. Le code détermine si le jeu de caractères est de type ASCII et copie le contenu de l'objet **Stream** dans txtDetails.

