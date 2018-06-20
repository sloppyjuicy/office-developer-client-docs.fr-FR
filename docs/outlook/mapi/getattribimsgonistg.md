---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ddb6d692a8e76a9c24affc3af9f612a6f1c0d769
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783401"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="320a7-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="320a7-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="320a7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="320a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="320a7-105">Récupère les attributs de propriétés sur un objet [IMessage](imessageimapiprop.md) fournie par la fonction [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="320a7-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="320a7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="320a7-106">Header file:</span></span>  <br/> |<span data-ttu-id="320a7-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="320a7-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="320a7-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="320a7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="320a7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="320a7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="320a7-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="320a7-110">Called by:</span></span>  <br/> |<span data-ttu-id="320a7-111">Fournisseurs de magasin d’applications clientes et message</span><span class="sxs-lookup"><span data-stu-id="320a7-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="320a7-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="320a7-112">Parameters</span></span>

 <span data-ttu-id="320a7-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="320a7-113">_lpObject_</span></span>
  
> <span data-ttu-id="320a7-114">[in] Pointeur vers un objet **IMessage** obtenu à partir de la fonction [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="320a7-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="320a7-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="320a7-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="320a7-116">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant les propriétés dont les attributs doivent être récupérés.</span><span class="sxs-lookup"><span data-stu-id="320a7-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="320a7-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="320a7-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="320a7-118">[out] Pointeur vers un pointeur vers la structure [SPropAttrArray](spropattrarray.md) retournée qui contient les attributs de la propriété extraite.</span><span class="sxs-lookup"><span data-stu-id="320a7-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="320a7-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="320a7-119">Return value</span></span>

<span data-ttu-id="320a7-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="320a7-120">S_OK</span></span> 
  
> <span data-ttu-id="320a7-121">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="320a7-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="320a7-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="320a7-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="320a7-123">L’appel a réussi, mais une ou plusieurs propriétés ne sont pas accessible et ont été renvoyées avec un type de propriété de PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="320a7-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="320a7-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="320a7-124">Remarks</span></span>

<span data-ttu-id="320a7-125">Attributs de la propriété est accessible uniquement sur propriété objets, autrement dit, l’implémentation de la [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="320a7-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="320a7-126">Pour rendre les propriétés MAPI disponible sur un objet de stockage structuré OLE, [OpenIMsgOnIStg](openimsgonistg.md) génère une [IMessage : IMAPIProp](imessageimapiprop.md) objet en haut de l’objet OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="320a7-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="320a7-127">Les attributs de propriété sur de tels objets peuvent définir ou a été modifiés avec [SetAttribIMsgOnIStg](setattribimsgonistg.md) et récupérés par **GetAttribIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="320a7-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="320a7-128">**GetAttribIMsgOnIStg** et **SetAttribIMsgOnIStg** ne fonctionnent pas sur tous les objets **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="320a7-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="320a7-129">Ils ne sont valides pour **IMessage**- sur - objets **IStorage** renvoyés par **OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="320a7-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="320a7-130">Le nombre et les positions des attributs dans le paramètre _lppPropAttrArray_ correspondent au nombre et les positions des balises de propriété dans le paramètre _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="320a7-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

