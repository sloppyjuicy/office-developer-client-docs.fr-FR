---
title: Mise en œuvre de la résolution de noms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 62370da7b5ae4eadffd1d55564d363de7ea6415d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567304"
---
# <a name="implementing-name-resolution"></a>Mise en œuvre de la résolution de noms

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnets d’adresses sont responsables de la prise en charge de la résolution de noms , c’est-à-dire le processus d’association d’un identificateur d’entrée à un nom complet. Les clients lancent la résolution de noms lorsqu’ils appellent [IAddrBook::ResolveName](iaddrbook-resolvename.md) pour s’assurer que chaque membre de la liste des destinataires d’un message sortant correspond à une adresse valide. 
  
Votre fournisseur peut prendre en charge la résolution de noms en :
  
- Prise en **charge PR_ANR** restriction de propriété ([PidTagAnr](pidtaganr-canonical-property.md)), une condition requise pour tous les conteneurs de carnet d’adresses.
    
- Mise en œuvre [de la méthode IABContainer::ResolveNames,](iabcontainer-resolvenames.md) une option pour tous les conteneurs de carnet d’adresses. 
    
Si vous choisissez de prendre en charge **IABContainer::ResolveNames,** essayez de rechercher une correspondance exacte pour chaque nom complet non résolu dans la structure [ADRLIST](adrlist.md) transmise avec le paramètre _lpAdrList._ Vous pouvez identifier un nom complet non résolu car il manque la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) dans le tableau de valeurs de propriété dans son membre **aEntries** de la structure **ADRLIST.** Ignorez les entrées qui ne sont associées à aucune propriété. 
  
Signalez le résultat de votre tentative de résolution dans le paramètre  _lpFlagList,_ un tableau d’indicateurs qui correspond au tableau de noms complets dans  _lpAdrList_. Les indicateurs sont positionnels de telle sorte que le premier indicateur corresponde au premier membre **aEntries** dans la structure **ADRLIST,** le deuxième indicateur correspond au deuxième membre **aEntries,** etc. 
  
Il existe trois résultats possibles pour chaque entrée non résolue :
  
- Aucune correspondance n’a été trouvée, ce qui signifie qu’aucune des entrées de votre conteneur ne correspond à l’entrée dans la structure **ADRLIST.** Définissez l’entrée correspondante dans  _le paramètre lpFlagList_ sur MAPI_UNRESOLVED. 
    
- Plusieurs correspondances sont trouvées, ce qui signifie qu’il existe plusieurs entrées de conteneur qui correspondent à l’entrée dans la structure **ADRLIST.** Définissez l’entrée correspondante dans  _le paramètre lpFlagList_ sur MAPI_AMBIGUOUS. Ne modifiez pas le nombre d’entrées dans la structure **ADRLIST.** 
    
- Une correspondance exacte est trouvée, ce qui signifie qu’il n’existe qu’une seule entrée de conteneur qui correspond à l’entrée dans la structure **ADRLIST.** Définissez le membre correspondant dans le paramètre _lpFlagList_ sur MAPI_RESOLVED et ajoutez l’identificateur d’entrée au tableau des propriétés associées à l’entrée **ADRLIST.** 
    
Si vous choisissez de ne pas prendre en charge **IABContainer::ResolveNames,** renvoyez MAPI_E_NO_SUPPORT à partir de votre implémentation.
  
Tous les fournisseurs de carnet d’adresses sont tenus de prendre en charge la résolution de noms **ambigus (restriction PR_ANR** propriété) sur les tables de contenu de leurs conteneurs. Pour fournir cette prise en charge, traitez la restriction PR_ANR dans votre implémentation [d’IMAPITable::Restrict](imapitable-restrict.md) en faisant une recherche de type « de meilleure estimation », en faisant la correspondance avec une ou plusieurs propriétés particulières qui sont logiques pour votre fournisseur. Vous pouvez choisir d’utiliser la même propriété ou propriété à chaque fois, par exemple **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), ou autoriser un administrateur à choisir parmi une liste de propriétés acceptables. 
  
Bien que la plupart des fournisseurs fournissent leur propre implémentation de table des matières, vous pouvez personnaliser l’implémentation fournie par MAPI via [la fonction CreateTable.](createtable.md) Toutefois, étant donné que l’implémentation MAPI ne prend en charge aucune restriction, vous devez créer un objet wrapper pour inclure une version personnalisée de **Restrict** qui intercepte l’appel. 
  

