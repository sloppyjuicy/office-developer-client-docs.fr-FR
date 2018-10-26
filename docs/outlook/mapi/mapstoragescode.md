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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8dbb871a234d94f8bb2e21b15ce5de6f0db0e4ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581831"
---
# <a name="mapstoragescode"></a><span data-ttu-id="7c1d6-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="7c1d6-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="7c1d6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c1d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c1d6-105">Cartes SCODE renvoie la valeur d’un objet de stockage OLE à un type de valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="7c1d6-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c1d6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7c1d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="7c1d6-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="7c1d6-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="7c1d6-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="7c1d6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7c1d6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7c1d6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7c1d6-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="7c1d6-110">Called by:</span></span>  <br/> |<span data-ttu-id="7c1d6-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="7c1d6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="7c1d6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c1d6-112">Parameters</span></span>

 <span data-ttu-id="7c1d6-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="7c1d6-113">_StgSCode_</span></span>
  
> <span data-ttu-id="7c1d6-114">[in] Valeur de retour MAPI SCODE à partir d’un objet de stockage OLE à mapper à une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="7c1d6-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c1d6-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7c1d6-115">Return value</span></span>

<span data-ttu-id="7c1d6-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c1d6-116">S_OK</span></span> 
  
> <span data-ttu-id="7c1d6-117">L’appel a réussi et a renvoyé la valeur attendue.</span><span class="sxs-lookup"><span data-stu-id="7c1d6-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="7c1d6-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="7c1d6-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="7c1d6-119">La fonction ne peut pas trouver une valeur correspondante.</span><span class="sxs-lookup"><span data-stu-id="7c1d6-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c1d6-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="7c1d6-120">Remarks</span></span>

<span data-ttu-id="7c1d6-121">MAPI fournit la fonction **MapStorageSCode** pour l’utilisation interne des composants MAPI que leurs implémentations de message dans la DLL de message de base.</span><span class="sxs-lookup"><span data-stu-id="7c1d6-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="7c1d6-122">Étant donné que ces composants ouvrir le stockage OLE eux-mêmes, ils doivent pouvoir mapper des valeurs d’erreur renvoyés de problèmes avec le stockage OLE à une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="7c1d6-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="7c1d6-123">Pour plus d’informations, voir [Stockage structuré](structured-storage-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="7c1d6-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

