---
title: Comparaison d’entrées de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e5c46aed7a15ae4f48c8e4f1fe308fcb20ab3fe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575356"
---
# <a name="comparing-address-book-entries"></a>Comparaison d’entrées de carnet d’adresses

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Implémentation de votre fournisseur [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) compare les identificateurs d’entrée de deux des objets de votre fournisseur. MAPI appelle cette méthode après que détermination que les identificateurs de deux entrée contenant votre fournisseur inscrit [MAPIUID](mapiuid.md). Par conséquent, votre méthode **CompareEntryIDs** doit vérifier pas que les identificateurs d’entrée passés pour les paramètres _lpEntryID1_ et _lpEntryID2_ appartiennent à votre fournisseur. 
  
**IABLogon::CompareEntryIDs** équivaut à la récupération de la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) pour chacun des deux objets et en les comparant directement.
  
 **Pour implémenter CompareEntryIds**
  
1. Vérifier le type des identificateurs d’entrée passé si votre fournisseur enregistre ces informations. Par exemple, un identificateur d’entrée peut appartenir à un utilisateur de messagerie pendant que l’autre peut appartenir à une liste de distribution. Si les types ne correspondent pas, le contenu du paramètre _lpulResult_ la valeur FALSE et retour. 
    
2. Comparer les tailles des identificateurs de deux entrée. Si elles ne sont pas les mêmes, définir le contenu du paramètre _lpulResult_ à FALSE et à renvoyer. 
    
3. Vérifiez que la taille des identificateurs d’entrée est la taille adéquate pour leur type. Si ce n’est pas le cas, le contenu du paramètre _lpulResult_ la valeur False et renvoyer la valeur d’erreur MAPI_E_UNKNOWN_ENTRYID. 
    
4. Vérifiez si les identificateurs d’entrée sont les mêmes. Si elles comparent également, définissez le contenu du paramètre _lpulResult_ sur TRUE et retour. Sinon, valeur FALSE avant de retourner. 
    
5. Si votre fournisseur compare un identificateur d’entrée à court terme avec un identificateur à long terme, ils doivent également comparer.
    

