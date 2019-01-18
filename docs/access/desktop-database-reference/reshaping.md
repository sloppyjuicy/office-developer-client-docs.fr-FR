---
title: Transformation (référence du bureau de la base de données Access)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c820e82669789d7c3806cc1fd38a2eb6844b722e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711901"
---
# <a name="reshaping"></a>Remise en forme

**S’applique à**: Access 2013, Office 2013

Un objet **Recordset** créé par une clause d’une commande de mise en forme peut recevoir un *alias* (généralement assorti du mot-clé AS). L’alias d’un objet **Recordset** mis en forme peut être référencé dans une commande totalement différente. En d’autres termes, vous pouvez réutiliser, c’est-à-dire *modifier la mise en forme* d’un objet **Recordset** préalablement mis en forme dans une nouvelle commande de mise en forme. Pour prendre en charge cette fonctionnalité, ADO propose une propriété nommée [Reshape Name](reshape-name-property-dynamic-ado.md).

La fonctionnalité de modification de la mise en forme s'avère utile dans deux cas. En premier lieu, elle permet d'associer un objet **Recordset** existant à un nouvel objet **Recordset** parent.

## <a name="example"></a>Exemple

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

La deuxième fonction consiste à activer l’accès non hiérarchisé aux objets **Recordset** enfants existants, à l’aide de la syntaxe `"SHAPE <recordset reshape name>"`.

> [!NOTE]
> [!REMARQUE] Vous ne pouvez pas ajouter de colonnes à un objet **Recordset** existant, ni modifier la mise en forme d'un objet **Recordset** paramétré ou des objets **Recordset** spécifiés dans une clause COMPUTE intermédiaire, ni exécuter des opérations d'agrégation sur un objet **Recordset** descendant de l'objet **Recordset** dont la mise en forme a été modifiée. Le **jeu d’enregistrements** en cours remodelée et la nouvelle forme commande doivent tous deux utiliser le même ** objet[Connection](connection-object-ado.md) .


