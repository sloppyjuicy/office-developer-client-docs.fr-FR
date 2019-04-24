---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7338edc13227e303ec5fa47da4a5d9ee611c6749
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326151"
---
# <a name="upread"></a><span data-ttu-id="51140-103">UPREAD</span><span class="sxs-lookup"><span data-stu-id="51140-103">UPREAD</span></span>

  
  
<span data-ttu-id="51140-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51140-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51140-105">Informations pour le téléchargement de l'état de lecture des éléments lors de l'état de [lecture de téléchargement](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="51140-105">Information for uploading the read state of items during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="51140-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="51140-106">Quick info</span></span>

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="51140-107">Membres</span><span class="sxs-lookup"><span data-stu-id="51140-107">Members</span></span>

 <span data-ttu-id="51140-108">_pupre_</span><span class="sxs-lookup"><span data-stu-id="51140-108">_pupre_</span></span>
  
>  <span data-ttu-id="51140-109">remarquer Vecteur des entrées de **[lecture](upreade.md)** .</span><span class="sxs-lookup"><span data-stu-id="51140-109">[out] Vector of **[UPREADE](upreade.md)** entries.</span></span> 
    
 <span data-ttu-id="51140-110">_Motivé_</span><span class="sxs-lookup"><span data-stu-id="51140-110">_cEnt_</span></span>
  
>  <span data-ttu-id="51140-111">remarquer Nombre d'entrées **lues** .</span><span class="sxs-lookup"><span data-stu-id="51140-111">[out] Number of **UPREADE** entries.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="51140-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51140-112">See also</span></span>



[<span data-ttu-id="51140-113">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="51140-113">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="51140-114">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="51140-114">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="51140-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="51140-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="51140-116">UPREADE</span><span class="sxs-lookup"><span data-stu-id="51140-116">UPREADE</span></span>](upreade.md)

