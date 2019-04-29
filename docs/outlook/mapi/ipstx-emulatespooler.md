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
# <a name="ipstxemulatespooler"></a><span data-ttu-id="abd61-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="abd61-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="abd61-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abd61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abd61-105">Définit une banque locale pour émuler le gestionnaire de protocoles Outlook afin de spouler les messages sortants vers un serveur.</span><span class="sxs-lookup"><span data-stu-id="abd61-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="abd61-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="abd61-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="abd61-107">dans Définissez ce paramètre sur true si le magasin local doit émuler le spouleur; Définissez-la sur false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="abd61-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="abd61-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="abd61-108">Remarks</span></span>

<span data-ttu-id="abd61-109">Un magasin local appelle **IPSTX:: EmulateSpooler** pour agir en tant que gestionnaire de protocoles Outlook, en spoule les messages de la file d'attente sortante vers le serveur principal (par exemple, le serveur MSN ou le serveur AOL) pour traitement.</span><span class="sxs-lookup"><span data-stu-id="abd61-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="abd61-110">Émulation d'un spouleur pendant la synchronisation, le magasin appelle les deux méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="abd61-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="abd61-111">**[IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** pour obtenir la file d'attente de messages sortante dans la Banque.</span><span class="sxs-lookup"><span data-stu-id="abd61-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="abd61-112">Cette méthode ne réussit que si la Banque émule le gestionnaire de protocoles Outlook.</span><span class="sxs-lookup"><span data-stu-id="abd61-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="abd61-113">**[IMsgStore:: SetLockState](imsgstore-setlockstate.md)** pour sécuriser l'accès exclusif à un message dans la file d'attente sortante juste avant de l'envoyer au serveur.</span><span class="sxs-lookup"><span data-stu-id="abd61-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="abd61-114">Cette méthode ne réussit que si la Banque émule le gestionnaire de protocoles Outlook.</span><span class="sxs-lookup"><span data-stu-id="abd61-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="abd61-115">Après l'envoi du message, le magasin appelle de nouveau cette méthode pour lui libérer un accès exclusif.</span><span class="sxs-lookup"><span data-stu-id="abd61-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="abd61-116">Depuis Outlook 2002, le gestionnaire de protocoles Outlook remplace le spouleur MAPI et est devenu responsable de la mise en file d'attente des messages sortants vers les serveurs principaux.</span><span class="sxs-lookup"><span data-stu-id="abd61-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="abd61-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abd61-117">See also</span></span>



[<span data-ttu-id="abd61-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="abd61-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="abd61-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="abd61-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

