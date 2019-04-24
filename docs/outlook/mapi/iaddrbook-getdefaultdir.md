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
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336693"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="44cb1-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="44cb1-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="44cb1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44cb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44cb1-105">Renvoie l'identificateur d'entrée pour le conteneur de carnet d'adresses initial.</span><span class="sxs-lookup"><span data-stu-id="44cb1-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="44cb1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44cb1-106">Parameters</span></span>

 <span data-ttu-id="44cb1-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="44cb1-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="44cb1-108">remarquer Pointeur vers le nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="44cb1-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="44cb1-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="44cb1-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="44cb1-110">remarquer Pointeur vers un pointeur vers l'identificateur d'entrée du conteneur par défaut.</span><span class="sxs-lookup"><span data-stu-id="44cb1-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="44cb1-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="44cb1-111">Return value</span></span>

<span data-ttu-id="44cb1-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="44cb1-112">S_OK</span></span> 
  
> <span data-ttu-id="44cb1-113">L'identificateur d'entrée du conteneur par défaut a été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="44cb1-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44cb1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="44cb1-114">Remarks</span></span>

<span data-ttu-id="44cb1-115">Les applications clientes et les fournisseurs de services appellent la méthode **GetDefaultDir** pour récupérer l'identificateur d'entrée du conteneur de carnet d'adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="44cb1-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="44cb1-116">Le conteneur par défaut est ce que l'utilisateur voit affiché dans le carnet d'adresses lors de la première ouverture du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="44cb1-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="44cb1-117">Si un conteneur par défaut n'a pas été défini par un appel à la méthode [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md) , MAPI affecte comme conteneur par défaut le premier conteneur avec des noms qui ne sont pas le carnet d'adresses personnel (PAB).</span><span class="sxs-lookup"><span data-stu-id="44cb1-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="44cb1-118">Si un tel conteneur est introuvable, le PAB devient le conteneur par défaut.</span><span class="sxs-lookup"><span data-stu-id="44cb1-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="44cb1-119">Pour définir le répertoire par défaut, un client ou un fournisseur appelle la méthode **SetDefaultDir** .</span><span class="sxs-lookup"><span data-stu-id="44cb1-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="44cb1-120">Les clients et les fournisseurs n'ont pas besoin d'appeler la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ; étant donné que les modifications apportées au carnet d'adresses ne sont pas traitées, les modifications sont immédiatement rendues permanentes.</span><span class="sxs-lookup"><span data-stu-id="44cb1-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="44cb1-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="44cb1-121">MFCMAPI reference</span></span>

<span data-ttu-id="44cb1-122">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="44cb1-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="44cb1-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="44cb1-123">**File**</span></span>|<span data-ttu-id="44cb1-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="44cb1-124">**Function**</span></span>|<span data-ttu-id="44cb1-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="44cb1-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="44cb1-126">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="44cb1-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="44cb1-127">CMainDlg:: OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="44cb1-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="44cb1-128">MFCMAPI utilise la méthode **GetDefaultDir** pour obtenir l'ID du conteneur de carnet d'adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="44cb1-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44cb1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44cb1-129">See also</span></span>



[<span data-ttu-id="44cb1-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="44cb1-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="44cb1-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="44cb1-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="44cb1-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="44cb1-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="44cb1-133">Propriété canonique PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="44cb1-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="44cb1-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="44cb1-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="44cb1-135">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="44cb1-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

