---
title: Comparaison des entrées de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
ms.openlocfilehash: 63d188acae6f9557d0a81b03e7b273dd21775dfa
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374473"
---
# <a name="comparing-address-book-entries"></a>Comparaison des entrées de carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’implémentation [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) de votre fournisseur compare les identificateurs d’entrée pour deux des objets de votre fournisseur. MAPI appelle cette méthode après avoir déterminé que les deux identificateurs d’entrée contiennent le [MAPIUID](mapiuid.md) enregistré de votre fournisseur. Par conséquent, votre méthode **CompareEntryIDs** ne doit pas vérifier que les identificateurs d’entrée transmis pour les paramètres  _lpEntryID1_ et  _lpEntryID2_ appartiennent à votre fournisseur. 
  
Appeler **IABLogon::CompareEntryIDs** équivaut à récupérer la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) pour chacun des deux objets et à les comparer directement.
  
 **Pour implémenter CompareEntryIds**
  
1. Vérifiez le type des identificateurs d’entrée transmis si votre fournisseur stocke ces informations. Par exemple, un identificateur d’entrée peut appartenir à un utilisateur de messagerie, tandis que l’autre peut appartenir à une liste de distribution. Si les types ne correspondent pas, définissez le contenu du paramètre  _lpulResult_ sur FALSE et renvoyez. 
    
2. Comparez les tailles des deux identificateurs d’entrée. S’ils ne sont pas identiques, définissez le contenu du paramètre  _lpulResult_ sur FALSE et renvoyer. 
    
3. Vérifiez que la taille des identificateurs d’entrée est la taille correcte pour leur type. Si ce n’est pas le cas, définissez le contenu du paramètre  _lpulResult_ sur FALSE et renvoyez la valeur d’erreur MAPI_E_UNKNOWN_ENTRYID. 
    
4. Vérifiez si les identificateurs d’entrée sont identiques. S’ils sont comparés de manière égale, définissez le contenu du  _paramètre lpulResult_ sur TRUE et renvoyer. Sinon, définissez-la sur FALSE avant de la renvoyer. 
    
5. Si votre fournisseur compare un identificateur d’entrée à court terme à un identificateur à long terme, il doit comparer de la même manière.
    

