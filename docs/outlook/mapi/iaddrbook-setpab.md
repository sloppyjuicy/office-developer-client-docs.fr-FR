---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424615"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="7acbd-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="7acbd-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="7acbd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7acbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7acbd-105">Désigne un conteneur particulier comme carnet d'adresses personnel (PAB).</span><span class="sxs-lookup"><span data-stu-id="7acbd-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="7acbd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7acbd-106">Parameters</span></span>

 <span data-ttu-id="7acbd-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7acbd-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7acbd-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7acbd-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7acbd-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7acbd-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7acbd-110">dans Pointeur vers l'identificateur d'entrée du conteneur à désigner comme PAB.</span><span class="sxs-lookup"><span data-stu-id="7acbd-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="7acbd-111">Le paramètre _lpEntryID_ ne peut pas être null.</span><span class="sxs-lookup"><span data-stu-id="7acbd-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7acbd-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7acbd-112">Return value</span></span>

<span data-ttu-id="7acbd-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7acbd-113">S_OK</span></span> 
  
> <span data-ttu-id="7acbd-114">Le conteneur spécifié a été défini en tant que PAB.</span><span class="sxs-lookup"><span data-stu-id="7acbd-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7acbd-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="7acbd-115">Remarks</span></span>

<span data-ttu-id="7acbd-116">Les clients et les fournisseurs de services appellent la méthode **SetPAB** pour désigner un conteneur particulier comme PAB.</span><span class="sxs-lookup"><span data-stu-id="7acbd-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="7acbd-117">Le PAB est un conteneur qui se compose d'entrées copiées à partir d'autres conteneurs, ainsi que de nouvelles entrées.</span><span class="sxs-lookup"><span data-stu-id="7acbd-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="7acbd-118">Un appel à **SetPAB** établit un conteneur en tant que PAB jusqu'à ce que ce conteneur soit rendu indisponible ou qu'un nouveau conteneur devienne le PAB via un appel ultérieur à **SetPAB**.</span><span class="sxs-lookup"><span data-stu-id="7acbd-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="7acbd-119">Les clients et les fournisseurs n'ont pas besoin d'appeler la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) pour que le carnet d'un PAB change de façon permanente.</span><span class="sxs-lookup"><span data-stu-id="7acbd-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7acbd-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7acbd-120">MFCMAPI reference</span></span>

<span data-ttu-id="7acbd-121">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7acbd-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7acbd-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="7acbd-122">**File**</span></span>|<span data-ttu-id="7acbd-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="7acbd-123">**Function**</span></span>|<span data-ttu-id="7acbd-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="7acbd-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7acbd-125">AbContDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="7acbd-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="7acbd-126">CAbContDlg:: OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="7acbd-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="7acbd-127">MFCMAPI utilise la méthode **SetPAB** pour définir le conteneur spécifié comme PAB.</span><span class="sxs-lookup"><span data-stu-id="7acbd-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7acbd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7acbd-128">See also</span></span>



[<span data-ttu-id="7acbd-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="7acbd-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="7acbd-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="7acbd-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="7acbd-131">Propriété canonique PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="7acbd-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="7acbd-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7acbd-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="7acbd-133">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="7acbd-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

