---
title: Boutons de navigation dans le Carnet d'adresses
TOCTitle: Address Book Navigation Buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0a6409bcdeca211c3badb1ca7918d3d34bc3f1f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869021"
---
# <a name="address-book-navigation-buttons"></a>Boutons de navigation dans le Carnet d'adresses


**S’applique à**: Access 2013, Office 2013

L’application Carnet d’adresses affiche les boutons de navigation au bas de la page Web. Vous pouvez utiliser ces boutons pour parcourir les données dans la grille HTML en sélectionnant la première ou la dernière ligne de données, ou les lignes adjacentes à la sélection actuelle.

## <a name="navigation-sub-procedures"></a>Sous-procédures de navigation

L'application Carnet d'adresses intègre plusieurs procédures qui permettent aux utilisateurs de parcourir les données en cliquant sur les boutons **Première**, **Suivante**, **Précédente** et **Dernière**.

Par exemple, le **premier** bouton permet d’activer le premier VBScript\_procédure OnClick Sub. Cette procédure exécute une méthode [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md), qui fait de la première ligne de données la sélection actuelle. En cliquant sur **le bouton** Active la dernière\_procédure OnClick Sub, qui appelle la méthode [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) , qui fait la dernière ligne de données la sélection actuelle. Les autres boutons de navigation fonctionnent de la même façon.

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

