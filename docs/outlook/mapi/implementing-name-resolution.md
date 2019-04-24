---
title: Implémentation de la résolution de noms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 15c1d502947865c02973f4950b6b6fa8109b8e78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310079"
---
# <a name="implementing-name-resolution"></a>Implémentation de la résolution de noms

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnets d'adresses sont responsables de la prise en charge de la résolution de noms (processus d'association d'un identificateur d'entrée à un nom d'affichage). Les clients commencent la résolution de noms lorsqu'ils appellent [IAddrBook:: ResolveName](iaddrbook-resolvename.md) pour s'assurer que chaque membre de la liste des destinataires d'un message sortant correspond à une adresse valide. 
  
Votre fournisseur peut prendre en charge la résolution de noms de la façon suivante:
  
- Prenant en charge la restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)), une condition requise pour tous les conteneurs de carnet d'adresses.
    
- Implémentation de la méthode [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) , une option pour tous les conteneurs de carnet d'adresses. 
    
Si vous choisissez de prendre en charge **IABContainer:: ResolveNames**, essayez de localiser une correspondance exacte pour chaque nom d'affichage non résolu dans la structure [ADRLIST](adrlist.md) passée avec le paramètre _lpAdrList_ . Vous pouvez identifier un nom complet non résolu, car la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) est manquante dans le tableau de valeurs de propriété dans son membre **aEntries** de la structure **ADRLIST** . Ignorez les entrées auxquelles aucune propriété n'est associée. 
  
Signalez le résultat de votre tentative de résolution dans le paramètre _lpFlagList_ , un tableau d'indicateurs correspondant au tableau de noms d'affichage dans _lpAdrList_. Les indicateurs sont positionnels de sorte que le premier indicateur correspond au premier membre **aEntries** de la structure **ADRLIST** , le deuxième indicateur correspond au deuxième membre **aEntries** , et ainsi de suite. 
  
Il existe trois résultats possibles pour chaque entrée non résolue:
  
- Aucune correspondance n'a été trouvée, ce qui signifie qu'aucune des entrées de vos entrées de conteneur ne correspond à l'entrée dans la structure **ADRLIST** . Définissez l'entrée correspondante dans le paramètre _lpFlagList_ sur MAPI_UNRESOLVED. 
    
- Plusieurs correspondances peuvent être trouvées, ce qui signifie qu'il existe plusieurs entrées de conteneur qui correspondent à l'entrée dans la structure **ADRLIST** . Définissez l'entrée correspondante dans le paramètre _lpFlagList_ sur MAPI_AMBIGUOUS. Ne modifiez pas le nombre d'entrées dans la structure **ADRLIST** . 
    
- Une correspondance exacte est trouvée, ce qui signifie qu'il n'y a qu'une seule entrée de conteneur correspondant à l'entrée dans la structure **ADRLIST** . Définissez le membre correspondant dans le paramètre _lpFlagList_ sur MAPI_RESOLVED et ajoutez l'identificateur d'entrée au tableau de propriétés associé à l'entrée **ADRLIST** . 
    
Si vous choisissez de ne pas prendre en charge **IABContainer:: ResolveNames**, retournez MAPI_E_NO_SUPPORT à partir de votre implémentation.
  
Tous les fournisseurs de carnets d'adresses doivent prendre en charge une résolution de nom ambiguë (la restriction de propriété **PR_ANR** ) sur les tables de contenu de leurs conteneurs. Pour fournir cette prise en charge, gérez la restriction PR_ANR dans votre implémentation de la méthode [IMAPITable:: limiter](imapitable-restrict.md) en effectuant un type de recherche «meilleure estimation», correspondant à une ou plusieurs propriétés spécifiques qui ont de l'intérêt pour votre fournisseur. Vous pouvez choisir d'utiliser à chaque fois la même propriété ou les mêmes propriétés, par exemple **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), ou autoriser un administrateur à choisir dans une liste de propriétés acceptables. 
  
Bien que la plupart des fournisseurs fournissent leur propre implémentation de table de contenu, vous pouvez personnaliser l'implémentation fournie par MAPI via la fonction [CreateTable](createtable.md) . Toutefois, étant donné que l'implémentation MAPI ne prend pas en charge les restrictions d'aucune sorte, vous devez créer un objet de wrapper pour inclure une version personnalisée de la **limite** qui intercepte l'appel. 
  

