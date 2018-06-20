---
title: Propriété canonique PidLidFlagString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 53fe309fb15807ad698fef5a06781e5c3e0bae0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785230"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="f5edb-103">Propriété canonique PidLidFlagString</span><span class="sxs-lookup"><span data-stu-id="f5edb-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="f5edb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5edb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5edb-105">Contient un index qui identifie un ensemble prédéfini de chaînes de texte associé à l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="f5edb-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5edb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f5edb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5edb-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="f5edb-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="f5edb-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="f5edb-108">Property set:</span></span>  <br/> |<span data-ttu-id="f5edb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f5edb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f5edb-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="f5edb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f5edb-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="f5edb-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="f5edb-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f5edb-112">Data type:</span></span>  <br/> |<span data-ttu-id="f5edb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f5edb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f5edb-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="f5edb-114">Area:</span></span>  <br/> |<span data-ttu-id="f5edb-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="f5edb-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5edb-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f5edb-116">Remarks</span></span>

<span data-ttu-id="f5edb-117">Si cette propriété est définie, les clients doivent utiliser la valeur de chaîne correspondant dans les tableaux ci-dessous (par exemple, pour remplacer une chaîne qui est convertie en langue de l’utilisateur actuel) et doivent ignorer la valeur définie dans **dispidFlagRequest** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) et **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f5edb-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="f5edb-118">Les valeurs par défaut suggérés pour l’utilisateur pour les objets contact sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5edb-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="f5edb-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f5edb-119">**Value**</span></span>|<span data-ttu-id="f5edb-120">**Chaîne en anglais**</span><span class="sxs-lookup"><span data-stu-id="f5edb-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5edb-121">0 x 00000000 ou absent</span><span class="sxs-lookup"><span data-stu-id="f5edb-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="f5edb-122">Suivez les instructions relatives à l’affichage de **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="f5edb-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="f5edb-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="f5edb-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="f5edb-124">« Suivi »</span><span class="sxs-lookup"><span data-stu-id="f5edb-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="f5edb-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="f5edb-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="f5edb-126">« Appel »</span><span class="sxs-lookup"><span data-stu-id="f5edb-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="f5edb-127">0 x 00000070</span><span class="sxs-lookup"><span data-stu-id="f5edb-127">0x00000070</span></span>  <br/> |<span data-ttu-id="f5edb-128">« Organiser la réunion »</span><span class="sxs-lookup"><span data-stu-id="f5edb-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="f5edb-129">0 x 00000071</span><span class="sxs-lookup"><span data-stu-id="f5edb-129">0x00000071</span></span>  <br/> |<span data-ttu-id="f5edb-130">« Envoyer un courrier électronique »</span><span class="sxs-lookup"><span data-stu-id="f5edb-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="f5edb-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="f5edb-131">0x00000072</span></span>  <br/> |<span data-ttu-id="f5edb-132">« Envoyer la lettre »</span><span class="sxs-lookup"><span data-stu-id="f5edb-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="f5edb-133">Les valeurs par défaut suggérés pour l’utilisateur pour tous les autres objets de message sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5edb-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="f5edb-134">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f5edb-134">**Value**</span></span>|<span data-ttu-id="f5edb-135">**Chaîne en anglais**</span><span class="sxs-lookup"><span data-stu-id="f5edb-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5edb-136">0 x 00000000 ou absent</span><span class="sxs-lookup"><span data-stu-id="f5edb-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="f5edb-137">Suivez les instructions relatives à l’affichage de **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="f5edb-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="f5edb-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f5edb-138">0x00000001</span></span>  <br/> |<span data-ttu-id="f5edb-139">« Appel »</span><span class="sxs-lookup"><span data-stu-id="f5edb-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="f5edb-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f5edb-140">0x00000002</span></span>  <br/> |<span data-ttu-id="f5edb-141">« Ne pas transférer »</span><span class="sxs-lookup"><span data-stu-id="f5edb-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="f5edb-142">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="f5edb-142">0x00000003</span></span>  <br/> |<span data-ttu-id="f5edb-143">« Suivi »</span><span class="sxs-lookup"><span data-stu-id="f5edb-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="f5edb-144">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="f5edb-144">0x00000004</span></span>  <br/> |<span data-ttu-id="f5edb-145">« Pour votre Information »</span><span class="sxs-lookup"><span data-stu-id="f5edb-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="f5edb-146">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="f5edb-146">0x00000005</span></span>  <br/> |<span data-ttu-id="f5edb-147">« Transférer »</span><span class="sxs-lookup"><span data-stu-id="f5edb-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="f5edb-148">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="f5edb-148">0x00000006</span></span>  <br/> |<span data-ttu-id="f5edb-149">« Aucune réponse nécessaire »</span><span class="sxs-lookup"><span data-stu-id="f5edb-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="f5edb-150">0 x 00000007</span><span class="sxs-lookup"><span data-stu-id="f5edb-150">0x00000007</span></span>  <br/> |<span data-ttu-id="f5edb-151">« Lecture »</span><span class="sxs-lookup"><span data-stu-id="f5edb-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="f5edb-152">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="f5edb-152">0x00000008</span></span>  <br/> |<span data-ttu-id="f5edb-153">« Reply »</span><span class="sxs-lookup"><span data-stu-id="f5edb-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="f5edb-154">0 x 00000009</span><span class="sxs-lookup"><span data-stu-id="f5edb-154">0x00000009</span></span>  <br/> |<span data-ttu-id="f5edb-155">« Répondre à tous »</span><span class="sxs-lookup"><span data-stu-id="f5edb-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="f5edb-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="f5edb-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="f5edb-157">« Révision »</span><span class="sxs-lookup"><span data-stu-id="f5edb-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="f5edb-158">Toutes les chaînes spécifiés ci-dessus peuvent être traduits à la langue de l’utilisateur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f5edb-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f5edb-159">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f5edb-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5edb-160">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f5edb-160">Protocol specifications</span></span>

<span data-ttu-id="f5edb-161">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5edb-161">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5edb-162">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="f5edb-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5edb-163">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5edb-163">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5edb-164">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="f5edb-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5edb-165">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f5edb-165">Header files</span></span>

<span data-ttu-id="f5edb-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5edb-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5edb-167">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f5edb-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5edb-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5edb-168">See also</span></span>



[<span data-ttu-id="f5edb-169">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f5edb-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5edb-170">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f5edb-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5edb-171">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f5edb-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5edb-172">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="f5edb-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

