---
title: Propriété canonique PidTagRecipientReassignmentProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0176485ca9b84260176e3be8ec9c8f42cf755cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786537"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="0685e-103">Propriété canonique PidTagRecipientReassignmentProhibited</span><span class="sxs-lookup"><span data-stu-id="0685e-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="0685e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0685e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0685e-105">Spécifie si l’ajout de destinataires supplémentaires, lors de la transmission du message, est interdite pour le message électronique.</span><span class="sxs-lookup"><span data-stu-id="0685e-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0685e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0685e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0685e-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="0685e-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="0685e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0685e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0685e-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="0685e-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="0685e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0685e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0685e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0685e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0685e-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="0685e-112">Area:</span></span>  <br/> |<span data-ttu-id="0685e-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="0685e-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0685e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0685e-114">Remarks</span></span>

<span data-ttu-id="0685e-115">Cette propriété est définie en fonction de valeur de **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) du message électronique.</span><span class="sxs-lookup"><span data-stu-id="0685e-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="0685e-116">Si **PR_SENSITIVITY** est défini sur « 0 x 00000000 » (normal) ou « 0 x 00000003 » (confidentiel), cette propriété doit être définie sur 0 x « 00 » ou absent ce qui signifie que l’ajout des destinataires supplémentaires ou différentes pour le message électronique est autorisé.</span><span class="sxs-lookup"><span data-stu-id="0685e-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="0685e-117">Si le message électronique de l’objet **PR_SENSITIVITY** est défini sur « 0 x 00000001 » (personnelles) ou « 0 x 00000002 » (privé), cette propriété doit être définie à « 0 x 01 » pour empêcher l’ajout de destinataires supplémentaires ou différentes de ce message électronique par le biais de transfert.</span><span class="sxs-lookup"><span data-stu-id="0685e-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0685e-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0685e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0685e-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0685e-119">Protocol specifications</span></span>

<span data-ttu-id="0685e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0685e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0685e-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="0685e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0685e-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0685e-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0685e-123">Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="0685e-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0685e-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0685e-124">Header files</span></span>

<span data-ttu-id="0685e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0685e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0685e-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0685e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0685e-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0685e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0685e-128">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="0685e-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0685e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0685e-129">See also</span></span>



[<span data-ttu-id="0685e-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0685e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0685e-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0685e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0685e-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0685e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0685e-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="0685e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

