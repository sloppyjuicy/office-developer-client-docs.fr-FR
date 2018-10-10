---
title: Ajout de plusieurs champs
TOCTitle: Adding Multiple Fields
ms:assetid: 81b2f9de-4805-4494-9990-09ffda1b2068
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249560(v=office.15)
ms:contentKeyID: 48545961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9bca4035917f4376ccf69201d79894a0273ceb9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471123"
---
# <a name="adding-multiple-fields"></a>Ajout de plusieurs champs


**S’applique à**: Access 2013 | Office 2013

Il est parfois plus efficace de passer un tableau de champs et leurs valeurs correspondantes à la méthode **AddNew** au lieu de définir plusieurs fois **Value** pour chaque nouveau champ. Si *FieldList* est un tableau, les *valeurs* doivent être également un tableau avec le même nombre de membres ; dans le cas contraire, une erreur se produit. L'ordre des noms de champs doit correspondre à l'ordre des valeurs de champs dans chaque tableau. Le code suivant passe un tableau de champs et un tableau de valeurs à la méthode **AddNew**.

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

