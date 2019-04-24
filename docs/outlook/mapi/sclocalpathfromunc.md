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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351246"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="e5f08-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="e5f08-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="e5f08-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5f08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5f08-105">Localise un chemin d'accès local équivalent au chemin d'accès UNC (Universal Naming Convention) donné.</span><span class="sxs-lookup"><span data-stu-id="e5f08-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5f08-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e5f08-106">Header file:</span></span>  <br/> |<span data-ttu-id="e5f08-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="e5f08-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e5f08-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e5f08-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e5f08-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e5f08-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e5f08-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e5f08-110">Called by:</span></span>  <br/> |<span data-ttu-id="e5f08-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e5f08-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="e5f08-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5f08-112">Parameters</span></span>

 <span data-ttu-id="e5f08-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="e5f08-113">_szUNC_</span></span>
  
> <span data-ttu-id="e5f08-114">dans Un chemin d'accès au \\format [ _Server_]\[ _share_]\[ _path_] d'un fichier ou d'un répertoire.</span><span class="sxs-lookup"><span data-stu-id="e5f08-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="e5f08-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="e5f08-115">_szLocal_</span></span>
  
> <span data-ttu-id="e5f08-116">remarquer Un chemin d'accès au format [ _lecteur:_]\[ _chemin d'accès_] du même fichier ou répertoire que le paramètre _szUNC_ .</span><span class="sxs-lookup"><span data-stu-id="e5f08-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="e5f08-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="e5f08-117">_cchLocal_</span></span>
  
> <span data-ttu-id="e5f08-118">dans Taille de la mémoire tampon pour la chaîne de sortie.</span><span class="sxs-lookup"><span data-stu-id="e5f08-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5f08-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e5f08-119">Return value</span></span>

<span data-ttu-id="e5f08-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5f08-120">S_OK</span></span>
  
> <span data-ttu-id="e5f08-121">Un chemin d'accès local a été correctement localisé.</span><span class="sxs-lookup"><span data-stu-id="e5f08-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="e5f08-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="e5f08-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="e5f08-123">_szLocal_ n'était pas assez grand pour contenir le résultat.</span><span class="sxs-lookup"><span data-stu-id="e5f08-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="e5f08-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e5f08-124">S_FALSE</span></span>
  
> <span data-ttu-id="e5f08-125">La chaîne UNC était déjà un chemin d'accès local.</span><span class="sxs-lookup"><span data-stu-id="e5f08-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="e5f08-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e5f08-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="e5f08-127">Un chemin d'accès local est introuvable.</span><span class="sxs-lookup"><span data-stu-id="e5f08-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5f08-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5f08-128">See also</span></span>



[<span data-ttu-id="e5f08-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="e5f08-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

