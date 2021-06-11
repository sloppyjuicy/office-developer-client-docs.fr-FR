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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341110"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="284b3-103">Propriété canonique PidTagRecipientReassignmentProhibited</span><span class="sxs-lookup"><span data-stu-id="284b3-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="284b3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="284b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="284b3-105">Spécifie si l’ajout de destinataires supplémentaires, lors du forwarding du message, est interdit pour le message électronique.</span><span class="sxs-lookup"><span data-stu-id="284b3-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="284b3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="284b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="284b3-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="284b3-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="284b3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="284b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="284b3-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="284b3-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="284b3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="284b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="284b3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="284b3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="284b3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="284b3-112">Area:</span></span>  <br/> |<span data-ttu-id="284b3-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="284b3-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="284b3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="284b3-114">Remarks</span></span>

<span data-ttu-id="284b3-115">Cette propriété est définie en fonction  de la valeur PR_SENSITIVITY[(PidTagSensitivity)](pidtagsensitivity-canonical-property.md)du message électronique.</span><span class="sxs-lookup"><span data-stu-id="284b3-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="284b3-116">Si **PR_SENSITIVITY** est définie sur « 0x00000000 » (normal) ou « 0x00000003 » (confidentiel), cette propriété doit être définie sur « 0x00 » ou ne signifie pas que l’ajout de destinataires supplémentaires ou différents au message électronique est autorisé.</span><span class="sxs-lookup"><span data-stu-id="284b3-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="284b3-117">Si **l’PR_SENSITIVITY** de l’objet de messagerie est définie sur « 0x00000001 » (personnel) ou « 0x00000002 » (privé), cette propriété doit être définie sur « 0x01 » pour empêcher l’ajout de destinataires supplémentaires ou différents de ce message électronique par le biais du forwarding.</span><span class="sxs-lookup"><span data-stu-id="284b3-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="284b3-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="284b3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="284b3-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="284b3-119">Protocol specifications</span></span>

<span data-ttu-id="284b3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="284b3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="284b3-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="284b3-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="284b3-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="284b3-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="284b3-123">Spécifie les propriétés et opérations autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="284b3-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="284b3-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="284b3-124">Header files</span></span>

<span data-ttu-id="284b3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="284b3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="284b3-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="284b3-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="284b3-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="284b3-127">Mapitags.h</span></span>
  
> <span data-ttu-id="284b3-128">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="284b3-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="284b3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="284b3-129">See also</span></span>



[<span data-ttu-id="284b3-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="284b3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="284b3-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="284b3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="284b3-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="284b3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="284b3-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="284b3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

