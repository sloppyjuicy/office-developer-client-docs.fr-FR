---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d90f502e2cd7f97ac273ebecedbd0363097b1d60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584953"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="bc8f7-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="bc8f7-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="bc8f7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc8f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc8f7-105">Donne le contrôle de l’UC pour le spouleur MAPI afin qu’elle puisse exécuter toutes les tâches qu’elle estime nécessaires.</span><span class="sxs-lookup"><span data-stu-id="bc8f7-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bc8f7-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="bc8f7-106">Parameters</span></span>

 <span data-ttu-id="bc8f7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc8f7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bc8f7-108">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="bc8f7-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bc8f7-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="bc8f7-109">Return value</span></span>

<span data-ttu-id="bc8f7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc8f7-110">S_OK</span></span> 
  
> <span data-ttu-id="bc8f7-111">Le fournisseur de transport a été libéré correctement l’UC.</span><span class="sxs-lookup"><span data-stu-id="bc8f7-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="bc8f7-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="bc8f7-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="bc8f7-113">Indique le fournisseur de transport pour arrêter la remise du message aux destinataires qui ne le n'avez pas encore reçu.</span><span class="sxs-lookup"><span data-stu-id="bc8f7-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc8f7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bc8f7-114">Remarks</span></span>

<span data-ttu-id="bc8f7-115">La méthode **IMAPISupport::SpoolerYield** est implémentée pour les objets de prise en charge de fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="bc8f7-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="bc8f7-116">Fournisseurs de transport appellent **SpoolerYield** pour autoriser le spouleur MAPI effectuer un traitement nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bc8f7-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bc8f7-117">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="bc8f7-117">Notes to callers</span></span>

<span data-ttu-id="bc8f7-118">Appelez **SpoolerYield** lorsque vous effectuez les opérations de longue durée peuvent être suspendues.</span><span class="sxs-lookup"><span data-stu-id="bc8f7-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="bc8f7-119">Cela permet aux applications de premier plan à exécuter pendant une longue opération, par exemple remise à une liste de destinataires volumineuse sur un réseau occupé (e).</span><span class="sxs-lookup"><span data-stu-id="bc8f7-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="bc8f7-120">Si **SpoolerYield** renvoie avec MAPI_W_CANCEL_MESSAGE, le spouleur MAPI a déterminé que le message ne doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="bc8f7-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="bc8f7-121">Retourner MAPI_E_USER_CANCEL à vos processus appelant et de sortie, si possible.</span><span class="sxs-lookup"><span data-stu-id="bc8f7-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="bc8f7-122">Pour plus d’informations sur les transmettre au spouleur MAPI, consultez [l’interaction avec le spouleur MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="bc8f7-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bc8f7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc8f7-123">See also</span></span>



[<span data-ttu-id="bc8f7-124">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bc8f7-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

