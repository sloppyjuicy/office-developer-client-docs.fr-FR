---
title: Ajout de plusieurs champs
TOCTitle: Adding multiple fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 41833d744ef94e50d011014401db6a48ef68a416
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590176"
---
# <a name="adding-multiple-fields"></a>Ajout de plusieurs champs

**S’applique à** : Access 2013, Office 2013

Il est parfois plus efficace de passer un tableau de champs et leurs valeurs correspondantes à la méthode **AddNew** au lieu de définir plusieurs fois **Value** pour chaque nouveau champ. Si l'argument *FieldList* est un tableau, l'argument *Values* doit également représenter un tableau comptant le même nombre de membres, sans quoi une erreur se produit. L'ordre des noms de champs doit correspondre à l'ordre des valeurs de champs dans chaque tableau. Le code suivant passe un tableau de champs et un tableau de valeurs à la méthode **AddNew**.

```vb 
 
'BeginAddNew2 
 Dim avarFldNames As Variant 
 Dim avarFldValues As Variant 
 
 avarFldNames = Array("CompanyName", "Phone") 
 avarFldValues = Array("Sample Shipper 2", "(931) 555-6334") 
 
 If objRs1.Supports(adAddNew) Then 
 objRs1.AddNew avarFldNames, avarFldValues 
 End If 
 
 'Re-establish a Connection and update 
 Set objRs1.ActiveConnection = GetNewConnection 
 objRs1.UpdateBatch 
'EndAddNew2 
```

