---
title: Fournisseurs de banque de messages étroitement couplés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 83ebb739302ca0e12604b9eaf854f273554826ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787347"
---
# <a name="tightly-coupled-message-store-providers"></a>Fournisseurs de banque de messages étroitement couplés

  
  
**S’applique à**: Outlook 
  
Fournisseurs de magasins de message peuvent être étroitement avec un fournisseur de transport. Associant étroitement les moyens de fournisseurs de service MAPI implémenter les deux fournisseurs tels que le fournisseur de magasin et le fournisseur de transport peuvent communiquer pour faciliter le processus d’envoi et réception de messages plus efficaces. L’avantage de cette approche est qu’améliorations des performances peuvent se produire lorsque deux fournisseurs de services peuvent interagir les uns avec les autres directement plutôt que prenait spouleur MAPI. Pour associer étroitement un fournisseur de banque de messages à un fournisseur de transport, le fournisseur de transport doit placer l’identificateur d’entrée du fournisseur de banque de messages dans la propriété **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) dans du fournisseur transport ligne dans la table d’état MAPI. Cela permet de spouleur MAPI pour se connecter au fournisseur de magasin pour le fournisseur de transport.
  
Il n’est pas nécessaire qu’un fournisseur de magasins message jamais être étroitement avec n’importe quel autre fournisseur de services. Le fournisseur de services les plus courants pour coupler étroitement avec un fournisseur de banque de messages est un fournisseur de transport. Cette opération est généralement effectuée afin que l’envoi et réception de messages peut être effectué sans impliquant le spouleur MAPI. Par exemple, lorsque l’utilisateur envoie un message sortant, le fournisseur de magasin combinée de message et le fournisseur de transport peuvent envoyer directement. Les fournisseurs de services combiné n’ont pas tout d’abord notification spouleur MAPI qu’il existe un nouveau message pour traiter et attendez spouleur MAPI lancer le processus de transfert du message à partir du fournisseur de magasin de message pour le fournisseur de transport. Cela présente des avantages particulières lorsqu’une banque de messages sur le serveur est utilisée en réduisant le trafic réseau entre l’ordinateur de l’utilisateur et le serveur.
  
En règle générale, il n’y a aucune précises modalités d’associant étroitement les fournisseurs de services. Toutefois, vous devez utiliser les instructions suivantes :
  
- Si la raison d’associant étroitement les fournisseurs de services est performances, n’oubliez pas que le couplage prend les composants du sous-système MAPI en dehors de ces composants seraient normalement être impliqués dans les processus. Cela implique que les composants individuels dans le fournisseur de services combiné doivent interagir avec eux d’une manière qui simule l’interaction qu’ils disposent normalement avec les composants du sous-système MAPI qui ne sont pas utilisés.
    
- Lorsque les fournisseurs de services étroitement couplés interaction avec d’autres composants MAPI, ils doivent toujours interagir avec eux dans exactement comme elles étaient si elles n’étaient pas étroitement couplés. Par exemple, si un utilisateur utilise un fournisseur de magasin combinée de message et le fournisseur de transport comme leur banque de messages par défaut, mais utilise un fournisseur de transport distincts pour envoyer des messages, comme peut se produire lorsqu’un utilisateur prend un ordinateur en déplacement et bascule vers un pr transport à distance ovider : la partie de la banque de message du fournisseur de services étroitement couplés doit toujours interagir avec spouleur MAPI comme s’il s’agissait d’un fournisseur de magasins de message autonome.
    
## <a name="see-also"></a>Voir aussi



[D�veloppement d'un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

