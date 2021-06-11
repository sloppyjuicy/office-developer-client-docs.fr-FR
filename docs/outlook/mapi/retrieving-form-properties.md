---
title: Récupération des propriétés du formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 023d2cf312438b1e4b6a90c57e1ead7d606d7727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412918"
---
# <a name="retrieving-form-properties"></a>Récupération des propriétés du formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour émettre une requête significative pour un type de message personnalisé, une application doit connaître les propriétés attendues sur ce message. Pour obtenir la liste des propriétés qu’une classe de message personnalisée utilise, une application cliente interroge le gestionnaire de formulaire MAPI. Le gestionnaire de formulaires obtient ces informations à partir du fichier de configuration de formulaire approprié afin que les applications clientes peuvent utiliser ces informations sans la surcharge d’activation du serveur de formulaires lui-même. Pour ce faire, l’application cliente appelle la méthode [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) comme suit : 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Notez que le troisième argument de **ResolveMessageClass** est le dossier qui contient la table des matières associée que la requête recherchera pour les serveurs de formulaires. NULL indique que le gestionnaire de formulaire doit effectuer une recherche dans tous les conteneurs de formulaires disponibles. Si la requête doit s’exécuter sur un dossier particulier, il est préférable d’inclure le pointeur [IMAPIFolder](imapifolderimapicontainer.md) approprié à la place. 
  
## <a name="see-also"></a>Voir aussi



[Interactions avec le serveur de formulaires](form-server-interactions.md)

