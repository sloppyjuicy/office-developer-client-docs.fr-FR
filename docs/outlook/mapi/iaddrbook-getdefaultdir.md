---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a9f0fac76f06bd638aeff89ff096507209cc0287
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568454"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="e0b94-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="e0b94-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="e0b94-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0b94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0b94-105">Renvoie l’identificateur d’entrée pour le conteneur de carnet d’adresses initiale.</span><span class="sxs-lookup"><span data-stu-id="e0b94-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e0b94-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0b94-106">Parameters</span></span>

 <span data-ttu-id="e0b94-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e0b94-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="e0b94-108">[out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e0b94-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e0b94-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="e0b94-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="e0b94-110">[out] Pointeur vers un pointeur vers l’identificateur d’entrée du conteneur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e0b94-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0b94-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e0b94-111">Return value</span></span>

<span data-ttu-id="e0b94-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0b94-112">S_OK</span></span> 
  
> <span data-ttu-id="e0b94-113">L’identificateur d’entrée du conteneur par défaut a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e0b94-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0b94-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0b94-114">Remarks</span></span>

<span data-ttu-id="e0b94-115">Fournisseurs de services et applications clientes appellent la méthode **GetDefaultDir** pour récupérer l’identificateur d’entrée du conteneur de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="e0b94-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="e0b94-116">Le conteneur par défaut est ce que l’utilisateur voit affiché dans le carnet d’adresses lors de la première ouverture du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="e0b94-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="e0b94-117">Si un conteneur par défaut n’a pas été défini par un appel à la méthode [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) , MAPI affecte en tant que le conteneur par défaut le premier conteneur avec des noms qui n’est pas le carnet d’adresses personnel (CAP).</span><span class="sxs-lookup"><span data-stu-id="e0b94-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="e0b94-118">Si le conteneur est introuvable, le carnet d’adresses personnel devient le conteneur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e0b94-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="e0b94-119">Pour définir la valeur par défaut directory, un client ou un fournisseur appelle la méthode **SetDefaultDir** .</span><span class="sxs-lookup"><span data-stu-id="e0b94-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="e0b94-120">Clients et fournisseurs n’ont pas d’appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ; Étant donné que les modifications apportées au carnet d’adresses ne sont pas traitées, les modifications sont apportées immédiatement définitive.</span><span class="sxs-lookup"><span data-stu-id="e0b94-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e0b94-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e0b94-121">MFCMAPI reference</span></span>

<span data-ttu-id="e0b94-122">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e0b94-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e0b94-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e0b94-123">**File**</span></span>|<span data-ttu-id="e0b94-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e0b94-124">**Function**</span></span>|<span data-ttu-id="e0b94-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e0b94-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0b94-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e0b94-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="e0b94-127">CMainDlg::OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="e0b94-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="e0b94-128">MFCMAPI utilise la méthode **GetDefaultDir** pour obtenir l’ID pour le conteneur de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="e0b94-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0b94-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0b94-129">See also</span></span>



[<span data-ttu-id="e0b94-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="e0b94-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="e0b94-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e0b94-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e0b94-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e0b94-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e0b94-133">Propriété canonique PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="e0b94-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="e0b94-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e0b94-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="e0b94-135">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e0b94-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

