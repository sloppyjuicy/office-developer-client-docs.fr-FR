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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426421"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="f940e-103">Structure des fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="f940e-103">Structure of message store providers</span></span>
  
<span data-ttu-id="f940e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f940e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f940e-105">Un fournisseur de magasin de messages, lorsqu’il est en cours d’exécution en mémoire, est une interface [IMSProvider : IUnknown.](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="f940e-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="f940e-106">**L’interface IMSProvider** permet aux applications clientes et aupooler MAPI de se connecter et de se déconnecter de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="f940e-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="f940e-107">Les interfaces que les applications clientes et lepooler MAPI utilisent pour accéder aux dossiers et aux messages dans la boutique de messages sont les interfaces [IMSLogon](imslogoniunknown.md) et [IMsgStore.](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="f940e-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="f940e-108">Ces interfaces sont généralement créées lors de la première ouverture de session de la magasin de messages, bien que le point d’entrée [MSProviderInit](msproviderinit.md) de la DLL de la magasin de messages puisse également les créer.</span><span class="sxs-lookup"><span data-stu-id="f940e-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="f940e-109">Étant donné que les interfaces **IMSLogon** et **IMsgStore** partagent certaines méthodes, il peut être plus facile de créer un objet de classe qui hérite de ces deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="f940e-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="f940e-110">Vous pouvez également implémenter ces interfaces dans des objets distincts et écrire des fonctions d’aide internes à votre DLL qui implémentent les méthodes partagées qui peuvent ensuite être appelées à partir des méthodes des interfaces **IMSLogon** et **IMsgStore.**</span><span class="sxs-lookup"><span data-stu-id="f940e-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="f940e-111">L’illustration suivante montre un plan de haut niveau de la hiérarchie d’objets au sein d’une magasin de messages en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f940e-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="f940e-112">**Hiérarchie d’objets de banque de messages**</span><span class="sxs-lookup"><span data-stu-id="f940e-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="f940e-113">![Hiérarchie d’objets de magasin de messages Hiérarchie](media/storeobj.gif "d’objets de magasin de messages")</span><span class="sxs-lookup"><span data-stu-id="f940e-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f940e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f940e-114">See also</span></span>

- [<span data-ttu-id="f940e-115">Développement d’un fournisseur de banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="f940e-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

