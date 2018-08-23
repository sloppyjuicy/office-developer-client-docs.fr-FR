---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: baf45fa33ca085f51a6f9c20f72ec1fd1545ad79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592371"
---
# <a name="uladdref"></a><span data-ttu-id="3afff-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="3afff-103">UlAddRef</span></span>

  
  
<span data-ttu-id="3afff-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3afff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3afff-105">Permet également d’appeler la méthode OLE **IUnknown::AddRef**.</span><span class="sxs-lookup"><span data-stu-id="3afff-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3afff-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3afff-106">Header file:</span></span>  <br/> |<span data-ttu-id="3afff-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3afff-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3afff-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="3afff-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3afff-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3afff-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3afff-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="3afff-110">Called by:</span></span>  <br/> |<span data-ttu-id="3afff-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="3afff-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="3afff-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3afff-112">Parameters</span></span>

 <span data-ttu-id="3afff-113">_pUnk_</span><span class="sxs-lookup"><span data-stu-id="3afff-113">_punk_</span></span>
  
> <span data-ttu-id="3afff-114">[in] Pointeur vers une interface dérivé de l’interface **IUnknown** , en d’autres termes n’importe quelle interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="3afff-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3afff-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3afff-115">Return value</span></span>

<span data-ttu-id="3afff-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3afff-116">S_OK</span></span> 
  
> <span data-ttu-id="3afff-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="3afff-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="3afff-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="3afff-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="3afff-119">Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer.</span><span class="sxs-lookup"><span data-stu-id="3afff-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3afff-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="3afff-120">Remarks</span></span>

 <span data-ttu-id="3afff-121">**UlAddRef** renvoie la valeur renvoyée par la méthode **IUnknown::AddRef** , qui est la nouvelle valeur du décompte de références pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="3afff-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="3afff-122">La valeur est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3afff-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="3afff-123">Pour plus d’informations sur **IUnknown::AddRef**, voir [implémentation de l’IUnknown Interface](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3afff-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

