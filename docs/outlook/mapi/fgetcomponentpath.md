---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335209"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="ae233-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="ae233-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="ae233-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae233-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae233-105">Renvoie le chemin d’accès au Mapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="ae233-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="ae233-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ae233-106">Parameters</span></span>

 <span data-ttu-id="ae233-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="ae233-107">_szComponent_</span></span>
  
> <span data-ttu-id="ae233-108">[in] La clé de registre MSIComponentID décrite dans [Mapi32.dll registre Stub Paramètres](https://msdn.microsoft.com/library/dd162409.aspx).</span><span class="sxs-lookup"><span data-stu-id="ae233-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="ae233-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="ae233-109">_szQualifier_</span></span>
  
> <span data-ttu-id="ae233-110">[in] La sous-clé MSIApplicationLCID ou MSIOfficeLCID décrite dans [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="ae233-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="ae233-111">Les appelants peuvent passer la **valeur null** s’il n’existe aucun qualificateur.</span><span class="sxs-lookup"><span data-stu-id="ae233-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="ae233-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="ae233-112">_szDllPath_</span></span>
  
> <span data-ttu-id="ae233-113">[in] Chemin d’accès au Mapi32.dll privé, qui dispose de toutes les fonctionnalités MAPI (les mêmes exportations que le Mapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="ae233-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="ae233-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="ae233-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="ae233-115">[in] Taille de  _szDllPath,_ en caractères.</span><span class="sxs-lookup"><span data-stu-id="ae233-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="ae233-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="ae233-116">_fInstall_</span></span>
  
> <span data-ttu-id="ae233-117">[in] Indique à MAPI d’installer le Mapi32.dll privé s’il est absent.</span><span class="sxs-lookup"><span data-stu-id="ae233-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ae233-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae233-118">Return value</span></span>

 <span data-ttu-id="ae233-119">**true**</span><span class="sxs-lookup"><span data-stu-id="ae233-119">**true**</span></span>
  
> <span data-ttu-id="ae233-120">Le chemin d’accès a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="ae233-120">The path was found.</span></span>
    
 <span data-ttu-id="ae233-121">**false**</span><span class="sxs-lookup"><span data-stu-id="ae233-121">**false**</span></span>
  
> <span data-ttu-id="ae233-122">Le chemin d’accès est in trouvé.</span><span class="sxs-lookup"><span data-stu-id="ae233-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae233-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="ae233-123">Remarks</span></span>

<span data-ttu-id="ae233-124">Utilisez la **fonction FGetComponentPath** lorsque vous avez besoin d’obtenir le chemin d’accès au Mapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="ae233-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae233-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae233-125">See also</span></span>



[<span data-ttu-id="ae233-126">Choisir une version spécifique de MAPI à charger</span><span class="sxs-lookup"><span data-stu-id="ae233-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="ae233-127">Mapi32.dll registre Stub Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae233-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

