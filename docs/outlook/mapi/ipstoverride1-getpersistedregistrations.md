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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 56aaf5caf93f90f54d152ab3684ca592cd45cd1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784409"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="5deeb-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="5deeb-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="5deeb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5deeb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5deeb-105">Récupère la liste des enregistrements pour le fichier de dossiers personnels (.pst).</span><span class="sxs-lookup"><span data-stu-id="5deeb-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="5deeb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5deeb-106">Parameters</span></span>

 <span data-ttu-id="5deeb-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="5deeb-107">_ppmval_</span></span>
  
> <span data-ttu-id="5deeb-108">[in] Pointeur vers un pointeur vers une structure [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="5deeb-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="5deeb-109">Le membre ulPropTag de cette structure est du type PT_MV_UNICODE, et le membre de la valeur MVszW sera un tableau de chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="5deeb-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="5deeb-110">Ces chaînes sont des chemins d’accès aux fichiers DLL pour laquelle l’enregistrement a été conservée.</span><span class="sxs-lookup"><span data-stu-id="5deeb-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="5deeb-111">prise en charge .pst ANSI n’est pas implémenté.</span><span class="sxs-lookup"><span data-stu-id="5deeb-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="5deeb-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="5deeb-112">Return value</span></span>

<span data-ttu-id="5deeb-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="5deeb-113">S_OK</span></span> 
  
> <span data-ttu-id="5deeb-114">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="5deeb-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5deeb-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5deeb-115">See also</span></span>



[<span data-ttu-id="5deeb-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5deeb-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="5deeb-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5deeb-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

