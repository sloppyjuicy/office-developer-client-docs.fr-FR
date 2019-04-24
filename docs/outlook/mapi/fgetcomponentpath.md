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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335209"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="62e58-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="62e58-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="62e58-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62e58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62e58-105">Renvoie le chemin d'accès au fichier Mapi32. dll privé.</span><span class="sxs-lookup"><span data-stu-id="62e58-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="62e58-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62e58-106">Parameters</span></span>

 <span data-ttu-id="62e58-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="62e58-107">_szComponent_</span></span>
  
> <span data-ttu-id="62e58-108">dans La clé Reg MSIComponentID décrite dans les [paramètres du Registre stub Mapi32. dll](https://msdn.microsoft.com/library/dd162409.aspx).</span><span class="sxs-lookup"><span data-stu-id="62e58-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="62e58-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="62e58-109">_szQualifier_</span></span>
  
> <span data-ttu-id="62e58-110">dans La sous-clé MSIApplicationLCID ou MSIOfficeLCID décrite dans [Choose a specific version of MAPI to load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="62e58-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="62e58-111">Les appelants peuvent transmettre la **valeur null** s'il n'y a aucun qualificateur.</span><span class="sxs-lookup"><span data-stu-id="62e58-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="62e58-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="62e58-112">_szDllPath_</span></span>
  
> <span data-ttu-id="62e58-113">dans Chemin d'accès au fichier Mapi32. dll privé, qui dispose de la fonctionnalité MAPI complète (les mêmes exportations que Mapi32. dll).</span><span class="sxs-lookup"><span data-stu-id="62e58-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="62e58-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="62e58-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="62e58-115">dans Taille de _szDllPath_, en caractères.</span><span class="sxs-lookup"><span data-stu-id="62e58-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="62e58-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="62e58-116">_fInstall_</span></span>
  
> <span data-ttu-id="62e58-117">dans Indique à MAPI d'installer le composant privé Mapi32. dll s'il est absent.</span><span class="sxs-lookup"><span data-stu-id="62e58-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="62e58-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="62e58-118">Return value</span></span>

 <span data-ttu-id="62e58-119">**true**</span><span class="sxs-lookup"><span data-stu-id="62e58-119">**true**</span></span>
  
> <span data-ttu-id="62e58-120">Le chemin d'accès a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="62e58-120">The path was found.</span></span>
    
 <span data-ttu-id="62e58-121">**true**</span><span class="sxs-lookup"><span data-stu-id="62e58-121">**false**</span></span>
  
> <span data-ttu-id="62e58-122">Le chemin d'accès est introuvable.</span><span class="sxs-lookup"><span data-stu-id="62e58-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="62e58-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="62e58-123">Remarks</span></span>

<span data-ttu-id="62e58-124">Utilisez la fonction **FGetComponentPath** lorsque vous devez obtenir le chemin d'accès au fichier Mapi32. dll privé.</span><span class="sxs-lookup"><span data-stu-id="62e58-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62e58-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62e58-125">See also</span></span>



[<span data-ttu-id="62e58-126">Choisir une version spécifique de MAPI à charger</span><span class="sxs-lookup"><span data-stu-id="62e58-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="62e58-127">Paramètres de Registre stub Mapi32. dll</span><span class="sxs-lookup"><span data-stu-id="62e58-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

