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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a948c8c25eec9b31735bb34b91e2dec4bca5fcfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583448"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="66795-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="66795-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="66795-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66795-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66795-105">Effectue post-traitement sur un message.</span><span class="sxs-lookup"><span data-stu-id="66795-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="66795-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="66795-106">Parameters</span></span>

 <span data-ttu-id="66795-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="66795-107">_ulFlags_</span></span>
  
> <span data-ttu-id="66795-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="66795-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="66795-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="66795-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="66795-110">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="66795-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="66795-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="66795-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="66795-112">[in] Pointeur vers l’identificateur d’entrée du message à traiter.</span><span class="sxs-lookup"><span data-stu-id="66795-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="66795-113">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="66795-113">Return value</span></span>

<span data-ttu-id="66795-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="66795-114">S_OK</span></span> 
  
> <span data-ttu-id="66795-115">Le post-traitement a réussi.</span><span class="sxs-lookup"><span data-stu-id="66795-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66795-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="66795-116">Remarks</span></span>

<span data-ttu-id="66795-117">La méthode **IMAPISupport::CompleteMsg** est implémentée pour les objets de prise en charge de fournisseur de magasin de message et est appelée uniquement par les fournisseurs de magasins de message sont étroitement liés à des fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="66795-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="66795-118">Fournisseurs de magasins étroitement couplés appellent **IMAPISupport::CompleteMsg** pour demander au spouleur MAPI de post-traitement d’un message.</span><span class="sxs-lookup"><span data-stu-id="66795-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="66795-119">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="66795-119">Notes to callers</span></span>

<span data-ttu-id="66795-120">Appelez **CompleteMsg** uniquement lorsque vous sont étroitement liés à un fournisseur de transport, vous pouvez gérer tous les destinataires du message et une des conditions suivantes existe :</span><span class="sxs-lookup"><span data-stu-id="66795-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="66795-121">Le message a été prétraité.</span><span class="sxs-lookup"><span data-stu-id="66795-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="66795-122">Le message requiert post-traitement par le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="66795-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66795-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66795-123">See also</span></span>



[<span data-ttu-id="66795-124">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66795-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

