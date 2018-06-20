---
title: Récupération des propriétés de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 334ecaacec88c3730f4cc2f4c80eb35d5a553c4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787024"
---
# <a name="retrieving-form-properties"></a>Récupération des propriétés de formulaire

  
  
**S’applique à**: Outlook 
  
Pour émettre une requête qui est explicite à un type de message personnalisé, une application a besoin de connaître les propriétés attendu sur ce message. Pour obtenir une liste des propriétés qui utilise une classe de message personnalisée, une application cliente interroge le Gestionnaire de formulaire MAPI. Le Gestionnaire de formulaire obtient ces informations à partir du fichier de configuration de formulaire adéquat afin que les applications clientes peuvent utiliser ces informations sans la surcharge d’activation du serveur du formulaire lui-même. Pour ce faire, l’application cliente appelle la méthode [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) comme suit : 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Notez que le troisième argument de **ResolveMessageClass** est le dossier qui contient la table de contenu associé à la requête de recherche pour les serveurs du formulaire. NULL indique que le Gestionnaire de formulaire doit rechercher tous les conteneurs de formulaires disponibles. Si la requête doit s’exécuter par rapport à un dossier particulier, il est préférable d’inclure le pointeur [IMAPIFolder](imapifolderimapicontainer.md) approprié à la place. 
  
## <a name="see-also"></a>Voir aussi



[Formulaire serveur Interactions](form-server-interactions.md)

