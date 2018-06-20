---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4f9d2f4d271e467d8fac32b8f17faa8f66cd3f99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783641"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="8b6fd-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="8b6fd-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="8b6fd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8b6fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8b6fd-105">Définit un nouveau chemin d’accès de la recherche dans le profil qui est utilisé pour le processus de résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="8b6fd-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="8b6fd-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="8b6fd-106">Parameters</span></span>

 <span data-ttu-id="8b6fd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8b6fd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8b6fd-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="8b6fd-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8b6fd-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="8b6fd-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="8b6fd-110">[in] Pointeur vers la structure [SRowSet](srowset.md) utilisée pour contenir le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="8b6fd-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="8b6fd-111">La première propriété de chaque membre **: UGAL** dans **SRowSet** doit être **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8b6fd-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8b6fd-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8b6fd-112">Return value</span></span>

<span data-ttu-id="8b6fd-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b6fd-113">S_OK</span></span> 
  
> <span data-ttu-id="8b6fd-114">Le chemin de recherche a été défini.</span><span class="sxs-lookup"><span data-stu-id="8b6fd-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="8b6fd-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="8b6fd-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="8b6fd-116">Un des conteneurs décrites dans la structure **SRowSet** ne comprend pas sa propriété **PR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="8b6fd-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8b6fd-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b6fd-117">Remarks</span></span>

<span data-ttu-id="8b6fd-118">Clients et fournisseurs de services appellent la méthode **SetSearchPath** pour enregistrer les modifications qui ont été apportées à l’ordre de recherche du conteneur qui est utilisé pour résoudre les noms avec la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="8b6fd-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="8b6fd-119">Le chemin d’accès de la recherche est enregistrée entre des instances d’une session.</span><span class="sxs-lookup"><span data-stu-id="8b6fd-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="8b6fd-120">Clients et fournisseurs n’ont pas d’appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour conserver les modifications de chemin d’accès de recherche.</span><span class="sxs-lookup"><span data-stu-id="8b6fd-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b6fd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b6fd-121">See also</span></span>



[<span data-ttu-id="8b6fd-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="8b6fd-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="8b6fd-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="8b6fd-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="8b6fd-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="8b6fd-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="8b6fd-125">Propriété canonique PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="8b6fd-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="8b6fd-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8b6fd-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

