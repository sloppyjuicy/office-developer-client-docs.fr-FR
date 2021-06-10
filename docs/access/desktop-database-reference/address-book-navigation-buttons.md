---
title: Boutons de navigation de Carnet d’adresses
TOCTitle: Address Book navigation buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7c87acd433df4a303c1e6a15a60184cadf994c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282463"
---
# <a name="address-book-navigation-buttons"></a>Boutons de navigation de Carnet d’adresses

**S’applique à** : Access 2013, Office 2013

L’application carnet d’adresses affiche les boutons de navigation en bas de la page web. Vous pouvez utiliser ces boutons pour parcourir les données dans la grille HTML en sélectionnant la première ou la dernière ligne de données, ou les lignes adjacentes à la sélection actuelle.

## <a name="navigation-sub-procedures"></a>Sous-procédures de navigation

L'application Carnet d'adresses intègre plusieurs procédures qui permettent aux utilisateurs de parcourir les données en cliquant sur les boutons **Première**, **Suivante**, **Précédente** et **Dernière**.

Par exemple, le fait de cliquer sur **le premier** bouton active la procédure VBScript First \_ OnClick Sub. Cette procédure exécute une méthode [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md), qui fait de la première ligne de données la sélection actuelle. Le fait de cliquer **sur** le bouton Dernier active la procédure Last OnClick Sub, qui appelle la méthode \_ [MoveLast,](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) faisant de la dernière ligne de données la sélection actuelle. Les autres boutons de navigation fonctionnent de la même façon.

```vb 
 
' Move to the first record in the bound Recordset. 
Sub First_OnClick 
 DC1.Recordset.MoveFirst 
End Sub 
 
' Move to the next record from the current position 
' in the bound Recordset. 
Sub Next_OnClick 
 If Not DC1.Recordset.EOF Then ' Cannot move beyond bottom record. 
 DC1.Recordset.MoveNext 
 Exit Sub 
 End If 
End Sub 
 
' Move to the previous record from the current position in the bound 
' Recordset. 
Sub Prev_OnClick 
 If Not DC1.Recordset.BOF Then ' Cannot move beyond top record. 
 DC1.Recordset.MovePrevious 
 Exit Sub 
 End If 
End Sub 
 
' Move to the last record in the bound Recordset. 
Sub Last_OnClick 
 DC1.Recordset.MoveLast 
End Sub 
```

