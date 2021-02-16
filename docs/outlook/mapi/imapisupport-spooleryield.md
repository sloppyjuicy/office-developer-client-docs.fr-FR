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
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409908"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="4c29c-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="4c29c-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="4c29c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c29c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c29c-105">Donne le contrôle de l’UC aupooler MAPI afin qu’il puisse effectuer les tâches qu’il considère nécessaires.</span><span class="sxs-lookup"><span data-stu-id="4c29c-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4c29c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c29c-106">Parameters</span></span>

 <span data-ttu-id="4c29c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c29c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4c29c-108">Réservé ; doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4c29c-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c29c-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4c29c-109">Return value</span></span>

<span data-ttu-id="4c29c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c29c-110">S_OK</span></span> 
  
> <span data-ttu-id="4c29c-111">Le fournisseur de transport a réussi à libérer l’UC.</span><span class="sxs-lookup"><span data-stu-id="4c29c-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="4c29c-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="4c29c-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="4c29c-113">Demande au fournisseur de transport d’arrêter la remise du message à tous les destinataires qui ne l’ont pas encore reçu.</span><span class="sxs-lookup"><span data-stu-id="4c29c-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c29c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4c29c-114">Remarks</span></span>

<span data-ttu-id="4c29c-115">La **méthode IMAPISupport::SpoolerYield** est implémentée pour les objets de prise en charge du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="4c29c-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="4c29c-116">Les fournisseurs de transport **appellent SpoolerYield** pour permettre aupooler MAPI d’effectuer tout traitement nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4c29c-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4c29c-117">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="4c29c-117">Notes to callers</span></span>

<span data-ttu-id="4c29c-118">Appelez **SpoolerYield** lorsque vous effectuez des opérations longues qui peuvent être suspendues.</span><span class="sxs-lookup"><span data-stu-id="4c29c-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="4c29c-119">Cela permet aux applications au premier plan de s’exécuter pendant une longue opération, telle que la remise à une liste de destinataires importante sur un réseau occupé.</span><span class="sxs-lookup"><span data-stu-id="4c29c-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="4c29c-120">Si **SpoolerYield** est renvoyé avec MAPI_W_CANCEL_MESSAGE, lepooler MAPI a déterminé que le message ne doit plus être envoyé.</span><span class="sxs-lookup"><span data-stu-id="4c29c-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="4c29c-121">Renvoyez MAPI_E_USER_CANCEL processus d’appel et quittez, si possible.</span><span class="sxs-lookup"><span data-stu-id="4c29c-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="4c29c-122">Pour plus d’informations sur le rendement aupooler MAPI, voir Interaction avec le [spooler MAPI.](interacting-with-the-mapi-spooler.md)</span><span class="sxs-lookup"><span data-stu-id="4c29c-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4c29c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c29c-123">See also</span></span>



[<span data-ttu-id="4c29c-124">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c29c-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

