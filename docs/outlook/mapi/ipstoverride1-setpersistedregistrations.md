---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408347"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="4a964-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="4a964-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="4a964-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a964-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a964-105">Enregistre les fichiers de dossiers personnels (.pst) pour le déverrouillage automatique, en évitant d’autres appels à HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="4a964-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="4a964-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a964-106">Parameters</span></span>

<span data-ttu-id="4a964-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="4a964-107">_pmval_</span></span>
  
> <span data-ttu-id="4a964-108">[in] Structure [SPropValue](spropvalue.md) qui contient un pointeur vers le chemin d’accès de la bibliothèque de liens dynamiques (DLL) à inscrire.</span><span class="sxs-lookup"><span data-stu-id="4a964-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="4a964-109">La structure présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a964-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="4a964-110">UlPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="4a964-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="4a964-111">Propriété de valeur MVszW définie sur un tableau de chaînes de caractères Unicode terminées par null.</span><span class="sxs-lookup"><span data-stu-id="4a964-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="4a964-112">Pour plus d’informations, [voir la rubrique SWStringArray.](swstringarray.md)</span><span class="sxs-lookup"><span data-stu-id="4a964-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="4a964-113">La valeur SPropValue est stockée dans une propriété MAPI dans la plage interne du PST.</span><span class="sxs-lookup"><span data-stu-id="4a964-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="4a964-114">Cette propriété n’est pas accessible aux applications MAPI ordinaires.</span><span class="sxs-lookup"><span data-stu-id="4a964-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="4a964-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4a964-115">Return value</span></span>

<span data-ttu-id="4a964-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4a964-116">S_OK</span></span> 
  
> <span data-ttu-id="4a964-117">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="4a964-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4a964-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="4a964-118">Remarks</span></span>

<span data-ttu-id="4a964-119">Les inscriptions persistantes peuvent nuire aux performances des applications, telles qu’Outlook et Windows Desktop Search, qui ouvrent des PST.</span><span class="sxs-lookup"><span data-stu-id="4a964-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="4a964-120">Prenons en compte l’impact sur les performances lors de l’utilisation ou de l’extension de l’utilisation d’inscriptions persistantes.</span><span class="sxs-lookup"><span data-stu-id="4a964-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="4a964-121">Cette méthode est implémentée pour Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="4a964-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="4a964-122">En outre, elle échouera de manière préemptive si l’un des chemins d’accès du tableau n’a pas d’extension de nom de fichier .dll.</span><span class="sxs-lookup"><span data-stu-id="4a964-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4a964-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a964-123">See also</span></span>

- [<span data-ttu-id="4a964-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a964-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="4a964-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a964-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

