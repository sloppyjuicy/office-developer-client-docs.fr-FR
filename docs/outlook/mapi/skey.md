---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c417e6f4412bc40e8c2ebc056514eb96f60798f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282676"
---
# <a name="skey"></a><span data-ttu-id="7bf0b-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="7bf0b-103">SKEY</span></span>

  
  
<span data-ttu-id="7bf0b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bf0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bf0b-105">Clé source pour un élément Outlook.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7bf0b-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7bf0b-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="7bf0b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7bf0b-107">Members</span></span>

 <span data-ttu-id="7bf0b-108">_directeurs_</span><span class="sxs-lookup"><span data-stu-id="7bf0b-108">_guid_</span></span>
  
> <span data-ttu-id="7bf0b-109">GUID du serveur qui crée l'objet.</span><span class="sxs-lookup"><span data-stu-id="7bf0b-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7bf0b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bf0b-110">See also</span></span>



[<span data-ttu-id="7bf0b-111">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="7bf0b-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7bf0b-112">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="7bf0b-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7bf0b-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="7bf0b-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="7bf0b-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="7bf0b-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="7bf0b-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="7bf0b-115">UPREADE</span></span>](upreade.md)

