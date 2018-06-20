---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f4ece0662b72047b785b03f3134c96fac48c219a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787190"
---
# <a name="skey"></a><span data-ttu-id="9c97b-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="9c97b-103">SKEY</span></span>

  
  
<span data-ttu-id="9c97b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c97b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c97b-105">Clé de la source d’un élément Outlook.</span><span class="sxs-lookup"><span data-stu-id="9c97b-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9c97b-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="9c97b-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="9c97b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9c97b-107">Members</span></span>

 <span data-ttu-id="9c97b-108">_GUID_</span><span class="sxs-lookup"><span data-stu-id="9c97b-108">_guid_</span></span>
  
> <span data-ttu-id="9c97b-109">GUID du serveur de création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9c97b-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c97b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c97b-110">See also</span></span>



[<span data-ttu-id="9c97b-111">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="9c97b-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9c97b-112">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="9c97b-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9c97b-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="9c97b-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="9c97b-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="9c97b-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="9c97b-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="9c97b-115">UPREADE</span></span>](upreade.md)

