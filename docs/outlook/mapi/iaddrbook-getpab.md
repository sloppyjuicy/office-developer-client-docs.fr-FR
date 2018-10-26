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
ms.openlocfilehash: 1f93ee653c9365488432c4e797b171a199c30107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583714"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="e1d75-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="e1d75-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="e1d75-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1d75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1d75-105">Renvoie l’identificateur d’entrée du conteneur qui est désigné comme le carnet d’adresses personnel (CAP).</span><span class="sxs-lookup"><span data-stu-id="e1d75-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e1d75-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1d75-106">Parameters</span></span>

 <span data-ttu-id="e1d75-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e1d75-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="e1d75-108">[out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e1d75-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e1d75-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="e1d75-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="e1d75-110">[out] Pointeur vers un pointeur vers l’identificateur d’entrée du carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="e1d75-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="e1d75-111">Le paramètre _lppEntryID_ contient zéro si aucun conteneur n’a été désigné comme le carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="e1d75-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e1d75-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e1d75-112">Return value</span></span>

<span data-ttu-id="e1d75-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1d75-113">S_OK</span></span> 
  
> <span data-ttu-id="e1d75-114">L’identificateur d’entrée du carnet d’adresses personnel a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e1d75-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1d75-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1d75-115">Remarks</span></span>

<span data-ttu-id="e1d75-116">Les clients appeler la méthode **GetPAB** pour récupérer l’identificateur d’entrée du conteneur désigné comme le carnet d’adresses personnel.</span><span class="sxs-lookup"><span data-stu-id="e1d75-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="e1d75-117">Si un carnet d’adresses personnel n’a pas été établie dans le profil, MAPI sélectionne comme le carnet d’adresses personnel le premier conteneur dans la hiérarchie de carnets d’adresses qui permet de modifier.</span><span class="sxs-lookup"><span data-stu-id="e1d75-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e1d75-118">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e1d75-118">MFCMAPI reference</span></span>

<span data-ttu-id="e1d75-119">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e1d75-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e1d75-120">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e1d75-120">**File**</span></span>|<span data-ttu-id="e1d75-121">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e1d75-121">**Function**</span></span>|<span data-ttu-id="e1d75-122">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e1d75-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1d75-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e1d75-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="e1d75-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="e1d75-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="e1d75-125">MFCMAPI utilise la méthode **GetPAB** pour obtenir l’ID de carnet d’adresses personnel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e1d75-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1d75-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1d75-126">See also</span></span>



[<span data-ttu-id="e1d75-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e1d75-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e1d75-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e1d75-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e1d75-129">Propriété canonique PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="e1d75-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="e1d75-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e1d75-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="e1d75-131">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e1d75-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

