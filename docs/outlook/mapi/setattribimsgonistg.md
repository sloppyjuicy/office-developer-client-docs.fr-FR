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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 076fb4946af9a80e53fb8452d720c22b351f5ef6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572521"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="604b8-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="604b8-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="604b8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="604b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="604b8-105">Définit ou modifie les attributs de propriétés sur un objet [IMessage](imessageimapiprop.md) fournie par la fonction [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="604b8-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="604b8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="604b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="604b8-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="604b8-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="604b8-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="604b8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="604b8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="604b8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="604b8-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="604b8-110">Called by:</span></span>  <br/> |<span data-ttu-id="604b8-111">Fournisseurs de magasin d’applications clientes et message</span><span class="sxs-lookup"><span data-stu-id="604b8-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="604b8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="604b8-112">Parameters</span></span>

 <span data-ttu-id="604b8-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="604b8-113">_lpObject_</span></span>
  
> <span data-ttu-id="604b8-114">[in] Pointeur vers l’objet pour la propriété attributs sont définies.</span><span class="sxs-lookup"><span data-stu-id="604b8-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="604b8-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="604b8-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="604b8-116">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) contenant un tableau de balises de propriété indiquant les propriétés pour la propriété attributs sont définies.</span><span class="sxs-lookup"><span data-stu-id="604b8-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="604b8-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="604b8-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="604b8-118">[in] Pointeur vers une structure [SPropAttrArray](spropattrarray.md) répertoriant les attributs de propriété à définir.</span><span class="sxs-lookup"><span data-stu-id="604b8-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="604b8-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="604b8-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="604b8-120">[out] Pointeur vers la structure [SPropProblemArray](spropproblemarray.md) retournée contenant un ensemble de problèmes de propriété.</span><span class="sxs-lookup"><span data-stu-id="604b8-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="604b8-121">Cette structure identifie les problèmes rencontrés si **SetAttribIMsgOnIStg** a été en mesure de définir certaines propriétés, mais pas toutes.</span><span class="sxs-lookup"><span data-stu-id="604b8-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="604b8-122">Si un pointeur null est passé dans le paramètre _lppPropProblems_ , aucun tableau de problème de propriété n’est renvoyé même si certaines propriétés n’ont pas été définies.</span><span class="sxs-lookup"><span data-stu-id="604b8-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="604b8-123">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="604b8-123">Return value</span></span>

<span data-ttu-id="604b8-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="604b8-124">S_OK</span></span> 
  
> <span data-ttu-id="604b8-125">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="604b8-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="604b8-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="604b8-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="604b8-127">L’appel a réussi, mais une ou plusieurs propriétés ne sont pas accessible et ont été renvoyées avec un type de propriété de PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="604b8-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="604b8-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="604b8-128">Remarks</span></span>

<span data-ttu-id="604b8-129">Attributs de la propriété est accessible uniquement sur propriété objets, autrement dit, l’implémentation de la [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="604b8-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="604b8-130">Pour rendre les propriétés MAPI disponible sur un objet de stockage structuré OLE, [OpenIMsgOnIStg](openimsgonistg.md) génère une [IMessage : IMAPIProp](imessageimapiprop.md) objet en haut de l’objet OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="604b8-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="604b8-131">Les attributs de propriété sur de tels objets peuvent définir ou a été modifiés avec **SetAttribIMsgOnIStg** et récupérés par [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="604b8-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="604b8-132">**Remarque** **GetAttribIMsgOnIStg** et **SetAttribIMsgOnIStg** ne fonctionnent pas sur tous les objets **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="604b8-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="604b8-133">Ils ne sont valides pour **IMessage**- sur - objets **IStorage** renvoyés par **OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="604b8-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="604b8-134">Dans le paramètre _lpPropAttrs_ , le nombre et la position des attributs doivent correspondre le nombre et la position des balises de propriété passées dans le paramètre _lpPropTags_ .</span><span class="sxs-lookup"><span data-stu-id="604b8-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="604b8-135">La fonction **SetAttribIMsgOnIStg** est utilisée pour définir les propriétés de message en lecture seule lorsque le schéma **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="604b8-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="604b8-136">L’exemple de fournisseur de magasin de message utilise à cet effet.</span><span class="sxs-lookup"><span data-stu-id="604b8-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="604b8-137">Pour plus d’informations, voir [les Messages](mapi-messages.md).</span><span class="sxs-lookup"><span data-stu-id="604b8-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

