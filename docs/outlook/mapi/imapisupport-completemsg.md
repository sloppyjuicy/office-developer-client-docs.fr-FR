---
title: IMAPISupportCompleteMsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331506"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="b115b-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="b115b-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="b115b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b115b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b115b-105">Effectue un post-traitement sur un message.</span><span class="sxs-lookup"><span data-stu-id="b115b-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="b115b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b115b-106">Parameters</span></span>

 <span data-ttu-id="b115b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b115b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b115b-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="b115b-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b115b-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b115b-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="b115b-110">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b115b-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b115b-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b115b-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="b115b-112">dans Pointeur vers l'identificateur d'entrée du message à traiter.</span><span class="sxs-lookup"><span data-stu-id="b115b-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b115b-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b115b-113">Return value</span></span>

<span data-ttu-id="b115b-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="b115b-114">S_OK</span></span> 
  
> <span data-ttu-id="b115b-115">Le post-traitement a réussi.</span><span class="sxs-lookup"><span data-stu-id="b115b-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b115b-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b115b-116">Remarks</span></span>

<span data-ttu-id="b115b-117">La méthode **IMAPISupport:: CompleteMsg** est implémentée pour les objets de prise en charge du fournisseur de banque de messages et est appelée uniquement par les fournisseurs de banques de messages étroitement couplés avec les fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="b115b-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="b115b-118">Les fournisseurs de magasins étroitement couplés appellent **IMAPISupport:: CompleteMsg** pour indiquer au spouleur MAPI d'postprocess un message.</span><span class="sxs-lookup"><span data-stu-id="b115b-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b115b-119">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="b115b-119">Notes to callers</span></span>

<span data-ttu-id="b115b-120">Appeler **CompleteMsg** uniquement lorsque vous êtes fermement couplé à un fournisseur de transport, vous pouvez gérer tous les destinataires du message, et l'une des conditions suivantes existe:</span><span class="sxs-lookup"><span data-stu-id="b115b-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="b115b-121">Le message a été prétraité.</span><span class="sxs-lookup"><span data-stu-id="b115b-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="b115b-122">Le message nécessite un post-traitement par le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="b115b-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b115b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b115b-123">See also</span></span>



[<span data-ttu-id="b115b-124">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b115b-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

