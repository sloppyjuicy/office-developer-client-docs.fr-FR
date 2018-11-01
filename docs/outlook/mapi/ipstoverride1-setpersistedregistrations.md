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
description: 'Dernière modification : 08 novembre 2011'
ms.openlocfilehash: 3592584a08bf14725c0289831740e91fb8f1a5b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587620"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="2d0a7-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="2d0a7-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="2d0a7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d0a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d0a7-105">Enregistre les fichiers de dossiers personnels (.pst) pour le déverrouillage automatique, en évitant les appels supplémentaires à la HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="2d0a7-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="2d0a7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d0a7-106">Parameters</span></span>

<span data-ttu-id="2d0a7-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="2d0a7-107">_pmval_</span></span>
  
> <span data-ttu-id="2d0a7-108">[in] Contient un pointeur vers le chemin d’accès de la bibliothèque de liens dynamiques (DLL) pour inscrire une structure [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="2d0a7-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="2d0a7-109">La structure présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="2d0a7-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="2d0a7-110">Un ulPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="2d0a7-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="2d0a7-111">Une propriété de valeur MVszW qui est définie sur un tableau de chaînes de caractères Unicode terminée par null.</span><span class="sxs-lookup"><span data-stu-id="2d0a7-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="2d0a7-112">Pour plus d’informations, consultez la rubrique [SWStringArray](swstringarray.md) .</span><span class="sxs-lookup"><span data-stu-id="2d0a7-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="2d0a7-113">Le SPropValue est stocké dans une propriété MAPI dans une plage interne du fichier PST.</span><span class="sxs-lookup"><span data-stu-id="2d0a7-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="2d0a7-114">Cette propriété n’est pas accessible pour les applications MAPI ordinaires.</span><span class="sxs-lookup"><span data-stu-id="2d0a7-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="2d0a7-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2d0a7-115">Return value</span></span>

<span data-ttu-id="2d0a7-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d0a7-116">S_OK</span></span> 
  
> <span data-ttu-id="2d0a7-117">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="2d0a7-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d0a7-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="2d0a7-118">Remarks</span></span>

<span data-ttu-id="2d0a7-119">Les enregistrements persistants peuvent affecter les performances des applications, tels qu’Outlook et Windows Desktop Search, ouvrez les fichiers pst.</span><span class="sxs-lookup"><span data-stu-id="2d0a7-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="2d0a7-120">Prendre en compte l’impact sur les performances lors de l’aide ou développer l’utilisation des enregistrements persistants.</span><span class="sxs-lookup"><span data-stu-id="2d0a7-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2d0a7-121">Cette méthode est implémentée uniquement pour le format Unicode.</span><span class="sxs-lookup"><span data-stu-id="2d0a7-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="2d0a7-122">En outre, il façon préventive échoue si un des chemins d’accès dans le tableau n’ont pas une extension de nom de fichier du fichier .dll.</span><span class="sxs-lookup"><span data-stu-id="2d0a7-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d0a7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d0a7-123">See also</span></span>

- [<span data-ttu-id="2d0a7-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d0a7-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="2d0a7-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d0a7-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

