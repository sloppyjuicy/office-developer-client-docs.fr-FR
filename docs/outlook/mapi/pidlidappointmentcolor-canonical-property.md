---
title: Propriété canonique PidLidAppointmentColor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 251377a7b9118437aff3fbb6b2b9376cbf70375c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784963"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="05e64-103">Propriété canonique PidLidAppointmentColor</span><span class="sxs-lookup"><span data-stu-id="05e64-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="05e64-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05e64-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05e64-105">Spécifie la couleur à utiliser lors de l’affichage Calendrier.</span><span class="sxs-lookup"><span data-stu-id="05e64-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05e64-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="05e64-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05e64-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="05e64-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="05e64-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="05e64-108">Property set:</span></span>  <br/> |<span data-ttu-id="05e64-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="05e64-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="05e64-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="05e64-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="05e64-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="05e64-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="05e64-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="05e64-112">Data type:</span></span>  <br/> |<span data-ttu-id="05e64-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="05e64-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="05e64-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="05e64-114">Area:</span></span>  <br/> |<span data-ttu-id="05e64-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="05e64-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05e64-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="05e64-116">Remarks</span></span>

<span data-ttu-id="05e64-117">Cette propriété spécifie la couleur à utiliser lors de l’affichage Calendrier.</span><span class="sxs-lookup"><span data-stu-id="05e64-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="05e64-118">Un client ou serveur doit définir cette valeur pour la compatibilité descendante avec les anciens clients.</span><span class="sxs-lookup"><span data-stu-id="05e64-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="05e64-119">Il peut afficher à la place du calendrier en fonction de la valeur de la propriété **mots clés** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) comme spécifié dans [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="05e64-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="05e64-120">Lorsque la valeur, la valeur doit être une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="05e64-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="05e64-121">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="05e64-121">**Value**</span></span>|<span data-ttu-id="05e64-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="05e64-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05e64-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05e64-123">0x00000000</span></span>  <br/> |<span data-ttu-id="05e64-124">Aucun</span><span class="sxs-lookup"><span data-stu-id="05e64-124">None</span></span>  <br/> |
|<span data-ttu-id="05e64-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="05e64-125">0x00000001</span></span>  <br/> |<span data-ttu-id="05e64-126">Rouge</span><span class="sxs-lookup"><span data-stu-id="05e64-126">Red</span></span>  <br/> |
|<span data-ttu-id="05e64-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="05e64-127">0x00000002</span></span>  <br/> |<span data-ttu-id="05e64-128">Bleu</span><span class="sxs-lookup"><span data-stu-id="05e64-128">Blue</span></span>  <br/> |
|<span data-ttu-id="05e64-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="05e64-129">0x00000003</span></span>  <br/> |<span data-ttu-id="05e64-130">Vert</span><span class="sxs-lookup"><span data-stu-id="05e64-130">Green</span></span>  <br/> |
|<span data-ttu-id="05e64-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="05e64-131">0x00000004</span></span>  <br/> |<span data-ttu-id="05e64-132">Gris</span><span class="sxs-lookup"><span data-stu-id="05e64-132">Grey</span></span>  <br/> |
|<span data-ttu-id="05e64-133">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="05e64-133">0x00000005</span></span>  <br/> |<span data-ttu-id="05e64-134">Orange</span><span class="sxs-lookup"><span data-stu-id="05e64-134">Orange</span></span>  <br/> |
|<span data-ttu-id="05e64-135">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="05e64-135">0x00000006</span></span>  <br/> |<span data-ttu-id="05e64-136">Cyan</span><span class="sxs-lookup"><span data-stu-id="05e64-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="05e64-137">0 x 00000007</span><span class="sxs-lookup"><span data-stu-id="05e64-137">0x00000007</span></span>  <br/> |<span data-ttu-id="05e64-138">Olive</span><span class="sxs-lookup"><span data-stu-id="05e64-138">Olive</span></span>  <br/> |
|<span data-ttu-id="05e64-139">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="05e64-139">0x00000008</span></span>  <br/> |<span data-ttu-id="05e64-140">Violet</span><span class="sxs-lookup"><span data-stu-id="05e64-140">Purple</span></span>  <br/> |
|<span data-ttu-id="05e64-141">0 x 00000009</span><span class="sxs-lookup"><span data-stu-id="05e64-141">0x00000009</span></span>  <br/> |<span data-ttu-id="05e64-142">Bleu-vert</span><span class="sxs-lookup"><span data-stu-id="05e64-142">Teal</span></span>  <br/> |
|<span data-ttu-id="05e64-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="05e64-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="05e64-144">Jaune</span><span class="sxs-lookup"><span data-stu-id="05e64-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="05e64-145">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="05e64-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05e64-146">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="05e64-146">Protocol specifications</span></span>

<span data-ttu-id="05e64-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05e64-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05e64-148">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="05e64-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05e64-149">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05e64-149">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05e64-150">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="05e64-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05e64-151">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="05e64-151">Header files</span></span>

<span data-ttu-id="05e64-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05e64-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="05e64-153">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="05e64-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05e64-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05e64-154">See also</span></span>



[<span data-ttu-id="05e64-155">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="05e64-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05e64-156">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="05e64-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05e64-157">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="05e64-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05e64-158">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="05e64-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

