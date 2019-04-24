---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357630"
---
# <a name="mapstoragescode"></a><span data-ttu-id="42155-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="42155-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="42155-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42155-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42155-105">Mappe une valeur de retour SCODE à partir d'un objet de stockage OLE vers un type HRESULT.</span><span class="sxs-lookup"><span data-stu-id="42155-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42155-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="42155-106">Header file:</span></span>  <br/> |<span data-ttu-id="42155-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="42155-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="42155-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="42155-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="42155-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="42155-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="42155-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="42155-110">Called by:</span></span>  <br/> |<span data-ttu-id="42155-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="42155-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="42155-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42155-112">Parameters</span></span>

 <span data-ttu-id="42155-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="42155-113">_StgSCode_</span></span>
  
> <span data-ttu-id="42155-114">dans Valeur de retour de la propriété SCODE MAPI d'un objet de stockage OLE à mapper à une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="42155-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="42155-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="42155-115">Return value</span></span>

<span data-ttu-id="42155-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="42155-116">S_OK</span></span> 
  
> <span data-ttu-id="42155-117">L'appel a réussi et a renvoyé la valeur attendue.</span><span class="sxs-lookup"><span data-stu-id="42155-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="42155-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="42155-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="42155-119">La fonction ne parvient pas à trouver une valeur correspondante.</span><span class="sxs-lookup"><span data-stu-id="42155-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42155-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="42155-120">Remarks</span></span>

<span data-ttu-id="42155-121">MAPI fournit la fonction **MapStorageSCode** pour l'utilisation interne des composants MAPI qui basent les implémentations de leurs messages sur la dll du message.</span><span class="sxs-lookup"><span data-stu-id="42155-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="42155-122">Étant donné que ces composants ouvrent le stockage OLE eux-mêmes, ils doivent être en mesure de mapper les valeurs d'erreur renvoyées pour les problèmes liés au stockage OLE vers une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="42155-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="42155-123">Pour plus d'informations, consultez la rubrique [stockage structuré](structured-storage-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="42155-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

