---
title: L’implémentation de la résolution de noms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4d55404149baca07a64b75d460bdfb2a8c541725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784182"
---
# <a name="implementing-name-resolution"></a>L’implémentation de la résolution de noms

  
  
**S’applique à**: Outlook 
  
Fournisseurs de carnet d’adresses sont responsables de la prise en charge de la résolution de noms, le processus d’association d’un identificateur d’entrée à un nom d’affichage. Clients initialisent la résolution de noms quand ils appellent [IAddrBook::ResolveName](iaddrbook-resolvename.md) pour s’assurer que chaque membre de la liste des destinataires d’un message sortant correspond à une adresse valide. 
  
Votre fournisseur peut prendre en charge la résolution de noms en :
  
- Prise en charge de la restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)), une demande pour tous les conteneurs de carnet d’adresses.
    
- L’implémentation de la méthode [IABContainer::ResolveNames](iabcontainer-resolvenames.md) , une option pour tous les conteneurs de carnet d’adresses. 
    
Si vous choisissez prendre en charge **IABContainer::ResolveNames**, essaie de rechercher une correspondance exacte pour chaque nom d’affichage non résolues dans la structure [ADRLIST](adrlist.md) passée avec le paramètre _lpAdrList_ . Vous pouvez identifier un nom d’affichage non résolues, car il manque la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) dans le tableau de valeurs de propriété dans ses membres **aEntries** de la structure **ADRLIST** . Ignorer les entrées qui ont zéro propriétés associées. 
  
Signaler le résultat de votre tentative de résolution dans le paramètre _lpFlagList_ , un tableau d’indicateurs qui correspond au tableau de noms d’affichage dans _lpAdrList_. Les indicateurs sont positionnels telles que le premier indicateur correspond au premier membre de la structure **ADRLIST** **aEntries** , le deuxième drapeau correspond à la deuxième membre **aEntries** et ainsi de suite. 
  
Il existe trois résultats possibles pour chaque entrée non résolue :
  
- Aucune correspondance n’a été trouvé, ce qui signifie qu’aucune des entrées dans vos entrées de conteneur correspondent à l’entrée dans la structure **ADRLIST** . Définissez l’entrée correspondante dans le paramètre _lpFlagList_ pour MAPI_UNRESOLVED. 
    
- Se trouve plusieurs correspondances, ce qui signifie qu’il n’y a plusieurs entrées de conteneur qui correspondent à l’entrée dans la structure **ADRLIST** . Définissez l’entrée correspondante dans le paramètre _lpFlagList_ pour MAPI_AMBIGUOUS. Ne modifiez pas le nombre d’entrées dans la structure **ADRLIST** . 
    
- Une correspondance exacte peut être trouvée, ce qui signifie qu’il existe une entrée d’un seul conteneur qui correspond à l’entrée dans la structure **ADRLIST** . Définir le membre correspondant dans le paramètre _lpFlagList_ pour MAPI_RESOLVED et ajoutez l’identificateur d’entrée dans le tableau des propriétés associées à l’entrée **ADRLIST** . 
    
Si vous choisissez de ne pas prendre en charge **IABContainer::ResolveNames**, renvoyer MAPI_E_NO_SUPPORT à partir de votre implémentation.
  
Tous les fournisseurs de carnet d’adresses sont requis pour prendre en charge la résolution de nom ambigu — la restriction de propriété **PR_ANR** — sur les tables des matières leurs conteneurs. Pour fournir cette prise en charge, gérer la restriction PR_ANR dans votre implémentation de [IMAPITable](imapitable-restrict.md) en effectuant un type de recherche, en correspondance avec une ou plusieurs propriétés particuliers que pertinent pour votre fournisseur de « deviner mieux ». Vous pouvez choisir d’utiliser les propriétés même à chaque fois, par exemple **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), ou permettre à un administrateur de choisir parmi une liste de propriétés acceptables. 
  
Bien que la plupart des fournisseurs de fournissent leur propre implémentation de table de contenu, vous pouvez personnaliser l’implémentation fournie par MAPI par le biais de la fonction [Create table](createtable.md) . Toutefois, étant donné que l’implémentation MAPI ne prend pas en charge restrictions de n’importe quel type, vous devez créer un objet de wrapper pour inclure une version personnalisée de **restreindre** qui intercepte l’appel. 
  

