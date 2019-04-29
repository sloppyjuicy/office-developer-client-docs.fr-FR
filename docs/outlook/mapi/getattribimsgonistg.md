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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439995"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="e8dbc-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="e8dbc-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="e8dbc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8dbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8dbc-105">Récupère les attributs des propriétés sur un objet [IMessage](imessageimapiprop.md) fourni par la fonction [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="e8dbc-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8dbc-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e8dbc-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8dbc-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="e8dbc-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="e8dbc-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e8dbc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e8dbc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e8dbc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e8dbc-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e8dbc-110">Called by:</span></span>  <br/> |<span data-ttu-id="e8dbc-111">Applications clientes et fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="e8dbc-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="e8dbc-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8dbc-112">Parameters</span></span>

 <span data-ttu-id="e8dbc-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="e8dbc-113">_lpObject_</span></span>
  
> <span data-ttu-id="e8dbc-114">dans Pointeur vers un objet **IMessage** obtenu à partir de la fonction [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="e8dbc-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="e8dbc-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="e8dbc-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="e8dbc-116">dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant les propriétés pour lesquelles les attributs doivent être récupérés.</span><span class="sxs-lookup"><span data-stu-id="e8dbc-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="e8dbc-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="e8dbc-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="e8dbc-118">remarquer Pointeur vers un pointeur vers la structure [SPropAttrArray](spropattrarray.md) renvoyée qui contient les attributs de propriété récupérés.</span><span class="sxs-lookup"><span data-stu-id="e8dbc-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e8dbc-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e8dbc-119">Return value</span></span>

<span data-ttu-id="e8dbc-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8dbc-120">S_OK</span></span> 
  
> <span data-ttu-id="e8dbc-121">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e8dbc-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e8dbc-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="e8dbc-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="e8dbc-123">L'appel a réussi globalement, mais une ou plusieurs propriétés n'ont pas été accessibles et ont été renvoyées avec un type de propriété PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="e8dbc-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8dbc-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8dbc-124">Remarks</span></span>

<span data-ttu-id="e8dbc-125">Les attributs de propriété ne sont accessibles que sur les objets Property, c'est-à-dire les objets qui implémentent l'interface [IMAPIProp: IUnknown](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="e8dbc-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="e8dbc-126">Pour que les propriétés MAPI soient disponibles sur un objet de stockage structuré OLE, [OpenIMsgOnIStg](openimsgonistg.md) crée un objet [IMessage: IMAPIProp](imessageimapiprop.md) en haut de l'objet OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="e8dbc-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="e8dbc-127">Les attributs de propriété sur ces objets peuvent être définis ou modifiés avec [SetAttribIMsgOnIStg](setattribimsgonistg.md) et récupérés avec **GetAttribIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="e8dbc-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e8dbc-128">**GetAttribIMsgOnIStg** et **SetAttribIMsgOnIStg** ne fonctionnent pas sur tous les objets **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="e8dbc-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="e8dbc-129">Elles ne sont valides que pour les objets **IMessage**sur le **IStorage** renvoyés par **OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="e8dbc-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="e8dbc-130">Le nombre et les positions des attributs dans le paramètre _lppPropAttrArray_ correspondent au nombre et aux positions des balises de propriété dans le paramètre _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="e8dbc-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

