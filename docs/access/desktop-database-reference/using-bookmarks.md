---
title: Utilisation des signets (référence de base de données du bureau Access)
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76c8cc793c3956ea0db0f01c7b33ba5740118e42
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947734"
---
# <a name="using-bookmarks"></a>Utilisation des signets


**S’applique à**: Access 2013, Office 2013

Il est souvent utile de pouvoir revenir directement à un enregistrement spécifique après vous être déplacé dans l'objet **Recordset**, sans devoir faire défiler tous les enregistrements et comparer leurs valeurs. Si, par exemple, vous recherchez un enregistrement à l'aide de la méthode **Find** mais que la recherche ne renvoie aucun enregistrement, vous revenez automatiquement à l'une des deux extrémités de l'objet **Recordset**. Si votre fournisseur les prend en charge, des signets peuvent être utilisés pour marquer votre position avant d'utiliser la méthode **Find**, afin de pouvoir revenir à votre emplacement d'origine. Un signet est une valeur de type **Variant** qui permet l'identification individuelle des enregistrements dans un objet **Recordset**.

Vous pouvez également utiliser un tableau de signets de type Variant avec la méthode **Filter** de l'objet **Recordset** pour filtrer un jeu d'enregistrements sélectionné. Pour plus d'informations sur cette technique, consultez la section Filtrage des résultats dans la rubrique [Utilisation des jeux d'enregistrements](working-with-recordsets.md), plus loin dans ce chapitre.

Vous pouvez utiliser la propriété **Bookmark** afin d'obtenir un signet pour un enregistrement ou définir l'enregistrement actif d'un objet **Recordset** en tant qu'enregistrement identifié par un signet valide . Le code suivant utilise la propriété **Bookmark** pour définir un signet et revenir ensuite à l'enregistrement marqué par le signet, après avoir accédé à d'autres enregistrements. Pour déterminer si votre objet **Recordset** prend en charge les signets, utilisez la méthode **Supports**.

```vb 
 
'BeginBookmarkEg 
 Dim varBookmark As Variant 
 Dim blnCanBkmrk As Boolean 
 
 objRs.Open strSQL, strConnStr, adOpenStatic, adLockOptimistic, adCmdText 
 
 If objRs.RecordCount > 4 Then 
 objRs.Move 4 ' move to the fifth record 
 blnCanBkmrk = objRs.Supports(adBookmark) 
 If blnCanBkmrk = True Then 
 varBookmark = objRs.Bookmark ' record the bookmark 
 objRs.MoveLast ' move to a different record 
 objRs.Bookmark = varBookmark ' return to the bookmarked (sixth) record 
 End If 
 End If 
'EndBookmarkEg 
```

La méthode [Supports](supports-method-ado.md) sera décrite plus en détail ultérieurement.

À l'exception des objets **Recordset** clonés, les signets sont spécifiques à l'objet **Recordset** dans lequel ils ont été créés, même en cas d'utilisation de la même commande. En d'autres termes, vous ne pouvez pas utiliser un objet **Bookmark** provenant d'un objet **Recordset** donné pour accéder au même enregistrement dans un second objet **Recordset** ouvert avec la même commande.

