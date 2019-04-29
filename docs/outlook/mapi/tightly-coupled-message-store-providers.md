---
title: Fournisseurs de banques de messages étroitement couplés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3c9996dad1e9aa8c291f1cd593d9651994d86141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413226"
---
# <a name="tightly-coupled-message-store-providers"></a>Fournisseurs de banques de messages étroitement couplés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de banques de messages peuvent être étroitement couplés à un fournisseur de transport. Le couplage étroit des fournisseurs de services MAPI implique l'implémentation des deux fournisseurs de sorte que le fournisseur de transport et le fournisseur de transport puissent communiquer pour que le processus d'envoi et de réception des messages soit plus efficace. L'avantage de cette opération est que les améliorations de performances peuvent survenir lorsque deux fournisseurs de services peuvent interagir les uns avec les autres directement au lieu d'utiliser le spouleur MAPI. Pour associer étroitement un fournisseur de banque de messages à un fournisseur de transport, le fournisseur de transport doit placer l'identificateur d'entrée du fournisseur de banque de messages dans la propriété **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) du fournisseur de transport. ligne dans la table d'État MAPI. Cela permet au spouleur MAPI de connecter le fournisseur de banque au fournisseur de transport.
  
Il n'est pas nécessaire qu'un fournisseur de banque de messages soit étroitement couplé avec tout autre fournisseur de services. Le fournisseur de services le plus courant à associer étroitement avec un fournisseur de banque de messages est un fournisseur de transport. Cette opération est généralement effectuée pour permettre l'envoi et la réception de messages sans impliquer le spouleur MAPI. Par exemple, lorsque l'utilisateur envoie un message sortant, le fournisseur de banque de messages combiné et le fournisseur de transport peuvent l'envoyer directement. Les fournisseurs de services combinés n'ont pas besoin de commencer par informer le spouleur MAPI qu'il y a un nouveau message à traiter, puis d'attendre le spouleur MAPI pour lancer le processus de transfert du message à partir du fournisseur de banque de messages vers le fournisseur de transport. Cela présente des avantages particuliers lorsqu'une banque de messages basée sur un serveur est utilisée en minimisant le trafic réseau entre l'ordinateur de l'utilisateur et le serveur.
  
En règle générale, il n'existe pas de procédures bien spécifiées pour le couplage étroit des fournisseurs de services. Toutefois, vous devez utiliser les instructions suivantes:
  
- Si la raison de l'association étroite des fournisseurs de services est des performances, sachez que le couplage prend des parties du sous-système MAPI en dehors des processus dans lesquels ces composants seraient normalement impliqués. Cela signifie que les composants individuels du fournisseur de services combinés doivent interagir les uns avec les autres de manière à simuler l'interaction avec les composants du sous-système MAPI qui ne sont pas utilisés.
    
- Lorsque des fournisseurs de services étroitement couplés interagissent avec d'autres composants MAPI, ils doivent toujours interagir avec eux exactement comme ils le ferait s'ils ne sont pas étroitement couplés. Par exemple, si un utilisateur utilise un fournisseur de banque de messages et un fournisseur de transport combinés comme banque de messages par défaut, mais utilise un fournisseur de transport distinct pour envoyer des messages, comme cela peut se produire lorsqu'un utilisateur prend un ordinateur en déplacement et bascule vers un RP de transport distant ovider — la partie de la Banque de messages du fournisseur de services étroitement couplé doit toujours interagir avec le spouleur MAPI, comme s'il s'agissait d'un fournisseur de banque de messages autonome.
    
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

