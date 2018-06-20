---
title: Création d’une restriction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3b40c8433f93237db2ae4fd5449fe8a0da486539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782991"
---
# <a name="building-a-restriction"></a>Création d’une restriction

**S’applique à**: Outlook 
  
Pour créer une restriction, une application cliente crée une hiérarchie d’une ou plusieurs des structures de restriction de différents types et passe un pointeur vers la hiérarchie à la méthode [IMAPITable](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md) . L’illustration suivante et l’exemple de code dans [l’Exemple de Code Restriction](sample-restriction-code.md) montrent comment une restriction classique est implémentée avec les structures de lié restriction de différents types. 

Dans cet exemple, un utilisateur d’une application cliente essaie de trouver tous les messages qui contiennent le mot « volleyball » dans la ligne d’objet et ont été envoyés à Marie de Sam. Tout d’abord, une structure [SRestriction](srestriction.md) générique est allouée. Cette structure devient la base pour les autres appels à la fonction [MAPIAllocateMore](mapiallocatemore.md) créer des structures [SRestriction](srestriction.md) et [SPropValue](spropvalue.md) liés qui peuvent être libérés avec un seul appel à [MAPIFreeBuffer](mapifreebuffer.md). Étant donné que les critères à appliquer à l’ensemble des messages est en trois parties, restriction **et** est la structure de restriction de niveau supérieur. Le [SAndRestriction](sandrestriction.md) membre la structure **cRes** est défini à 3 pour indiquer les trois restrictions pour évaluer et ses membres **lpRes** est défini sur un tableau de trois membres de structures **SRestriction** . 
  
Pour rechercher les messages envoyés à un destinataire particulier, il est nécessaire rechercher la table de destinataires pour chaque message, plutôt que le message lui-même. Une restriction sous-objet est utilisée pour effectuer une recherche de la table des destinataires. Par conséquent, le premier membre de la pointe de tableau vers une structure [SSubRestriction](ssubrestriction.md) avec son membre **ulSubObject** défini à **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Ensuite, pour spécifier les éléments à rechercher dans la table de destinataires, une restriction de contenu est utilisée. 
  
Les deuxième et troisième membres du tableau sont plus simples. Ils permettent tous deux pointent aux structures de restriction de contenu, un pour rechercher des messages dont la propriété **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) la valeur « Sam » et une autre qui possède une propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) » volleyball. »
  
**Implémentation de restriction**
  
![Implémentation de restriction] (media/amapi_61.gif "Implémentation de restriction")
  
## <a name="see-also"></a>Voir aussi

- [Tables MAPI](mapi-tables.md)

