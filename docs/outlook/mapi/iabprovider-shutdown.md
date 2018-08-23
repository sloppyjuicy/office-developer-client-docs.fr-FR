---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0a93dd44960a01996672a55501a7626d0ff56986
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567887"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="39d95-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="39d95-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="39d95-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39d95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39d95-105">Annule une connexion à une session active.</span><span class="sxs-lookup"><span data-stu-id="39d95-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="39d95-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39d95-106">Parameters</span></span>

 <span data-ttu-id="39d95-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="39d95-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="39d95-108">[In] Réservé ; doit être un pointeur vers zéro.</span><span class="sxs-lookup"><span data-stu-id="39d95-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="39d95-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="39d95-109">Return value</span></span>

<span data-ttu-id="39d95-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="39d95-110">S_OK</span></span> 
  
> <span data-ttu-id="39d95-111">La connexion a été annulée.</span><span class="sxs-lookup"><span data-stu-id="39d95-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="39d95-112">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="39d95-112">Notes to implementers</span></span>

<span data-ttu-id="39d95-113">Dans votre implémentation de la méthode **Shutdown** , effectuez toutes les tâches estiment nécessaires.</span><span class="sxs-lookup"><span data-stu-id="39d95-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="39d95-114">MAPI appelle votre méthode **Shutdown** uniquement une fois que vous avez publié tous les objets d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="39d95-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39d95-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39d95-115">See also</span></span>



[<span data-ttu-id="39d95-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="39d95-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

