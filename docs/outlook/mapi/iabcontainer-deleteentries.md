---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4140dc39b7f866b0372e5940aef5efc0524ad593
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573109"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="9f714-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="9f714-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="9f714-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f714-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f714-105">Supprime une ou plusieurs entrées, généralement autres conteneurs, listes de distribution ou les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9f714-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9f714-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f714-106">Parameters</span></span>

 <span data-ttu-id="9f714-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="9f714-107">_lpEntries_</span></span>
  
> <span data-ttu-id="9f714-108">[in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui contiennent des identificateurs d’entrée qui représentent les entrées en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="9f714-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="9f714-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f714-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9f714-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="9f714-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f714-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9f714-111">Return value</span></span>

<span data-ttu-id="9f714-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f714-112">S_OK</span></span> 
  
> <span data-ttu-id="9f714-113">Les entrées spécifiées ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="9f714-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="9f714-114">MAPI_W_PARTIAL_COMPLETION SE PRODUIT</span><span class="sxs-lookup"><span data-stu-id="9f714-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="9f714-115">L’appel a réussi, mais un ou plusieurs des entrées pas peuvent être supprimé.</span><span class="sxs-lookup"><span data-stu-id="9f714-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="9f714-116">Lorsque cette valeur est renvoyée, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="9f714-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="9f714-117">Pour tester cette valeur, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="9f714-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="9f714-118">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="9f714-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="9f714-119">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9f714-119">MFCMAPI reference</span></span>

<span data-ttu-id="9f714-120">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9f714-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9f714-121">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="9f714-121">**File**</span></span>|<span data-ttu-id="9f714-122">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="9f714-122">**Function**</span></span>|<span data-ttu-id="9f714-123">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="9f714-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9f714-124">Abdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9f714-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="9f714-125">CabDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="9f714-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="9f714-126">MFCMAPI utilise la méthode **DeleteEntries** pour supprimer une entrée spécifique à partir d’un conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="9f714-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9f714-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f714-127">See also</span></span>



[<span data-ttu-id="9f714-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9f714-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="9f714-129">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="9f714-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

