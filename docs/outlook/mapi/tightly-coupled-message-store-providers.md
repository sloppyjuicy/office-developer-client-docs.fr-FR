---
title: Fournisseurs de magasins de messages étroitement couplés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e9052228da750316c68f65d2489549d560ec0cc5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578514"
---
# <a name="tightly-coupled-message-store-providers"></a>Fournisseurs de magasins de messages étroitement couplés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de magasins de messages peuvent être étroitement associés à un fournisseur de transport. Un couplage étroit des fournisseurs de services MAPI implique l’implémentation des deux fournisseurs afin que le fournisseur de magasins et le fournisseur de transport communiquent pour rendre le processus d’envoi et de réception de messages plus efficace. L’avantage de cette fonction est que des améliorations des performances peuvent se faire lorsque deux fournisseurs de services peuvent interagir directement entre eux plutôt qu’au moyen dupooler MAPI. Pour coupler étroitement un fournisseur de magasins de messages à un fournisseur de transport, le fournisseur de transport doit placer l’identificateur d’entrée du fournisseur de magasins de messages dans la propriété **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) dans la ligne du fournisseur de transport dans la table d’état MAPI. Cela permet aupooler MAPI de connecter le fournisseur de magasin au fournisseur de transport.
  
Il n’est pas obligatoire qu’un fournisseur de magasin de messages soit étroitement associé à un autre fournisseur de services. Le fournisseur de services le plus courant à coupler étroitement avec un fournisseur de magasins de messages est un fournisseur de transport. Cela permet généralement d’envoyer et de recevoir des messages sans impliquer lepooler MAPI. Par exemple, lorsque l’utilisateur envoie un message sortant, le fournisseur de magasins de messages combiné et le fournisseur de transport peuvent l’envoyer directement. Les fournisseurs de services combinés n’ont pas besoin d’informer d’abord lepooler MAPI qu’un nouveau message doit être traiter, puis d’attendre que lepooler MAPI lance le processus de transfert du message du fournisseur de magasins de messages au fournisseur de transport. Cela présente des avantages particuliers lorsqu’une boutique de messages basée sur un serveur est utilisée en réduisant le trafic réseau entre l’ordinateur de l’utilisateur et le serveur.
  
En règle générale, il n’existe aucune procédure bien spécifiée pour l’couplage étroit des fournisseurs de services. Toutefois, vous devez utiliser les instructions suivantes :
  
- Si la raison d’un couplage étroit des fournisseurs de services est la performance, sachez que le couplage fait sortir des parties du sous-système MAPI des processus qui impliquent normalement ces composants. Cela implique que les parties individuelles du fournisseur de services combinés doivent interagir les unes avec les autres de manière à simuler l’interaction normale qu’elles auraient avec les parties du sous-système MAPI qui ne sont pas utilisées.
    
- Lorsque des fournisseurs de services étroitement couplés interagissent avec d’autres composants MAPI, ils doivent toujours interagir avec eux exactement comme ils le feraient s’ils n’étaient pas étroitement associés. Par exemple, si un utilisateur utilise un fournisseur de magasins de messages et un fournisseur de transport combinés comme magasin de messages par défaut, mais utilise un fournisseur de transport distinct pour envoyer des messages, comme cela peut se produire lorsqu’un utilisateur prend un ordinateur sur la route et bascule vers un fournisseur de transport distant, la partie de la boutique de messages du fournisseur de services étroitement couplé doit toujours interagir avec lepooler MAPI comme s’il s’agit d’un fournisseur de magasin de messages autonome.
    
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

