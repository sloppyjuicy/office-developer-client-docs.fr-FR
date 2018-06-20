---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 480a50bd8c3738ad7d0c178cb4cabfdecd15412e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784484"
---
# <a name="itnefsetprops"></a><span data-ttu-id="93c5c-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="93c5c-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="93c5c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93c5c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93c5c-105">Définit la valeur d’une ou plusieurs propriétés d’un message encapsulé ou d’une pièce jointe sans modifier le message d’origine ou une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="93c5c-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="93c5c-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="93c5c-106">Parameters</span></span>

 <span data-ttu-id="93c5c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="93c5c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="93c5c-108">[in] Masque de bits d’indicateurs qui contrôle la façon dont les valeurs de propriété sont définies.</span><span class="sxs-lookup"><span data-stu-id="93c5c-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="93c5c-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="93c5c-109">The following flag can be set:</span></span>
    
<span data-ttu-id="93c5c-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="93c5c-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="93c5c-111">Code uniquement les propriétés à partir du message ou d’une pièce jointe spécifié par le paramètre _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="93c5c-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="93c5c-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="93c5c-112">_ulElemID_</span></span>
  
> <span data-ttu-id="93c5c-113">[in] Propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d’une pièce jointe qui contient un numéro qui identifie de façon unique identifie la pièce jointe dans un message de son parent.</span><span class="sxs-lookup"><span data-stu-id="93c5c-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="93c5c-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="93c5c-114">_cValues_</span></span>
  
> <span data-ttu-id="93c5c-115">[in] Le nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) indiqué par le paramètre _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="93c5c-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="93c5c-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="93c5c-116">_lpProps_</span></span>
  
> <span data-ttu-id="93c5c-117">[in] Pointeur vers une structure **SPropValue** qui contient des propriétés pour définir les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="93c5c-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="93c5c-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="93c5c-118">Return value</span></span>

<span data-ttu-id="93c5c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="93c5c-119">S_OK</span></span> 
  
> <span data-ttu-id="93c5c-120">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="93c5c-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93c5c-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="93c5c-121">Remarks</span></span>

<span data-ttu-id="93c5c-122">Transport fournisseurs, les fournisseurs de banque de message et passerelles appel la méthode **ITnef::SetProps** pour définir les propriétés à inclure dans l’encapsulation d’un message ou d’une pièce jointe sans modifier le message d’origine ou la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="93c5c-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="93c5c-123">Toutes les propriétés définies avec cet appel substituent les propriétés existantes dans le message encapsulé.</span><span class="sxs-lookup"><span data-stu-id="93c5c-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="93c5c-124">**SetProps** est pris en charge uniquement pour les objets TNEF ouverts avec l’indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="93c5c-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="93c5c-125">Nombre de propriétés peut être défini avec cet appel.</span><span class="sxs-lookup"><span data-stu-id="93c5c-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="93c5c-126">Aucun réel le codage TNEF pour **SetProps** passe-t-il jusqu'à ce que la méthode [ITnef::Finish](itnef-finish.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="93c5c-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="93c5c-127">Cette fonctionnalité signifie que des pointeurs passées dans **SetProps** reste valables jusqu'à après l’appel à la **fin** .</span><span class="sxs-lookup"><span data-stu-id="93c5c-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="93c5c-128">À ce stade, tous les objets et les données passées dans **SetProps** appels peuvent être publiées ou libérées.</span><span class="sxs-lookup"><span data-stu-id="93c5c-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93c5c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93c5c-129">See also</span></span>



[<span data-ttu-id="93c5c-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="93c5c-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="93c5c-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="93c5c-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="93c5c-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="93c5c-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="93c5c-133">Propriété canonique PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="93c5c-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="93c5c-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="93c5c-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="93c5c-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="93c5c-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

