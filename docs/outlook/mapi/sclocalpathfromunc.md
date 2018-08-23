---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e303361f4f0dd3a08dbb362096d07b8b391a6d97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594417"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="4e37f-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="4e37f-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="4e37f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e37f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e37f-105">Localise un équivalent du chemin d’accès local pour le chemin UNC (convention) d’affectation de noms universels.</span><span class="sxs-lookup"><span data-stu-id="4e37f-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e37f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4e37f-106">Header file:</span></span>  <br/> |<span data-ttu-id="4e37f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4e37f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4e37f-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="4e37f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4e37f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4e37f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4e37f-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="4e37f-110">Called by:</span></span>  <br/> |<span data-ttu-id="4e37f-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="4e37f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="4e37f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e37f-112">Parameters</span></span>

 <span data-ttu-id="4e37f-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="4e37f-113">_szUNC_</span></span>
  
> <span data-ttu-id="4e37f-114">[in] Un chemin d’accès au format \\[ _server_]\[ _partager_]\[ _chemin d’accès_] d’un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="4e37f-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="4e37f-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="4e37f-115">_szLocal_</span></span>
  
> <span data-ttu-id="4e37f-116">[out] Un chemin d’accès dans le format [ _lecteur :_]\[ _chemin d’accès_] du même fichier ou répertoire que pour le paramètre _szUNC_ .</span><span class="sxs-lookup"><span data-stu-id="4e37f-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="4e37f-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="4e37f-117">_cchLocal_</span></span>
  
> <span data-ttu-id="4e37f-118">[in] Taille de la mémoire tampon de la chaîne de sortie.</span><span class="sxs-lookup"><span data-stu-id="4e37f-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4e37f-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4e37f-119">Return value</span></span>

<span data-ttu-id="4e37f-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e37f-120">S_OK</span></span>
  
> <span data-ttu-id="4e37f-121">Un chemin d’accès local a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="4e37f-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="4e37f-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="4e37f-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="4e37f-123">_szLocal_ n’était pas suffisante pour contenir le résultat.</span><span class="sxs-lookup"><span data-stu-id="4e37f-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="4e37f-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="4e37f-124">S_FALSE</span></span>
  
> <span data-ttu-id="4e37f-125">La chaîne UNC est déjà un chemin d’accès local.</span><span class="sxs-lookup"><span data-stu-id="4e37f-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="4e37f-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4e37f-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="4e37f-127">Un chemin d’accès local est introuvable.</span><span class="sxs-lookup"><span data-stu-id="4e37f-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e37f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e37f-128">See also</span></span>



[<span data-ttu-id="4e37f-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="4e37f-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

