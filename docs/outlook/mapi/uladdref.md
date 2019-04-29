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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432834"
---
# <a name="uladdref"></a><span data-ttu-id="0c23b-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="0c23b-103">UlAddRef</span></span>

  
  
<span data-ttu-id="0c23b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c23b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c23b-105">Offre un autre moyen d'appeler la méthode OLE **IUnknown:: AddRef**.</span><span class="sxs-lookup"><span data-stu-id="0c23b-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c23b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0c23b-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c23b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0c23b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0c23b-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="0c23b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0c23b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0c23b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0c23b-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="0c23b-110">Called by:</span></span>  <br/> |<span data-ttu-id="0c23b-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="0c23b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="0c23b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c23b-112">Parameters</span></span>

 <span data-ttu-id="0c23b-113">_Punk_</span><span class="sxs-lookup"><span data-stu-id="0c23b-113">_punk_</span></span>
  
> <span data-ttu-id="0c23b-114">dans Pointeur vers une interface dérivée de l'interface **IUnknown** , en d'autres termes, toute interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="0c23b-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0c23b-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0c23b-115">Return value</span></span>

<span data-ttu-id="0c23b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c23b-116">S_OK</span></span> 
  
> <span data-ttu-id="0c23b-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="0c23b-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="0c23b-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="0c23b-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="0c23b-119">Une erreur d'origine inattendue ou inconnue a empêché l'opération de s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="0c23b-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c23b-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c23b-120">Remarks</span></span>

 <span data-ttu-id="0c23b-121">**UlAddRef** renvoie la valeur retournée par la méthode **IUnknown:: AddRef** , qui est la nouvelle valeur du décompte de références pour l'interface.</span><span class="sxs-lookup"><span data-stu-id="0c23b-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="0c23b-122">La valeur est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="0c23b-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="0c23b-123">Pour plus d'informations sur **IUnknown:: AddRef**, consultez [la rubrique Implementing the IUnknown interface](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="0c23b-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

