---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784532"
---
# <a name="ltid"></a><span data-ttu-id="a8fde-103">LTID</span><span class="sxs-lookup"><span data-stu-id="a8fde-103">LTID</span></span>

  
  
<span data-ttu-id="a8fde-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8fde-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8fde-105">Générique ID termes Long d’un objet dans un magasin d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="a8fde-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a8fde-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a8fde-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="a8fde-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a8fde-107">Members</span></span>

 <span data-ttu-id="a8fde-108">_GUID_</span><span class="sxs-lookup"><span data-stu-id="a8fde-108">_guid_</span></span>
  
- <span data-ttu-id="a8fde-109">[out] Le GUID du serveur qui a créé l’objet.</span><span class="sxs-lookup"><span data-stu-id="a8fde-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="a8fde-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="a8fde-110">_globcnt_</span></span>
  
- <span data-ttu-id="a8fde-111">[out] Numéro unique 6 octets qui identifie l’objet au sein de la banque d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="a8fde-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="a8fde-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="a8fde-112">_wLevel_</span></span>
  
- <span data-ttu-id="a8fde-113">[out] Niveau de la hiérarchie de l’identificateur d’entrée pour un dossier Public favoris Exchange.</span><span class="sxs-lookup"><span data-stu-id="a8fde-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8fde-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8fde-114">See also</span></span>



[<span data-ttu-id="a8fde-115">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="a8fde-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a8fde-116">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="a8fde-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a8fde-117">FEID</span><span class="sxs-lookup"><span data-stu-id="a8fde-117">FEID</span></span>](feid.md)

