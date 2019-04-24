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
description: 'Dernière modification: 08 08, 2011'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315476"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="4dce0-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="4dce0-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="4dce0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4dce0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4dce0-105">Enregistre les fichiers de dossiers personnels (. pst) pour le déverrouillage automatique, en évitant d'autres appels à HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="4dce0-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="4dce0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4dce0-106">Parameters</span></span>

<span data-ttu-id="4dce0-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="4dce0-107">_pmval_</span></span>
  
> <span data-ttu-id="4dce0-108">dans Une structure [SPropValue](spropvalue.md) qui contient un pointeur vers le chemin d'accès de la bibliothèque de liens dynamiques (dll) à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="4dce0-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="4dce0-109">La structure présente les caractéristiques suivantes:</span><span class="sxs-lookup"><span data-stu-id="4dce0-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="4dce0-110">UlPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="4dce0-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="4dce0-111">Propriété de valeur MVszW définie sur un tableau de chaînes de caractères Unicode terminées par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="4dce0-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="4dce0-112">Pour plus d'informations, consultez la rubrique [SWStringArray](swstringarray.md) .</span><span class="sxs-lookup"><span data-stu-id="4dce0-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="4dce0-113">Le SPropValue est stocké dans une propriété MAPI dans la plage interne du PST.</span><span class="sxs-lookup"><span data-stu-id="4dce0-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="4dce0-114">Cette propriété n'est pas accessible aux applications MAPI ordinaires.</span><span class="sxs-lookup"><span data-stu-id="4dce0-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="4dce0-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4dce0-115">Return value</span></span>

<span data-ttu-id="4dce0-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4dce0-116">S_OK</span></span> 
  
> <span data-ttu-id="4dce0-117">L'appel de la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="4dce0-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4dce0-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="4dce0-118">Remarks</span></span>

<span data-ttu-id="4dce0-119">Les enregistrements rendus persistants peuvent avoir un impact négatif sur les performances des applications, telles que Outlook et Windows Desktop Search, qui ouvrent des fichiers PST.</span><span class="sxs-lookup"><span data-stu-id="4dce0-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="4dce0-120">Tenez compte de l'impact sur les performances lors de l'utilisation ou du développement de l'utilisation des enregistrements rendus persistants.</span><span class="sxs-lookup"><span data-stu-id="4dce0-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="4dce0-121">Cette méthode est implémentée uniquement pour Unicode.</span><span class="sxs-lookup"><span data-stu-id="4dce0-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="4dce0-122">De plus, il échouera de manière préventive si l'un des chemins d'accès dans le tableau n'a pas d'extension de nom de fichier. dll.</span><span class="sxs-lookup"><span data-stu-id="4dce0-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4dce0-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4dce0-123">See also</span></span>

- [<span data-ttu-id="4dce0-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4dce0-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="4dce0-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4dce0-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

