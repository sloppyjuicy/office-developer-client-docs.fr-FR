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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 667eda2a018d2a5d712950a31e05ec0ba9bb32ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787095"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="e5452-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="e5452-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="e5452-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5452-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5452-105">Localise un équivalent chemin d’accès UNC (convention) d’affectation de noms universels pour le chemin d’accès local donné.</span><span class="sxs-lookup"><span data-stu-id="e5452-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5452-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e5452-106">Header file:</span></span>  <br/> |<span data-ttu-id="e5452-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5452-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e5452-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="e5452-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e5452-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e5452-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e5452-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="e5452-110">Called by:</span></span>  <br/> |<span data-ttu-id="e5452-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e5452-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="e5452-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5452-112">Parameters</span></span>

 <span data-ttu-id="e5452-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="e5452-113">_szLocal_</span></span>
  
> <span data-ttu-id="e5452-114">[in] Un chemin d’accès dans le format [ _lecteur :_]\[ _chemin d’accès_] d’un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="e5452-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="e5452-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="e5452-115">_szUNC_</span></span>
  
> <span data-ttu-id="e5452-116">[out] Un chemin d’accès au format \\[ _server_]\[ _partager_]\[ _chemin d’accès_] du même fichier ou répertoire que pour le paramètre _szLocal_ .</span><span class="sxs-lookup"><span data-stu-id="e5452-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="e5452-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="e5452-117">_cchUNC_</span></span>
  
> <span data-ttu-id="e5452-118">[in] Taille de la mémoire tampon de la chaîne de sortie.</span><span class="sxs-lookup"><span data-stu-id="e5452-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5452-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e5452-119">Return value</span></span>

<span data-ttu-id="e5452-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5452-120">S_OK</span></span>
  
> <span data-ttu-id="e5452-121">L’équivalent du chemin d’accès UNC a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="e5452-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="e5452-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e5452-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="e5452-123">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e5452-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="e5452-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="e5452-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="e5452-125">_szUNC_ n’était pas suffisante pour contenir le résultat.</span><span class="sxs-lookup"><span data-stu-id="e5452-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="e5452-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e5452-126">S_FALSE</span></span>
  
> <span data-ttu-id="e5452-127">Le chemin d’accès local a déjà une chaîne UNC.</span><span class="sxs-lookup"><span data-stu-id="e5452-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5452-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5452-128">See also</span></span>



[<span data-ttu-id="e5452-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="e5452-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

