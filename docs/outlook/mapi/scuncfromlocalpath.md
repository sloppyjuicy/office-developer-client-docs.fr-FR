---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: faba91d813d27f7ea45e978724ce0d4707803cba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590105"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="55d4e-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="55d4e-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="55d4e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55d4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55d4e-105">Localise un équivalent chemin d’accès UNC (convention) d’affectation de noms universels pour le chemin d’accès local donné.</span><span class="sxs-lookup"><span data-stu-id="55d4e-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55d4e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="55d4e-106">Header file:</span></span>  <br/> |<span data-ttu-id="55d4e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55d4e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="55d4e-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="55d4e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="55d4e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="55d4e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="55d4e-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="55d4e-110">Called by:</span></span>  <br/> |<span data-ttu-id="55d4e-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="55d4e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="55d4e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55d4e-112">Parameters</span></span>

 <span data-ttu-id="55d4e-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="55d4e-113">_szLocal_</span></span>
  
> <span data-ttu-id="55d4e-114">[in] Un chemin d’accès dans le format [ _lecteur :_]\[ _chemin d’accès_] d’un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="55d4e-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="55d4e-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="55d4e-115">_szUNC_</span></span>
  
> <span data-ttu-id="55d4e-116">[out] Un chemin d’accès au format \\[ _server_]\[ _partager_]\[ _chemin d’accès_] du même fichier ou répertoire que pour le paramètre _szLocal_ .</span><span class="sxs-lookup"><span data-stu-id="55d4e-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="55d4e-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="55d4e-117">_cchUNC_</span></span>
  
> <span data-ttu-id="55d4e-118">[in] Taille de la mémoire tampon de la chaîne de sortie.</span><span class="sxs-lookup"><span data-stu-id="55d4e-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="55d4e-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="55d4e-119">Return value</span></span>

<span data-ttu-id="55d4e-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="55d4e-120">S_OK</span></span>
  
> <span data-ttu-id="55d4e-121">L’équivalent du chemin d’accès UNC a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="55d4e-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="55d4e-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="55d4e-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="55d4e-123">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="55d4e-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="55d4e-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="55d4e-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="55d4e-125">_szUNC_ n’était pas suffisante pour contenir le résultat.</span><span class="sxs-lookup"><span data-stu-id="55d4e-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="55d4e-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="55d4e-126">S_FALSE</span></span>
  
> <span data-ttu-id="55d4e-127">Le chemin d’accès local a déjà une chaîne UNC.</span><span class="sxs-lookup"><span data-stu-id="55d4e-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55d4e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55d4e-128">See also</span></span>



[<span data-ttu-id="55d4e-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="55d4e-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

