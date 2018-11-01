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
ms.openlocfilehash: 7bf69e560142ab282d6545389e02766389e4d018
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580697"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="51ece-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="51ece-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="51ece-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51ece-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51ece-105">Renvoie une liste triée des identificateurs d’entrée des conteneurs à inclure dans le processus de résolution de noms initié par la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="51ece-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="51ece-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="51ece-106">Parameters</span></span>

 <span data-ttu-id="51ece-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="51ece-107">_ulFlags_</span></span>
  
> <span data-ttu-id="51ece-108">[in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées dans le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="51ece-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="51ece-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="51ece-109">The following flag can be set:</span></span>
    
<span data-ttu-id="51ece-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="51ece-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="51ece-111">Les chaînes retournées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="51ece-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="51ece-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="51ece-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="51ece-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="51ece-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="51ece-114">[out] Pointeur vers un pointeur vers une liste triée des identificateurs d’entrée de conteneur.</span><span class="sxs-lookup"><span data-stu-id="51ece-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="51ece-115">**GetSearchPath** stocke la liste dans une structure [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="51ece-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="51ece-116">S’il n’y a aucun conteneur dans la hiérarchie de carnets d’adresses, zéro est retournée dans la structure **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="51ece-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="51ece-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="51ece-117">Return value</span></span>

<span data-ttu-id="51ece-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="51ece-118">S_OK</span></span> 
  
> <span data-ttu-id="51ece-119">Le chemin de recherche a été récupéré correctement.</span><span class="sxs-lookup"><span data-stu-id="51ece-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51ece-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="51ece-120">Remarks</span></span>

<span data-ttu-id="51ece-121">Clients et fournisseurs de services appellent la méthode **GetSearchPath** pour obtenir le chemin de recherche qui est utilisé pour résoudre les noms avec la méthode **ResolveName** .</span><span class="sxs-lookup"><span data-stu-id="51ece-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="51ece-122">En règle générale, les clients appellent la méthode de [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) pour établir un chemin de recherche du conteneur dans le profil avant d’appeler **GetSearchPath** pour récupérer.</span><span class="sxs-lookup"><span data-stu-id="51ece-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="51ece-123">Toutefois, l’appel de **SetSearchPath** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="51ece-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="51ece-124">Si **SetSearchPath** n’a jamais été appelée, **GetSearchPath** génère un chemin d’accès en passant par l’adresse de tables de hiérarchie du livre.</span><span class="sxs-lookup"><span data-stu-id="51ece-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="51ece-125">Le chemin de recherche par défaut ouverte par **GetSearchPath** se compose des conteneurs suivants dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="51ece-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="51ece-126">Le premier conteneur avec l’autorisation de lecture/écriture, généralement le carnet d’adresses personnel (CAP).</span><span class="sxs-lookup"><span data-stu-id="51ece-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="51ece-127">Chaque conteneur dont la propriété **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) la valeur DT_GLOBAL.</span><span class="sxs-lookup"><span data-stu-id="51ece-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="51ece-128">Ce paramètre indique que le conteneur contient des destinataires.</span><span class="sxs-lookup"><span data-stu-id="51ece-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="51ece-129">Le conteneur désigné en tant que la valeur par défaut, s’il n’existe aucun conteneur dont l’indicateur DT_GLOBAL dans leur propriété **PR_DISPLAY_TYPE** et le conteneur par défaut diffère du premier conteneur disposant d’une autorisation en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="51ece-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="51ece-130">Si **SetSearchPath** a été appelée, **GetSearchPath** génère un chemin d’accès en utilisant les conteneurs du carnet d’adresses qui ont été stockées dans le profil.</span><span class="sxs-lookup"><span data-stu-id="51ece-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="51ece-131">**GetSearchPath** valide ce chemin d’accès avant qu’il renvoie à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="51ece-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="51ece-132">Après le premier appel à **SetSearchPath**, les appels suivants de **SetSearchPath** permet de modifier le chemin d’accès de la recherche renvoyé par **GetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="51ece-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="51ece-133">En d’autres termes, le client ou le fournisseur appelant ne reçoit pas le chemin d’accès de la recherche par défaut après le premier appel à **SetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="51ece-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="51ece-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51ece-134">See also</span></span>



[<span data-ttu-id="51ece-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="51ece-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="51ece-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="51ece-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="51ece-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="51ece-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

