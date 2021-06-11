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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432232"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="36068-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="36068-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="36068-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36068-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36068-105">Recherche un chemin d’accès local équivalent au chemin d’accès UNC (Universal Naming Convention) donné.</span><span class="sxs-lookup"><span data-stu-id="36068-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36068-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="36068-106">Header file:</span></span>  <br/> |<span data-ttu-id="36068-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="36068-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="36068-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="36068-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="36068-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="36068-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="36068-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="36068-110">Called by:</span></span>  <br/> |<span data-ttu-id="36068-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="36068-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="36068-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="36068-112">Parameters</span></span>

 <span data-ttu-id="36068-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="36068-113">_szUNC_</span></span>
  
> <span data-ttu-id="36068-114">[in] Un chemin d’accès au format \\ [ _serveur_] \[ _partage_] \[ _chemin_] d’un fichier ou d’un répertoire.</span><span class="sxs-lookup"><span data-stu-id="36068-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="36068-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="36068-115">_szLocal_</span></span>
  
> <span data-ttu-id="36068-116">[out] Chemin d’accès au format [ _lecteur :_] chemin ] du même fichier ou répertoire que pour le \[ paramètre _szUNC._</span><span class="sxs-lookup"><span data-stu-id="36068-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="36068-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="36068-117">_cchLocal_</span></span>
  
> <span data-ttu-id="36068-118">[in] Taille de la mémoire tampon pour la chaîne de sortie.</span><span class="sxs-lookup"><span data-stu-id="36068-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36068-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="36068-119">Return value</span></span>

<span data-ttu-id="36068-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="36068-120">S_OK</span></span>
  
> <span data-ttu-id="36068-121">Un chemin d’accès local a été localisé.</span><span class="sxs-lookup"><span data-stu-id="36068-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="36068-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="36068-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="36068-123">_szLocal n’était_ pas assez grand pour contenir le résultat.</span><span class="sxs-lookup"><span data-stu-id="36068-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="36068-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="36068-124">S_FALSE</span></span>
  
> <span data-ttu-id="36068-125">La chaîne UNC était déjà un chemin d’accès local.</span><span class="sxs-lookup"><span data-stu-id="36068-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="36068-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="36068-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="36068-127">Un chemin d’accès local n’a pas été trouvé.</span><span class="sxs-lookup"><span data-stu-id="36068-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36068-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36068-128">See also</span></span>



[<span data-ttu-id="36068-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="36068-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

