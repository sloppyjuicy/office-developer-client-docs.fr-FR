---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415130"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="351b6-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="351b6-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="351b6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="351b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="351b6-105">Extrait la liste des inscriptions pour le fichier de dossiers personnels (.pst).</span><span class="sxs-lookup"><span data-stu-id="351b6-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="351b6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="351b6-106">Parameters</span></span>

 <span data-ttu-id="351b6-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="351b6-107">_ppmval_</span></span>
  
> <span data-ttu-id="351b6-108">[in] Pointeur vers un pointeur vers une structure [SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="351b6-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="351b6-109">Le membre ulPropTag de cette structure est de type PT_MV_UNICODE et le membre de valeur MVszW sera un tableau de chaînes Unicode terminées par null.</span><span class="sxs-lookup"><span data-stu-id="351b6-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="351b6-110">Ces chaînes sont des chemins d’accès aux DLLs pour lesquelles l’inscription a été persistante.</span><span class="sxs-lookup"><span data-stu-id="351b6-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="351b6-111">La prise en charge de .pst pour ANSI n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="351b6-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="351b6-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="351b6-112">Return value</span></span>

<span data-ttu-id="351b6-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="351b6-113">S_OK</span></span> 
  
> <span data-ttu-id="351b6-114">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="351b6-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="351b6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="351b6-115">See also</span></span>



[<span data-ttu-id="351b6-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="351b6-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="351b6-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="351b6-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

