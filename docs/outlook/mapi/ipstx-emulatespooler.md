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
ms.openlocfilehash: 024583926b5d0be638b33b1b60c5d4c5dc74d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438952"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="439d5-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="439d5-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="439d5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="439d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="439d5-105">Définit un magasin local pour émuler le gestionnaire Outlook protocole pour mettre en file d’ensemble les messages sortants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="439d5-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="439d5-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="439d5-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="439d5-107">[in] Définissez ce paramètre sur True si le magasin local doit émuler lepooler ; si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="439d5-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="439d5-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="439d5-108">Remarks</span></span>

<span data-ttu-id="439d5-109">Un magasin local appelle **IPSTX::EmulateSpooler** pour agir en tant que gestionnaire de protocole Outlook, en stockant les messages dans la file d’attente sortante vers le serveur principal (par exemple, le serveur MSN ou le serveur AOL) pour le traitement.</span><span class="sxs-lookup"><span data-stu-id="439d5-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="439d5-110">Lors de l’émulation d’unpooler lors de la synchronisation, le magasin appelle ensuite les deux méthodes ci-après :</span><span class="sxs-lookup"><span data-stu-id="439d5-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="439d5-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span><span class="sxs-lookup"><span data-stu-id="439d5-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="439d5-112">Cette méthode réussit uniquement si le magasin émule le gestionnaire Outlook protocole.</span><span class="sxs-lookup"><span data-stu-id="439d5-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="439d5-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** pour sécuriser l’accès unique à un message dans la file d’attente sortante juste avant de l’envoyer au serveur.</span><span class="sxs-lookup"><span data-stu-id="439d5-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="439d5-114">Cette méthode réussit uniquement si le magasin émule le gestionnaire Outlook protocole.</span><span class="sxs-lookup"><span data-stu-id="439d5-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="439d5-115">Après l’envoi du message, la boutique appelle à nouveau cette méthode pour libérer l’accès unique à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="439d5-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="439d5-116">Depuis Outlook 2002, le gestionnaire de protocole Outlook a remplacé lepooler MAPI et est devenu responsable dupooling des messages sortants sur les serveurs back-end.</span><span class="sxs-lookup"><span data-stu-id="439d5-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="439d5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="439d5-117">See also</span></span>



[<span data-ttu-id="439d5-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="439d5-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="439d5-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="439d5-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

