---
title: Comparaison des entrées de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1a4a06a76ec9bb7d46de9d13d42cfca00c2c353b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571996"
---
# <a name="comparing-address-book-entries"></a>Comparaison des entrées de carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’implémentation [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) de votre fournisseur compare les identificateurs d’entrée pour deux des objets de votre fournisseur. MAPI appelle cette méthode après avoir déterminé que les deux identificateurs d’entrée contiennent le [MAPIUID](mapiuid.md)enregistré de votre fournisseur. Par conséquent, votre méthode **CompareEntryIDs n’a** pas besoin de vérifier que les identificateurs d’entrée transmis pour les paramètres  _lpEntryID1_ et  _lpEntryID2_ appartiennent à votre fournisseur. 
  
Appeler **IABLogon::CompareEntryIDs** équivaut à récupérer la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) pour chacun des deux objets et à les comparer directement.
  
 **Pour implémenter CompareEntryIds**
  
1. Vérifiez le type des identificateurs d’entrée transmis si votre fournisseur stocke ces informations. Par exemple, un identificateur d’entrée peut appartenir à un utilisateur de messagerie, tandis que l’autre peut appartenir à une liste de distribution. Si les types ne correspondent pas, définissez le contenu du paramètre  _lpulResult_ sur FALSE et renvoyez. 
    
2. Comparez les tailles des deux identificateurs d’entrée. S’ils ne sont pas identiques, définissez le contenu du paramètre  _lpulResult_ sur FALSE et renvoyer. 
    
3. Vérifiez que la taille des identificateurs d’entrée est la taille correcte pour leur type. Si ce n’est pas le cas, définissez le contenu du paramètre  _lpulResult_ sur FALSE et renvoyez la valeur d’erreur MAPI_E_UNKNOWN_ENTRYID. 
    
4. Vérifiez si les identificateurs d’entrée sont identiques. S’ils sont comparés de manière égale, définissez le contenu du paramètre  _lpulResult_ sur TRUE et renvoyer. Sinon, définissez-la sur FALSE avant de la renvoyer. 
    
5. Si votre fournisseur compare un identificateur d’entrée à court terme à un identificateur à long terme, il doit comparer de la même manière.
    

