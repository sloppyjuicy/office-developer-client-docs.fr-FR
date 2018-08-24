---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 079b54757cfcd5c9b38365abc5a6d901e2b06724
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580718"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="5360c-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="5360c-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="5360c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5360c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5360c-105">Définit un magasin pour émuler le Gestionnaire de protocole Outlook pour mettre en attente des messages sortants vers un serveur local.</span><span class="sxs-lookup"><span data-stu-id="5360c-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="5360c-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="5360c-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="5360c-107">[in] Définissez ce paramètre sur True si la banque locale doit émuler le spouleur ; défini sur False dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5360c-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5360c-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="5360c-108">Remarks</span></span>

<span data-ttu-id="5360c-109">Une banque locale appelle **IPSTX::EmulateSpooler** pour agir comme un gestionnaire de protocole Outlook, les messages en attente dans la file d’attente sortante pour le serveur principal (par exemple, le serveur MSN ou le serveur de AOL) pour le traitement.</span><span class="sxs-lookup"><span data-stu-id="5360c-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="5360c-110">Le magasin émule un spouleur lors de la synchronisation, puis appelle ces deux méthodes :</span><span class="sxs-lookup"><span data-stu-id="5360c-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="5360c-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** pour obtenir la sortant de la file d’attente de messages dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="5360c-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="5360c-112">Cette méthode fonctionne uniquement si la banque émule le Gestionnaire de protocole Outlook.</span><span class="sxs-lookup"><span data-stu-id="5360c-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="5360c-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** pour sécuriser l’accès exclusif à un message dans la file d’attente sortante juste avant l’envoi au serveur.</span><span class="sxs-lookup"><span data-stu-id="5360c-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="5360c-114">Cette méthode fonctionne uniquement si la banque émule le Gestionnaire de protocole Outlook.</span><span class="sxs-lookup"><span data-stu-id="5360c-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="5360c-115">Après avoir envoyé le message, le magasin appelle cette méthode pour libérer un accès exclusif au son.</span><span class="sxs-lookup"><span data-stu-id="5360c-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="5360c-116">Depuis Outlook 2002, le Gestionnaire de protocole Outlook remplacé le spouleur MAPI et qu’il est devenu responsable pour les messages sortants en attente pour les serveurs principaux.</span><span class="sxs-lookup"><span data-stu-id="5360c-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5360c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5360c-117">See also</span></span>



[<span data-ttu-id="5360c-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="5360c-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="5360c-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="5360c-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

