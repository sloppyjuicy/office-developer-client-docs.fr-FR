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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7309f65965fe3c88f927eeba0bbcccff97c479af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783629"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="3dbe6-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="3dbe6-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="3dbe6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3dbe6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3dbe6-105">Renvoie l’identificateur d’entrée pour le conteneur de carnet d’adresses initiale.</span><span class="sxs-lookup"><span data-stu-id="3dbe6-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="3dbe6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3dbe6-106">Parameters</span></span>

 <span data-ttu-id="3dbe6-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3dbe6-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="3dbe6-108">[out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="3dbe6-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3dbe6-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="3dbe6-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="3dbe6-110">[out] Pointeur vers un pointeur vers l’identificateur d’entrée du conteneur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3dbe6-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3dbe6-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3dbe6-111">Return value</span></span>

<span data-ttu-id="3dbe6-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="3dbe6-112">S_OK</span></span> 
  
> <span data-ttu-id="3dbe6-113">L’identificateur d’entrée du conteneur par défaut a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="3dbe6-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3dbe6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3dbe6-114">Remarks</span></span>

<span data-ttu-id="3dbe6-115">Fournisseurs de services et applications clientes appellent la méthode **GetDefaultDir** pour récupérer l’identificateur d’entrée du conteneur de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="3dbe6-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="3dbe6-116">Le conteneur par défaut est ce que l’utilisateur voit affiché dans le carnet d’adresses lors de la première ouverture du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3dbe6-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="3dbe6-117">Si un conteneur par défaut n’a pas été défini par un appel à la méthode [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) , MAPI affecte en tant que le conteneur par défaut le premier conteneur avec des noms qui n’est pas le carnet d’adresses personnel (CAP).</span><span class="sxs-lookup"><span data-stu-id="3dbe6-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="3dbe6-118">Si le conteneur est introuvable, le carnet d’adresses personnel devient le conteneur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3dbe6-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="3dbe6-119">Pour définir la valeur par défaut directory, un client ou un fournisseur appelle la méthode **SetDefaultDir** .</span><span class="sxs-lookup"><span data-stu-id="3dbe6-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="3dbe6-120">Clients et fournisseurs n’ont pas d’appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ; Étant donné que les modifications apportées au carnet d’adresses ne sont pas traitées, les modifications sont apportées immédiatement définitive.</span><span class="sxs-lookup"><span data-stu-id="3dbe6-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3dbe6-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3dbe6-121">MFCMAPI reference</span></span>

<span data-ttu-id="3dbe6-122">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3dbe6-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3dbe6-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="3dbe6-123">**File**</span></span>|<span data-ttu-id="3dbe6-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="3dbe6-124">**Function**</span></span>|<span data-ttu-id="3dbe6-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="3dbe6-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3dbe6-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3dbe6-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="3dbe6-127">CMainDlg::OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="3dbe6-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="3dbe6-128">MFCMAPI utilise la méthode **GetDefaultDir** pour obtenir l’ID pour le conteneur de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="3dbe6-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3dbe6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dbe6-129">See also</span></span>



[<span data-ttu-id="3dbe6-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="3dbe6-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="3dbe6-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3dbe6-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3dbe6-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3dbe6-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3dbe6-133">Propriété canonique PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="3dbe6-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="3dbe6-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3dbe6-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="3dbe6-135">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="3dbe6-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

