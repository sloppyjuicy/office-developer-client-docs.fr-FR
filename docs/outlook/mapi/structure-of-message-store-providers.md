---
title: Structure des fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 58b6771c6bdae91ad0e496189258e4745de5bc84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584288"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="c4ba0-103">Structure des fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="c4ba0-103">Structure of message store providers</span></span>
  
<span data-ttu-id="c4ba0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4ba0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4ba0-105">Un fournisseur de magasin de message, lorsqu’il s’exécute en mémoire, est un [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="c4ba0-106">L’interface **IMSProvider** permet aux clients applications et le spouleur MAPI pour vous connecter à et sur la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="c4ba0-107">Les interfaces par les applications clientes et le spouleur MAPI pour accéder aux dossiers et des messages dans la banque de messages sont des interfaces [IMSLogon](imslogoniunknown.md) et [IMsgStore](imsgstoreimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="c4ba0-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="c4ba0-108">Ces interfaces sont généralement créés lors de la banque de messages est tout d’abord ouvrir une session sur, bien que le point d’entrée du message [MSProviderInit](msproviderinit.md) stocker DLL peut également les créer.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="c4ba0-109">Étant donné que les interfaces **IMSLogon** et **IMsgStore** partagent certaines méthodes, il peut être plus facile de créer un objet de classe qui hérite de ces deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="c4ba0-110">Vous pouvez également implémenter ces interfaces dans des objets distincts et écrire des fonctions d’assistance internes à votre DLL implémentent les méthodes partagés qui peuvent être appelées à partir des méthodes dans les interfaces **IMSLogon** et **IMsgStore** .</span><span class="sxs-lookup"><span data-stu-id="c4ba0-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="c4ba0-111">L’illustration suivante montre un plan de haut niveau de la hiérarchie d’objets au sein d’une banque de messages en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c4ba0-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="c4ba0-112">**Hiérarchie d’objets de banque de messages**</span><span class="sxs-lookup"><span data-stu-id="c4ba0-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="c4ba0-113">![Hiérarchie d’objets de banque de messages] (media/storeobj.gif "Hiérarchie d’objets de banque de messages")</span><span class="sxs-lookup"><span data-stu-id="c4ba0-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c4ba0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4ba0-114">See also</span></span>

- [<span data-ttu-id="c4ba0-115">Développement d’un fournisseur de banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="c4ba0-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

