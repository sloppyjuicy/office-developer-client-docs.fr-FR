---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348621"
---
# <a name="itnefaddprops"></a><span data-ttu-id="b8f0a-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="b8f0a-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="b8f0a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8f0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8f0a-105">Permet au fournisseur de services d'appel ou à la passerelle d'ajouter des propriétés à l'encapsulation d'un message ou d'une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="b8f0a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8f0a-106">Parameters</span></span>

 <span data-ttu-id="b8f0a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b8f0a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b8f0a-108">dans Masque de des indicateurs qui contrôle la manière dont les propriétés sont incluses ou exclues de l'encapsulation.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="b8f0a-109">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="b8f0a-109">The following flags can be set:</span></span>
    
<span data-ttu-id="b8f0a-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="b8f0a-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="b8f0a-111">Code uniquement les propriétés du paramètre _lpPropList_ qui font partie des pièces jointes dans le message.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="b8f0a-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="b8f0a-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="b8f0a-113">Encode uniquement les propriétés de la pièce jointe spécifiée par le paramètre _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="b8f0a-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="b8f0a-114">Si le paramètre _lpvData_ n'est pas null, les données pointées sur sont écrites dans l'encapsulation de la pièce jointe dans le fichier indiqué par la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b8f0a-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="b8f0a-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="b8f0a-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="b8f0a-116">Encode uniquement les propriétés du message ou de la pièce jointe spécifiées par le paramètre _ulElemID_ .</span><span class="sxs-lookup"><span data-stu-id="b8f0a-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="b8f0a-117">Si cet indicateur est défini, la valeur dans _lpvData_ doit être un pointeur [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="b8f0a-117">If this flag is set, the value in  _lpvData_ must be an [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) pointer.</span></span> 
    
<span data-ttu-id="b8f0a-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="b8f0a-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="b8f0a-119">Encode toutes les propriétés non spécifiées dans le paramètre _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="b8f0a-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="b8f0a-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="b8f0a-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="b8f0a-121">Encode toutes les propriétés spécifiées dans _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="b8f0a-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="b8f0a-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="b8f0a-123">Encode uniquement les propriétés spécifiées dans _lpPropList_ qui font partie du message lui-même.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="b8f0a-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="b8f0a-124">_ulElemID_</span></span>
  
> <span data-ttu-id="b8f0a-125">dans Propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d'une pièce jointe, qui contient un numéro qui identifie de manière unique la pièce jointe dans son message parent.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="b8f0a-126">Le paramètre _ulElemID_ est utilisé lorsqu'une gestion spéciale est demandée pour une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="b8f0a-127">Le paramètre _ulElemID_ doit être égal à 0 sauf si l'indicateur TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b8f0a-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b8f0a-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="b8f0a-128">_lpvData_</span></span>
  
> <span data-ttu-id="b8f0a-129">dans Pointeur vers les données de la pièce jointe utilisée pour remplacer les données de la pièce jointe spécifiée dans _ulElemID_.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="b8f0a-130">Le paramètre _lpvData_ doit être null, sauf si TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF est défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="b8f0a-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="b8f0a-131">_lpPropList_</span></span>
  
> <span data-ttu-id="b8f0a-132">dans Pointeur vers la liste des propriétés à inclure dans l'encapsulation ou à exclure de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b8f0a-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b8f0a-133">Return value</span></span>

<span data-ttu-id="b8f0a-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="b8f0a-134">S_OK</span></span> 
  
> <span data-ttu-id="b8f0a-135">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8f0a-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8f0a-136">Remarks</span></span>

<span data-ttu-id="b8f0a-137">Les fournisseurs de transport, les fournisseurs de banques de messages et les passerelles appellent la méthode **ITnef:: AddProps** pour répertorier les propriétés à inclure dans le traitement TNEF (Transport-Neutral Encapsulation Format) d'un message ou une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="b8f0a-138">En utilisant des appels successifs, le fournisseur ou la passerelle peut spécifier une liste de propriétés à ajouter et encoder ou à exclure de l'encodage.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="b8f0a-139">Les fournisseurs et les passerelles peuvent également utiliser **AddProps** pour fournir des informations sur toute manipulation particulière de pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="b8f0a-140">**AddProps** est pris en charge uniquement pour les objets TNEF ouverts avec l'indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="b8f0a-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="b8f0a-141">Notez qu'aucun codage TNEF réel ne se produit pour **AddProps** tant que la méthode [ITnef:: Finish](itnef-finish.md) n'est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="b8f0a-142">Cette fonctionnalité signifie que les pointeurs transmis dans **AddProps** doivent rester valides jusqu'à ce \*\*\*\* que l'appel soit effectué.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="b8f0a-143">À ce stade, tous les objets et toutes les données transmis avec des appels **AddProps** peuvent être libérés ou libérés.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b8f0a-144">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b8f0a-144">MFCMAPI reference</span></span>

<span data-ttu-id="b8f0a-145">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b8f0a-146">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="b8f0a-146">**File**</span></span>|<span data-ttu-id="b8f0a-147">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="b8f0a-147">**Function**</span></span>|<span data-ttu-id="b8f0a-148">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="b8f0a-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8f0a-149">File. cpp</span><span class="sxs-lookup"><span data-stu-id="b8f0a-149">File.cpp</span></span>  <br/> |<span data-ttu-id="b8f0a-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="b8f0a-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="b8f0a-151">MFCMAPI utilise la méthode **ITnef:: AddProps** pour copier les propriétés d'un message vers un flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="b8f0a-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8f0a-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8f0a-152">See also</span></span>



[<span data-ttu-id="b8f0a-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="b8f0a-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="b8f0a-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="b8f0a-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="b8f0a-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="b8f0a-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="b8f0a-156">Propriété canonique PidTagAttachTransportName</span><span class="sxs-lookup"><span data-stu-id="b8f0a-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="b8f0a-157">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8f0a-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="b8f0a-158">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="b8f0a-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

