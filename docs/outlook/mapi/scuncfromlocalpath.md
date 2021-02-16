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
ms.openlocfilehash: b53dd9aaaf18dba5c7e33e0bc7d984de757634a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414535"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="45e80-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="45e80-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="45e80-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45e80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45e80-105">Recherche un chemin d’accès UNC (Universal Naming Convention) équivalent au chemin local donné.</span><span class="sxs-lookup"><span data-stu-id="45e80-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45e80-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="45e80-106">Header file:</span></span>  <br/> |<span data-ttu-id="45e80-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45e80-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="45e80-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="45e80-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="45e80-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="45e80-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="45e80-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="45e80-110">Called by:</span></span>  <br/> |<span data-ttu-id="45e80-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="45e80-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="45e80-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45e80-112">Parameters</span></span>

 <span data-ttu-id="45e80-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="45e80-113">_szLocal_</span></span>
  
> <span data-ttu-id="45e80-114">[in] Chemin d’accès au format [ _lecteur :_] \[ _chemin_] d’un fichier ou d’un répertoire.</span><span class="sxs-lookup"><span data-stu-id="45e80-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="45e80-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="45e80-115">_szUNC_</span></span>
  
> <span data-ttu-id="45e80-116">[out] Un chemin d’accès au format [ serveur ] partage ] chemin ] du même fichier ou répertoire que pour le \\  \[ paramètre \[  _szLocal._</span><span class="sxs-lookup"><span data-stu-id="45e80-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="45e80-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="45e80-117">_cchUNC_</span></span>
  
> <span data-ttu-id="45e80-118">[in] Taille de la mémoire tampon pour la chaîne de sortie.</span><span class="sxs-lookup"><span data-stu-id="45e80-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="45e80-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="45e80-119">Return value</span></span>

<span data-ttu-id="45e80-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="45e80-120">S_OK</span></span>
  
> <span data-ttu-id="45e80-121">L’équivalent du chemin d’accès UNC a été localisé avec succès.</span><span class="sxs-lookup"><span data-stu-id="45e80-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="45e80-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="45e80-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="45e80-123">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="45e80-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="45e80-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="45e80-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="45e80-125">_szUNC_ n’était pas assez grand pour contenir le résultat.</span><span class="sxs-lookup"><span data-stu-id="45e80-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="45e80-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="45e80-126">S_FALSE</span></span>
  
> <span data-ttu-id="45e80-127">Le chemin d’accès local était déjà une chaîne UNC.</span><span class="sxs-lookup"><span data-stu-id="45e80-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45e80-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45e80-128">See also</span></span>



[<span data-ttu-id="45e80-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="45e80-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

