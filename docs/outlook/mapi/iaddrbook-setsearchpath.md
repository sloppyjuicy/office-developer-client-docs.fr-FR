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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8611249207811446ae47f056486ec498bf1e7eab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349307"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="a6072-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="a6072-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="a6072-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6072-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6072-105">Définit un nouveau chemin de recherche dans le profil qui est utilisé pour le processus de résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="a6072-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="a6072-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6072-106">Parameters</span></span>

 <span data-ttu-id="a6072-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6072-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a6072-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="a6072-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a6072-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="a6072-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="a6072-110">dans Pointeur vers la structure [SRowSet](srowset.md) utilisée pour conserver le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="a6072-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="a6072-111">La première propriété pour chaque membre du **aRow** dans **SRowSet** doit être **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a6072-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6072-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a6072-112">Return value</span></span>

<span data-ttu-id="a6072-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6072-113">S_OK</span></span> 
  
> <span data-ttu-id="a6072-114">Le chemin de recherche a été correctement défini.</span><span class="sxs-lookup"><span data-stu-id="a6072-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="a6072-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="a6072-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="a6072-116">L'un des conteneurs décrits dans la structure **SRowSet** n'inclut pas sa propriété **PR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="a6072-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a6072-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="a6072-117">Remarks</span></span>

<span data-ttu-id="a6072-118">Les clients et les fournisseurs de services appellent la méthode **SetSearchPath** pour enregistrer les modifications apportées à l'ordre de recherche de conteneur utilisé pour résoudre les noms à l'aide de la méthode [IAddrBook:: ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="a6072-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="a6072-119">Le chemin de recherche est enregistré entre les instances d'une session.</span><span class="sxs-lookup"><span data-stu-id="a6072-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="a6072-120">Les clients et les fournisseurs n'ont pas besoin d'appeler la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) pour faire en sorte que le chemin de recherche change définitivement.</span><span class="sxs-lookup"><span data-stu-id="a6072-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6072-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6072-121">See also</span></span>



[<span data-ttu-id="a6072-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="a6072-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="a6072-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="a6072-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="a6072-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="a6072-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="a6072-125">Propriété canonique PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="a6072-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="a6072-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a6072-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

