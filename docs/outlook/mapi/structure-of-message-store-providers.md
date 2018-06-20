---
title: Structure de fournisseurs de magasins de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2f78428b8067b7937e9bd2ee36934cc29a16bfb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787293"
---
# <a name="structure-of-message-store-providers"></a>Structure de fournisseurs de magasins de message
  
**S’applique à**: Outlook 
  
Un fournisseur de magasin de message, lorsqu’il s’exécute en mémoire, est un [IMSProvider : IUnknown](imsprovideriunknown.md) interface. L’interface **IMSProvider** permet aux clients applications et le spouleur MAPI pour vous connecter à et sur la banque de messages. Les interfaces par les applications clientes et le spouleur MAPI pour accéder aux dossiers et des messages dans la banque de messages sont des interfaces [IMSLogon](imslogoniunknown.md) et [IMsgStore](imsgstoreimapiprop.md) . Ces interfaces sont généralement créés lors de la banque de messages est tout d’abord ouvrir une session sur, bien que le point d’entrée du message [MSProviderInit](msproviderinit.md) stocker DLL peut également les créer. 
  
Étant donné que les interfaces **IMSLogon** et **IMsgStore** partagent certaines méthodes, il peut être plus facile de créer un objet de classe qui hérite de ces deux interfaces. Vous pouvez également implémenter ces interfaces dans des objets distincts et écrire des fonctions d’assistance internes à votre DLL implémentent les méthodes partagés qui peuvent être appelées à partir des méthodes dans les interfaces **IMSLogon** et **IMsgStore** . 
  
L’illustration suivante montre un plan de haut niveau de la hiérarchie d’objets au sein d’une banque de messages en cours d’exécution.
  
**Hiérarchie d’objets de banque de messages**
  
![Hiérarchie d’objets de banque de messages] (media/storeobj.gif "Hiérarchie d’objets de banque de messages")
  
## <a name="see-also"></a>Voir aussi

- [D�veloppement d'un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

