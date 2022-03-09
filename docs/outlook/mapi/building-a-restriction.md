---
title: Création d’une restriction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
ms.openlocfilehash: e70f8bed54c330795feaba99551699e86ddc4594
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381291"
---
# <a name="building-a-restriction"></a>Création d’une restriction

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour créer une restriction, une application cliente crée une hiérarchie d’une ou plusieurs structures de restriction de différents types et transmet un pointeur vers la hiérarchie vers la méthode [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md) . L’illustration qui suit et l’exemple [](sample-restriction-code.md) de code de l’exemple de code de restriction montrent comment une restriction type est implémentée avec des structures de restriction liées de différents types. 

Dans cet exemple, un utilisateur d’une application cliente tente de trouver tous les messages qui contiennent le mot « domaine » dans la ligne d’objet et qui ont été envoyés à Sue à partir de Sam. Tout d’abord, une structure [SRestriction générique](srestriction.md) est allouée. Cette structure devient la base d’autres appels à la fonction [MAPIAllocateMore](mapiallocatemore.md) pour créer des structures [SRestriction](srestriction.md) et [SPropValue](spropvalue.md) liées qui peuvent être libérées en un seul appel à [MAPIFreeBuffer](mapifreebuffer.md). Étant donné que les critères à appliquer à l’ensemble de messages sont en trois parties, la structure de restriction de niveau supérieur est une restriction **AND** . Le membre **cRes** de la structure [SAndRestriction](sandrestriction.md) est définie sur 3 pour indiquer les trois restrictions à évaluer et son membre **lpRes** sur un tableau de trois membres de structures **SRestriction**. 
  
Pour rechercher des messages envoyés à un destinataire particulier, il est nécessaire de rechercher chaque message dans la table des destinataires plutôt que le message lui-même. Une restriction de sous-objet est utilisée pour effectuer la recherche dans la table des destinataires. Par conséquent, le premier membre du tableau pointe vers une structure [SSubRestriction](ssubrestriction.md) dont le membre **ulSubObject** est **PR_MESSAGE_RECIPIENTS (**[PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Ensuite, pour spécifier ce qu’il faut rechercher dans la table des destinataires, une restriction de contenu est utilisée. 
  
Les deuxième et troisième membres du tableau sont plus simples. Elles pointent toutes les deux vers des structures de restriction de contenu, l’une pour rechercher les messages dont la propriété **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) a la valeur « Sam » et l’autre qui a une propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) définie sur « domaine ».
  
**Implémentation de restriction**
  
![Implémentation de restriction](media/amapi_61.gif "Implémentation de restriction")
  
## <a name="see-also"></a>Voir aussi

- [MAPI Tables](mapi-tables.md)

