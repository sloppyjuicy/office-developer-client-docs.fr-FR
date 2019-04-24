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
ms.openlocfilehash: eda62a4cd31e0de695d52391a6717e7a0f5ea581
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327204"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="3f5bb-103">Structure des fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="3f5bb-103">Structure of message store providers</span></span>
  
<span data-ttu-id="3f5bb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f5bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f5bb-105">Un fournisseur de banque de messages, lorsqu'il est exécuté en mémoire, est une interface [IMSProvider: IUnknown](imsprovideriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="3f5bb-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="3f5bb-106">L'interface **IMSProvider** permet aux applications clientes et au SPOULEur MAPI de se connecter à la Banque de messages et de s'en déconnecter.</span><span class="sxs-lookup"><span data-stu-id="3f5bb-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="3f5bb-107">Les interfaces que les applications clientes et le spouleur MAPI utilisent pour accéder aux dossiers et aux messages dans la Banque de messages sont des interfaces [IMSLogon](imslogoniunknown.md) et [IMsgStore](imsgstoreimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="3f5bb-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="3f5bb-108">Ces interfaces sont généralement créées lors de la première ouverture de session de la Banque de messages, bien que le point d'entrée [MSProviderInit](msproviderinit.md) de la dll de la Banque de messages puisse également les créer.</span><span class="sxs-lookup"><span data-stu-id="3f5bb-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="3f5bb-109">Étant donné que les interfaces **IMSLogon** et **IMsgStore** partagent certaines méthodes, il peut être plus facile de créer un objet de classe qui hérite de ces deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="3f5bb-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="3f5bb-110">Vous pouvez également implémenter ces interfaces dans des objets distincts et écrire des fonctions d'assistance internes à votre DLL qui implémentent les méthodes partagées qui peuvent être appelées à partir des méthodes des interfaces **IMSLogon** et **IMsgStore** .</span><span class="sxs-lookup"><span data-stu-id="3f5bb-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="3f5bb-111">L'illustration suivante montre un plan de haut niveau de la hiérarchie des objets au sein d'une banque de messages en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="3f5bb-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="3f5bb-112">**Hiérarchie d’objets de banque de messages**</span><span class="sxs-lookup"><span data-stu-id="3f5bb-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="3f5bb-113">![Hiérarchie des objets] de la Banque de messages (media/storeobj.gif "Hiérarchie des objets") de la Banque de messages</span><span class="sxs-lookup"><span data-stu-id="3f5bb-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f5bb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f5bb-114">See also</span></span>

- [<span data-ttu-id="3f5bb-115">Développement d’un fournisseur de banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="3f5bb-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

