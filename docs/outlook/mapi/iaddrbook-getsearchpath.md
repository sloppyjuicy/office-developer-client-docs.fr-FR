---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412981"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="d68c5-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="d68c5-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="d68c5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d68c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d68c5-105">Renvoie une liste triée des identificateurs d’entrée des conteneurs à inclure dans le processus de résolution de noms initié par la méthode [IAddrBook::ResolveName.](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="d68c5-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="d68c5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d68c5-106">Parameters</span></span>

 <span data-ttu-id="d68c5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d68c5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d68c5-108">[in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées dans le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="d68c5-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="d68c5-109">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="d68c5-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d68c5-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d68c5-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d68c5-111">Les chaînes renvoyées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="d68c5-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="d68c5-112">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="d68c5-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d68c5-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="d68c5-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="d68c5-114">[out] Pointeur vers un pointeur vers une liste ordonnée d’identificateurs d’entrée de conteneur.</span><span class="sxs-lookup"><span data-stu-id="d68c5-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="d68c5-115">**GetSearchPath stocke** la liste ordonnée dans une structure [SRowSet.](srowset.md)</span><span class="sxs-lookup"><span data-stu-id="d68c5-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="d68c5-116">S’il n’existe aucun conteneur dans la hiérarchie du carnet d’adresses, zéro est renvoyé dans la structure **SRowSet.**</span><span class="sxs-lookup"><span data-stu-id="d68c5-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d68c5-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d68c5-117">Return value</span></span>

<span data-ttu-id="d68c5-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d68c5-118">S_OK</span></span> 
  
> <span data-ttu-id="d68c5-119">Le chemin de recherche a été récupéré avec succès.</span><span class="sxs-lookup"><span data-stu-id="d68c5-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d68c5-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="d68c5-120">Remarks</span></span>

<span data-ttu-id="d68c5-121">Les clients et les fournisseurs de services appellent la **méthode GetSearchPath** pour obtenir le chemin de recherche utilisé pour résoudre les noms avec **la méthode ResolveName.**</span><span class="sxs-lookup"><span data-stu-id="d68c5-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="d68c5-122">En règle générale, les clients appellent la méthode [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) pour établir un chemin de recherche de conteneur dans le profil avant d’appeler **GetSearchPath** pour le récupérer.</span><span class="sxs-lookup"><span data-stu-id="d68c5-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="d68c5-123">Toutefois, **l’appel de SetSearchPath** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="d68c5-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="d68c5-124">Si **SetSearchPath n’a** jamais été appelé, **GetSearchPath** crée un chemin d’accès en passant par les tables hiérarchiques du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="d68c5-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="d68c5-125">Le chemin de recherche par défaut établi par **GetSearchPath** se compose des conteneurs suivants dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="d68c5-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="d68c5-126">Premier conteneur avec autorisation de lecture/écriture, généralement le carnet d’adresses personnel .</span><span class="sxs-lookup"><span data-stu-id="d68c5-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="d68c5-127">Chaque conteneur dont la propriété **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) est définie sur DT_GLOBAL.</span><span class="sxs-lookup"><span data-stu-id="d68c5-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="d68c5-128">Ce paramètre indique que le conteneur contient des destinataires.</span><span class="sxs-lookup"><span data-stu-id="d68c5-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="d68c5-129">Conteneur désigné comme conteneur par défaut, s’il n’existe aucun conteneur dont l’indicateur DT_GLOBAL est définie dans sa propriété **PR_DISPLAY_TYPE** et que le conteneur par défaut diffère du premier conteneur avec une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d68c5-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="d68c5-130">Si **SetSearchPath** a été appelé, **GetSearchPath** crée un chemin d’accès à l’aide des conteneurs de carnet d’adresses qui ont été stockés dans le profil.</span><span class="sxs-lookup"><span data-stu-id="d68c5-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="d68c5-131">**GetSearchPath** valide ce chemin d’accès avant de le retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="d68c5-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="d68c5-132">Après le premier appel à **SetSearchPath**, les appels suivants à **SetSearchPath** doivent être utilisés pour modifier le chemin de recherche renvoyé par **GetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="d68c5-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="d68c5-133">En d’autres termes, le client ou le fournisseur appelant ne reçoit pas le chemin de recherche par défaut après le premier appel **à SetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="d68c5-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d68c5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d68c5-134">See also</span></span>



[<span data-ttu-id="d68c5-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="d68c5-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="d68c5-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="d68c5-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="d68c5-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d68c5-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

