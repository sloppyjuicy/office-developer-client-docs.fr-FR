---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419897"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="91a43-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="91a43-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="91a43-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91a43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91a43-105">Renvoie l’identificateur d’entrée du conteneur désigné comme carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="91a43-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="91a43-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="91a43-106">Parameters</span></span>

 <span data-ttu-id="91a43-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="91a43-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="91a43-108">[out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par _le paramètre lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="91a43-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="91a43-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="91a43-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="91a43-110">[out] Pointeur vers un pointeur vers l’identificateur d’entrée du PAB.</span><span class="sxs-lookup"><span data-stu-id="91a43-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="91a43-111">Le  _paramètre lppEntryID_ contient zéro si aucun conteneur n’a été désigné comme PAB.</span><span class="sxs-lookup"><span data-stu-id="91a43-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="91a43-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="91a43-112">Return value</span></span>

<span data-ttu-id="91a43-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="91a43-113">S_OK</span></span> 
  
> <span data-ttu-id="91a43-114">L’identificateur d’entrée du PAB a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="91a43-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91a43-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="91a43-115">Remarks</span></span>

<span data-ttu-id="91a43-116">Les clients appellent **la méthode GetPAB** pour récupérer l’identificateur d’entrée du conteneur désigné comme PAB.</span><span class="sxs-lookup"><span data-stu-id="91a43-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="91a43-117">Si un carnet d’adresses en mode page n’a pas été établi dans le profil, MAPI sélectionne comme carnet d’adresses en mode page le premier conteneur de la hiérarchie de carnet d’adresses qui autorise les modifications.</span><span class="sxs-lookup"><span data-stu-id="91a43-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="91a43-118">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="91a43-118">MFCMAPI reference</span></span>

<span data-ttu-id="91a43-119">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="91a43-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="91a43-120">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="91a43-120">**File**</span></span>|<span data-ttu-id="91a43-121">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="91a43-121">**Function**</span></span>|<span data-ttu-id="91a43-122">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="91a43-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="91a43-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="91a43-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="91a43-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="91a43-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="91a43-125">MFCMAPI utilise la **méthode GetPAB** pour obtenir l’ID du carnet d’adresses personnel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="91a43-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91a43-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91a43-126">See also</span></span>



[<span data-ttu-id="91a43-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="91a43-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="91a43-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="91a43-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="91a43-129">Propriété canonique PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="91a43-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="91a43-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="91a43-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="91a43-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="91a43-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

