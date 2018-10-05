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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384499"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="e8caa-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="e8caa-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="e8caa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8caa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8caa-105">Renvoie le chemin d’accès pour le fichier Mapi32.dll privé.</span><span class="sxs-lookup"><span data-stu-id="e8caa-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="e8caa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8caa-106">Parameters</span></span>

 <span data-ttu-id="e8caa-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="e8caa-107">_szComponent_</span></span>
  
> <span data-ttu-id="e8caa-108">[in] La clé de Registre MSIComponentID décrite dans les [Paramètres de Registre Stub Mapi32.dll](https://msdn.microsoft.com/library/dd162409.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8caa-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="e8caa-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="e8caa-109">_szQualifier_</span></span>
  
> <span data-ttu-id="e8caa-110">[in] La sous-clé MSIApplicationLCID ou MSIOfficeLCID décrite dans la zone [Choisissez une Version spécifique de MAPI à charge](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="e8caa-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="e8caa-111">Les appelants peuvent passer **null** s’il n’existe aucun qualificateur.</span><span class="sxs-lookup"><span data-stu-id="e8caa-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="e8caa-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="e8caa-112">_szDllPath_</span></span>
  
> <span data-ttu-id="e8caa-113">[in] Le chemin d’accès pour le fichier Mapi32.dll privée, qui comprend toutes les fonctionnalités MAPI (exportations même en tant que le fichier Mapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="e8caa-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="e8caa-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="e8caa-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="e8caa-115">[in] Taille de _szDllPath_, en caractères.</span><span class="sxs-lookup"><span data-stu-id="e8caa-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="e8caa-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="e8caa-116">_fInstall_</span></span>
  
> <span data-ttu-id="e8caa-117">[in] Indique à MAPI pour installer le composant Mapi32.dll privé si elle est absente.</span><span class="sxs-lookup"><span data-stu-id="e8caa-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8caa-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e8caa-118">Return value</span></span>

 <span data-ttu-id="e8caa-119">**valeur True**</span><span class="sxs-lookup"><span data-stu-id="e8caa-119">**true**</span></span>
  
> <span data-ttu-id="e8caa-120">Le chemin d’accès a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="e8caa-120">The path was found.</span></span>
    
 <span data-ttu-id="e8caa-121">**False**</span><span class="sxs-lookup"><span data-stu-id="e8caa-121">**false**</span></span>
  
> <span data-ttu-id="e8caa-122">Le chemin d’accès est introuvable.</span><span class="sxs-lookup"><span data-stu-id="e8caa-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8caa-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8caa-123">Remarks</span></span>

<span data-ttu-id="e8caa-124">Utilisez la fonction **FGetComponentPath** lorsque vous avez besoin obtenir le chemin d’accès pour le fichier Mapi32.dll privé.</span><span class="sxs-lookup"><span data-stu-id="e8caa-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8caa-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8caa-125">See also</span></span>



[<span data-ttu-id="e8caa-126">Choisir une version spécifique de MAPI à charger</span><span class="sxs-lookup"><span data-stu-id="e8caa-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="e8caa-127">Paramètres de Registre Stub Mapi32.dll</span><span class="sxs-lookup"><span data-stu-id="e8caa-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

