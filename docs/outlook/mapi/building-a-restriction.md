---
title: Création d’une restriction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 38182abd922cd5806a14b6541c22ce675b997387
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318258"
---
# <a name="building-a-restriction"></a>Création d’une restriction

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour créer une restriction, une application cliente crée une hiérarchie d'une ou plusieurs structures de restriction de différents types et transmet un pointeur vers la hiérarchie à la méthode [IMAPITable](imapitable-restrict.md) :: restrict ou [IMAPITable:: FindRow](imapitable-findrow.md) . L'illustration qui suit et l'exemple de code dans l' [exemple de code de restriction](sample-restriction-code.md) montrent comment une restriction standard est implémentée avec des structures de restriction liées de types différents. 

Dans cet exemple, un utilisateur d'une application client essaie de trouver tous les messages qui contiennent le mot «Volleyball» dans la ligne d'objet et qui ont été envoyés à Sue à partir de Sam. Tout d'abord, une structure [SRestriction](srestriction.md) générique est allouée. Cette structure devient la base des autres appels à la fonction [MAPIAllocateMore](mapiallocatemore.md) pour créer des structures [SRestriction](srestriction.md) et [SPropValue](spropvalue.md) liées, qui peuvent être libérées par un seul appel à [MAPIFreeBuffer](mapifreebuffer.md). Étant donné que les critères à appliquer à l'ensemble de messages se comportent en trois parties, la structure de restriction de niveau supérieur est une restriction **et** . Le membre **cRes** de la structure [SAndRestriction](sandrestriction.md) est défini sur 3 pour indiquer les trois restrictions à évaluer et son membre **lpRes** est défini sur un tableau de trois membres de structures **SRestriction** . 
  
Pour rechercher des messages envoyés à un destinataire particulier, il est nécessaire d'effectuer une recherche dans la table de destinataires pour chaque message, plutôt que dans le message lui-même. Une restriction de sous-objet est utilisée pour effectuer la recherche dans la table de destinataires. Par conséquent, le premier membre du tableau pointe vers une structure [SSubRestriction](ssubrestriction.md) dont le membre **ulSubObject** est défini sur **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Ensuite, pour spécifier les éléments à rechercher dans la table des destinataires, une restriction de contenu est utilisée. 
  
Les deuxième et troisième membres du tableau sont plus simples. Elles pointent toutes deux vers des structures de restriction de contenu, une pour rechercher des messages dont la propriété **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) est définie sur «Sam» et une autre dont la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) a la valeur « volleyball. "
  
**Implémentation de restriction**
  
![Implémentation de restriction] (media/amapi_61.gif "Implémentation de restriction")
  
## <a name="see-also"></a>Voir aussi

- [Tables MAPI](mapi-tables.md)

