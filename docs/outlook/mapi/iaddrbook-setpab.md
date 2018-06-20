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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3f13a4d278b85ffae33e8f44f3a15eb499fb11b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783646"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="e8a53-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="e8a53-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="e8a53-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e8a53-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e8a53-105">Désigne un conteneur spécifique comme le carnet d’adresses personnel (CAP).</span><span class="sxs-lookup"><span data-stu-id="e8a53-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e8a53-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8a53-106">Parameters</span></span>

 <span data-ttu-id="e8a53-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e8a53-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="e8a53-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e8a53-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e8a53-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e8a53-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="e8a53-110">[in] Pointeur vers l’identificateur d’entrée du conteneur à désigner comme le carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="e8a53-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="e8a53-111">Le paramètre _lpEntryID_ ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="e8a53-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e8a53-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e8a53-112">Return value</span></span>

<span data-ttu-id="e8a53-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8a53-113">S_OK</span></span> 
  
> <span data-ttu-id="e8a53-114">Le conteneur spécifié a été établi en tant que le carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="e8a53-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8a53-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8a53-115">Remarks</span></span>

<span data-ttu-id="e8a53-116">Clients et fournisseurs de services appellent la méthode **SetPAB** pour désigner un conteneur spécifique comme le carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="e8a53-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="e8a53-117">Le carnet d’adresses personnel est un conteneur qui se compose d’entrées copiées à partir d’autres conteneurs, ainsi que les nouvelles entrées.</span><span class="sxs-lookup"><span data-stu-id="e8a53-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="e8a53-118">Un appel à **SetPAB** établit un conteneur en tant que le carnet d’adresses personnel jusqu'à ce que ce conteneur devient indisponible, ou un nouveau conteneur devient le carnet d’adresses personnel via un autre appel à **SetPAB**.</span><span class="sxs-lookup"><span data-stu-id="e8a53-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="e8a53-119">Clients et fournisseurs n’ont pas d’appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour conserver le changement de carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="e8a53-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e8a53-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e8a53-120">MFCMAPI reference</span></span>

<span data-ttu-id="e8a53-121">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e8a53-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e8a53-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e8a53-122">**File**</span></span>|<span data-ttu-id="e8a53-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e8a53-123">**Function**</span></span>|<span data-ttu-id="e8a53-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e8a53-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e8a53-125">AbContDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e8a53-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="e8a53-126">CAbContDlg::OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="e8a53-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="e8a53-127">MFCMAPI utilise la méthode **SetPAB** pour effectuer le conteneur spécifié le carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="e8a53-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8a53-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8a53-128">See also</span></span>



[<span data-ttu-id="e8a53-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="e8a53-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="e8a53-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="e8a53-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="e8a53-131">Propriété canonique PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="e8a53-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="e8a53-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e8a53-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="e8a53-133">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e8a53-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

