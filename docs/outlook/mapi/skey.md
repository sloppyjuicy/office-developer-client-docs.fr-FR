---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 26b08535d81cb961ed0ace70ea227316b30cd526
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573459"
---
# <a name="skey"></a><span data-ttu-id="7066b-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="7066b-103">SKEY</span></span>

  
  
<span data-ttu-id="7066b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7066b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7066b-105">Clé de la source d’un élément Outlook.</span><span class="sxs-lookup"><span data-stu-id="7066b-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7066b-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7066b-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="7066b-107">Members</span><span class="sxs-lookup"><span data-stu-id="7066b-107">Members</span></span>

 <span data-ttu-id="7066b-108">_GUID_</span><span class="sxs-lookup"><span data-stu-id="7066b-108">_guid_</span></span>
  
> <span data-ttu-id="7066b-109">GUID du serveur de création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7066b-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7066b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7066b-110">See also</span></span>



[<span data-ttu-id="7066b-111">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="7066b-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7066b-112">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="7066b-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7066b-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="7066b-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="7066b-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="7066b-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="7066b-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="7066b-115">UPREADE</span></span>](upreade.md)

