---
title: Récupération des propriétés de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a6636b6298fcf565a297ed5df8a885c43c279c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583847"
---
# <a name="retrieving-form-properties"></a>Récupération des propriétés de formulaires

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour émettre une requête qui est explicite à un type de message personnalisé, une application a besoin de connaître les propriétés attendu sur ce message. Pour obtenir une liste des propriétés qui utilise une classe de message personnalisée, une application cliente interroge le Gestionnaire de formulaire MAPI. Le Gestionnaire de formulaire obtient ces informations à partir du fichier de configuration de formulaire adéquat afin que les applications clientes peuvent utiliser ces informations sans la surcharge d’activation du serveur du formulaire lui-même. Pour ce faire, l’application cliente appelle la méthode [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) comme suit : 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Notez que le troisième argument de **ResolveMessageClass** est le dossier qui contient la table de contenu associé à la requête de recherche pour les serveurs du formulaire. NULL indique que le Gestionnaire de formulaire doit rechercher tous les conteneurs de formulaires disponibles. Si la requête doit s’exécuter par rapport à un dossier particulier, il est préférable d’inclure le pointeur [IMAPIFolder](imapifolderimapicontainer.md) approprié à la place. 
  
## <a name="see-also"></a>Voir aussi



[Interactions avec le serveur de formulaire](form-server-interactions.md)

