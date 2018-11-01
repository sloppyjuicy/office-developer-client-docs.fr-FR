---
title: Transformation (référence du bureau de la base de données Access)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a051c62d73a36fed0832f17b1cb53b1641d4a152
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889279"
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
> <P>[!REMARQUE] Vous ne pouvez pas ajouter de colonnes à un objet <STRONG>Recordset</STRONG> existant, ni modifier la mise en forme d'un objet <STRONG>Recordset</STRONG> paramétré ou des objets <STRONG>Recordset</STRONG> spécifiés dans une clause COMPUTE intermédiaire, ni exécuter des opérations d'agrégation sur un objet <STRONG>Recordset</STRONG> descendant de l'objet <STRONG>Recordset</STRONG> dont la mise en forme a été modifiée. L'objet <STRONG>Recordset</STRONG> visé par l'opération de modification de la mise en forme et la nouvelle commande de mise en forme doivent tous deux utiliser le même objet <A href="connection-object-ado.md">Connection</A>.</P>


