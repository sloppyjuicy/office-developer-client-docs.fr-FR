---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428829"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="ce3c1-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="ce3c1-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="ce3c1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce3c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce3c1-105">Définit ou modifie les attributs des propriétés sur un objet [IMessage](imessageimapiprop.md) fourni par la fonction [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="ce3c1-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce3c1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ce3c1-106">Header file:</span></span>  <br/> |<span data-ttu-id="ce3c1-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="ce3c1-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="ce3c1-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="ce3c1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ce3c1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ce3c1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ce3c1-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="ce3c1-110">Called by:</span></span>  <br/> |<span data-ttu-id="ce3c1-111">Applications clientes et fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="ce3c1-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="ce3c1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce3c1-112">Parameters</span></span>

 <span data-ttu-id="ce3c1-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="ce3c1-113">_lpObject_</span></span>
  
> <span data-ttu-id="ce3c1-114">dans Pointeur vers l'objet pour lequel les attributs de propriété sont définis.</span><span class="sxs-lookup"><span data-stu-id="ce3c1-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="ce3c1-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="ce3c1-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="ce3c1-116">dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) contenant un tableau de balises de propriété indiquant les propriétés pour lesquelles les attributs de propriété sont définis.</span><span class="sxs-lookup"><span data-stu-id="ce3c1-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="ce3c1-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="ce3c1-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="ce3c1-118">dans Pointeur vers une structure [SPropAttrArray](spropattrarray.md) répertoriant les attributs de propriété à définir.</span><span class="sxs-lookup"><span data-stu-id="ce3c1-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="ce3c1-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="ce3c1-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="ce3c1-120">remarquer Pointeur vers la structure [SPropProblemArray](spropproblemarray.md) renvoyée contenant un ensemble de problèmes de propriété.</span><span class="sxs-lookup"><span data-stu-id="ce3c1-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="ce3c1-121">Cette structure identifie les problèmes rencontrés si **SetAttribIMsgOnIStg** a pu définir certaines propriétés, mais pas toutes.</span><span class="sxs-lookup"><span data-stu-id="ce3c1-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="ce3c1-122">Si un pointeur vers NULL est transmis dans le paramètre _lppPropProblems_ , aucun tableau de problèmes de propriété n'est renvoyé, même si certaines propriétés n'ont pas été définies.</span><span class="sxs-lookup"><span data-stu-id="ce3c1-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ce3c1-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ce3c1-123">Return value</span></span>

<span data-ttu-id="ce3c1-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce3c1-124">S_OK</span></span> 
  
> <span data-ttu-id="ce3c1-125">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="ce3c1-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ce3c1-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="ce3c1-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="ce3c1-127">L'appel a réussi globalement, mais une ou plusieurs propriétés n'ont pas été accessibles et ont été renvoyées avec un type de propriété PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="ce3c1-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce3c1-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="ce3c1-128">Remarks</span></span>

<span data-ttu-id="ce3c1-129">Les attributs de propriété ne sont accessibles que sur les objets Property, c'est-à-dire les objets qui implémentent l'interface [IMAPIProp: IUnknown](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ce3c1-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="ce3c1-130">Pour que les propriétés MAPI soient disponibles sur un objet de stockage structuré OLE, [OpenIMsgOnIStg](openimsgonistg.md) crée un objet [IMessage: IMAPIProp](imessageimapiprop.md) en haut de l'objet OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="ce3c1-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="ce3c1-131">Les attributs de propriété sur ces objets peuvent être définis ou modifiés avec **SetAttribIMsgOnIStg** et récupérés avec [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="ce3c1-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="ce3c1-132">**Note** **GetAttribIMsgOnIStg** et **SetAttribIMsgOnIStg** ne fonctionnent pas sur tous les objets **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="ce3c1-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="ce3c1-133">Elles ne sont valides que pour les objets **IMessage**sur le **IStorage** renvoyés par **OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="ce3c1-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="ce3c1-134">Dans le paramètre _lpPropAttrs_ , le nombre et la position des attributs doivent correspondre au nombre et à la position des balises de propriété transmises dans le paramètre _lpPropTags_ .</span><span class="sxs-lookup"><span data-stu-id="ce3c1-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="ce3c1-135">La fonction **SetAttribIMsgOnIStg** permet de définir des propriétés de message en lecture seule lorsque cela est requis par le schéma **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="ce3c1-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="ce3c1-136">L'exemple de fournisseur de banque d'messages l'utilise à cette fin.</span><span class="sxs-lookup"><span data-stu-id="ce3c1-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="ce3c1-137">Pour plus d'informations, consultez la rubrique [messages](mapi-messages.md).</span><span class="sxs-lookup"><span data-stu-id="ce3c1-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

