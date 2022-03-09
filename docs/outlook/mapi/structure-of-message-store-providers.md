---
title: Structure des fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
ms.openlocfilehash: 04c5bf5a7e1f433ae13bfc1cd322c91be6676ab6
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368740"
---
# <a name="structure-of-message-store-providers"></a>Structure des fournisseurs de banques de messages
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur de magasin de messages, lorsqu’il est en cours d’exécution en mémoire, est une interface [IMSProvider : IUnknown](imsprovideriunknown.md) . **L’interface IMSProvider** permet aux applications clientes et aupooler MAPI de se connecter et de se déconnecter de la magasin de messages. Les interfaces que les applications clientes et lepooler MAPI utilisent pour accéder aux dossiers et aux messages dans la boutique de messages sont les interfaces [IMSLogon](imslogoniunknown.md) et [IMsgStore](imsgstoreimapiprop.md) . Ces interfaces sont généralement créées lors de la première ouverture de session de la magasin de messages, bien que le point d’entrée [MSProviderInit](msproviderinit.md) de la DLL de la magasin de messages puisse également les créer. 
  
Étant donné que les interfaces **IMSLogon** et **IMsgStore** partagent certaines méthodes, il peut être plus facile de créer un objet de classe qui hérite de ces deux interfaces. Vous pouvez également implémenter ces interfaces dans des objets distincts et écrire des fonctions d’aide internes à votre DLL qui implémentent les méthodes partagées qui peuvent ensuite être appelées à partir des méthodes dans les interfaces **IMSLogon** et **IMsgStore** . 
  
L’illustration suivante montre un plan de haut niveau de la hiérarchie d’objets au sein d’une magasin de messages en cours d’exécution.
  
**Hiérarchie d’objets de banque de messages**
  
![Hiérarchie d’objets de banque de messages](media/storeobj.gif "Hiérarchie d’objets de banque de messages")
  
## <a name="see-also"></a>Voir aussi

- [Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

