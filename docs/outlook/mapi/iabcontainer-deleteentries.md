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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e3b238129e55e03da33ef3af75ecce7e73fbad03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339381"
---
# <a name="iabcontainerdeleteentries"></a><span data-ttu-id="78b67-103">IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="78b67-103">IABContainer::DeleteEntries</span></span>

  
  
<span data-ttu-id="78b67-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78b67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78b67-105">Supprime une ou plusieurs entrées, généralement les utilisateurs de messagerie, les listes de distribution ou d'autres conteneurs.</span><span class="sxs-lookup"><span data-stu-id="78b67-105">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="78b67-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78b67-106">Parameters</span></span>

 <span data-ttu-id="78b67-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="78b67-107">_lpEntries_</span></span>
  
> <span data-ttu-id="78b67-108">dans Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui contiennent des identificateurs d'entrée qui représentent les entrées en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="78b67-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contain entry identifiers that represent the entries being deleted.</span></span> 
    
 <span data-ttu-id="78b67-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78b67-109">_ulFlags_</span></span>
  
> <span data-ttu-id="78b67-110">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="78b67-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78b67-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="78b67-111">Return value</span></span>

<span data-ttu-id="78b67-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="78b67-112">S_OK</span></span> 
  
> <span data-ttu-id="78b67-113">Les entrées spécifiées ont été correctement supprimées.</span><span class="sxs-lookup"><span data-stu-id="78b67-113">The specified entries have been successfully deleted.</span></span> 
    
<span data-ttu-id="78b67-114">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="78b67-114">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="78b67-115">L'appel a réussi, mais une ou plusieurs entrées n'ont pas pu être supprimées.</span><span class="sxs-lookup"><span data-stu-id="78b67-115">The call succeeded, but one or more of the entries could not be deleted.</span></span> <span data-ttu-id="78b67-116">Lorsque cette valeur est renvoyée, l'appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="78b67-116">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="78b67-117">Pour tester cette valeur, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="78b67-117">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="78b67-118">Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="78b67-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="78b67-119">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="78b67-119">MFCMAPI reference</span></span>

<span data-ttu-id="78b67-120">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="78b67-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="78b67-121">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="78b67-121">**File**</span></span>|<span data-ttu-id="78b67-122">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="78b67-122">**Function**</span></span>|<span data-ttu-id="78b67-123">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="78b67-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="78b67-124">Abdlg. cpp</span><span class="sxs-lookup"><span data-stu-id="78b67-124">Abdlg.cpp</span></span>  <br/> |<span data-ttu-id="78b67-125">CabDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="78b67-125">CabDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="78b67-126">MFCMAPI utilise la méthode **DeleteEntries** pour supprimer une entrée spécifique d'un conteneur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="78b67-126">MFCMAPI uses the **DeleteEntries** method to delete a specific entry from an address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78b67-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78b67-127">See also</span></span>



[<span data-ttu-id="78b67-128">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="78b67-128">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)


[<span data-ttu-id="78b67-129">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="78b67-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

