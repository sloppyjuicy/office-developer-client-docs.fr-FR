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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315042"
---
# <a name="itnefsetprops"></a><span data-ttu-id="9f969-103">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="9f969-103">ITnef::SetProps</span></span>

  
  
<span data-ttu-id="9f969-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f969-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f969-105">Définit la valeur d'une ou plusieurs propriétés pour un message encapsulé ou une pièce jointe sans modifier le message ou la pièce jointe d'origine.</span><span class="sxs-lookup"><span data-stu-id="9f969-105">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span> 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="9f969-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f969-106">Parameters</span></span>

 <span data-ttu-id="9f969-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f969-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9f969-108">dans Masque de des indicateurs qui contrôle la manière dont les valeurs des propriétés sont définies.</span><span class="sxs-lookup"><span data-stu-id="9f969-108">[in] A bitmask of flags that controls how property values are set.</span></span> <span data-ttu-id="9f969-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="9f969-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9f969-110">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="9f969-110">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="9f969-111">Encode uniquement les propriétés du message ou de la pièce jointe spécifiées par le paramètre _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="9f969-111">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> 
    
 <span data-ttu-id="9f969-112">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="9f969-112">_ulElemID_</span></span>
  
> <span data-ttu-id="9f969-113">dans Propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d'une pièce jointe, qui contient un numéro qui identifie de manière unique la pièce jointe dans son message parent.</span><span class="sxs-lookup"><span data-stu-id="9f969-113">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span>
    
 <span data-ttu-id="9f969-114">_cValues_</span><span class="sxs-lookup"><span data-stu-id="9f969-114">_cValues_</span></span>
  
> <span data-ttu-id="9f969-115">dans Nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) vers laquelle pointe le paramètre _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="9f969-115">[in] The number of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="9f969-116">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="9f969-116">_lpProps_</span></span>
  
> <span data-ttu-id="9f969-117">dans Pointeur vers une structure **SPropValue** qui contient les valeurs de propriété des propriétés à définir.</span><span class="sxs-lookup"><span data-stu-id="9f969-117">[in] A pointer to an **SPropValue** structure that contains the property values of the properties to set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9f969-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9f969-118">Return value</span></span>

<span data-ttu-id="9f969-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f969-119">S_OK</span></span> 
  
> <span data-ttu-id="9f969-120">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="9f969-120">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f969-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="9f969-121">Remarks</span></span>

<span data-ttu-id="9f969-122">Les fournisseurs de transport, les fournisseurs de banques de messages et les passerelles appellent la méthode **ITnef:: SetProps** pour définir les propriétés à inclure dans l'encapsulation d'un message ou d'une pièce jointe sans modifier le message ou la pièce jointe d'origine.</span><span class="sxs-lookup"><span data-stu-id="9f969-122">Transport providers, message store providers, and gateways call the **ITnef::SetProps** method to set properties to include in the encapsulation of a message or an attachment without modifying the original message or attachment.</span></span> <span data-ttu-id="9f969-123">Les propriétés définies avec cet appel remplacent les propriétés existantes dans le message encapsulé.</span><span class="sxs-lookup"><span data-stu-id="9f969-123">Any properties set with this call override existing properties in the encapsulated message.</span></span> 
  
 <span data-ttu-id="9f969-124">**SetProps** est pris en charge uniquement pour les objets TNEF ouverts avec l'indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="9f969-124">**SetProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> <span data-ttu-id="9f969-125">Il est possible de définir n'importe quel nombre de propriétés avec cet appel.</span><span class="sxs-lookup"><span data-stu-id="9f969-125">Any number of properties can be set with this call.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9f969-126">Aucun codage TNEF réel n'a lieu pour **SetProps** n'a lieu qu'après l'appel de la méthode [ITnef:: Finish](itnef-finish.md) .</span><span class="sxs-lookup"><span data-stu-id="9f969-126">No actual TNEF encoding for **SetProps** happens until after the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="9f969-127">Cette fonctionnalité signifie que les pointeurs transmis dans **SetProps** doivent rester valides jusqu'à ce \*\*\*\* que l'appel soit effectué.</span><span class="sxs-lookup"><span data-stu-id="9f969-127">This functionality means that pointers passed into **SetProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="9f969-128">À ce stade, tous les objets et données transmis aux appels **SetProps** peuvent être libérés ou libérés.</span><span class="sxs-lookup"><span data-stu-id="9f969-128">At that point, all objects and data passed into **SetProps** calls can be released or freed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f969-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f969-129">See also</span></span>



[<span data-ttu-id="9f969-130">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="9f969-130">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="9f969-131">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="9f969-131">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="9f969-132">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="9f969-132">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="9f969-133">Propriété canonique PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="9f969-133">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="9f969-134">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9f969-134">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="9f969-135">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f969-135">ITnef : IUnknown</span></span>](itnefiunknown.md)

