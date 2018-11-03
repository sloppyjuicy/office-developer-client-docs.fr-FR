---
title: Gérer les mises à jour échouées
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 659b5389074371ed4de41b909ab5228ad8fca080
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947748"
---
# <a name="dealing-with-failed-updates"></a>Gérer les mises à jour échouées

**S’applique à**: Access 2013, Office 2013

## <a name="dealing-with-failed-updates"></a>Traitement des échecs de mise à jour

Lorsqu'une mise à jour se solde par un échec, la résolution des erreurs dépend de leur nature, de leur sévérité et de la logique de votre application. Toutefois, si la base de données est partagée avec d'autres utilisateurs, une erreur commune consiste à ce qu'une autre personne modifie le champ avant vous. Ce type d'erreur est appelé un *conflit*. ADO détecte cette situation et signale une erreur.

Si des erreurs de mise à jour surviennent, elles sont dirigées dans un programme de gestion des erreurs. Pour que seules les lignes présentant des conflits soient visibles, filtrez le **jeu d'enregistrements** avec la constante **adFilterConflictingRecords**. Dans cet exemple, la stratégie de résolution des erreurs consiste tout simplement à imprimer l’auteur du premier et du prénom (**au\_fname** et **au\_lname**).

Le code permettant d'alerter l'utilisateur du conflit de mise à jour ressemble à ceci :

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

