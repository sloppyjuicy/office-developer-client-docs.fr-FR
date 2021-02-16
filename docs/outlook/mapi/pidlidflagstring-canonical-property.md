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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357784"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="53e69-103">Propriété canonique PidLidFlagString</span><span class="sxs-lookup"><span data-stu-id="53e69-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="53e69-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53e69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53e69-105">Contient un index qui identifie l’un des ensembles de chaînes de texte prédéfinës associées à l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="53e69-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53e69-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="53e69-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53e69-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="53e69-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="53e69-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="53e69-108">Property set:</span></span>  <br/> |<span data-ttu-id="53e69-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="53e69-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="53e69-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="53e69-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="53e69-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="53e69-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="53e69-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="53e69-112">Data type:</span></span>  <br/> |<span data-ttu-id="53e69-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="53e69-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="53e69-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="53e69-114">Area:</span></span>  <br/> |<span data-ttu-id="53e69-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="53e69-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53e69-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="53e69-116">Remarks</span></span>

<span data-ttu-id="53e69-117">Si cette propriété est définie, les clients doivent utiliser la valeur de chaîne correspondante dans les tableaux ci-dessous (par exemple, pour remplacer une chaîne traduite dans la langue de l’utilisateur actuel) et doivent ignorer la valeur définie dans **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) et **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="53e69-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="53e69-118">Les valeurs par défaut suggérées à l’utilisateur pour les objets contact sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="53e69-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="53e69-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="53e69-119">**Value**</span></span>|<span data-ttu-id="53e69-120">**Chaîne anglaise**</span><span class="sxs-lookup"><span data-stu-id="53e69-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53e69-121">0x00000000 ou non présent</span><span class="sxs-lookup"><span data-stu-id="53e69-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="53e69-122">Suivez les instructions relatives à l’affichage **de dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="53e69-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="53e69-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="53e69-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="53e69-124">« Suivi »</span><span class="sxs-lookup"><span data-stu-id="53e69-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="53e69-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="53e69-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="53e69-126">« Appeler »</span><span class="sxs-lookup"><span data-stu-id="53e69-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="53e69-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="53e69-127">0x00000070</span></span>  <br/> |<span data-ttu-id="53e69-128">« Organiser une réunion »</span><span class="sxs-lookup"><span data-stu-id="53e69-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="53e69-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="53e69-129">0x00000071</span></span>  <br/> |<span data-ttu-id="53e69-130">« Envoyer un e-mail »</span><span class="sxs-lookup"><span data-stu-id="53e69-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="53e69-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="53e69-131">0x00000072</span></span>  <br/> |<span data-ttu-id="53e69-132">« Envoyer une lettre »</span><span class="sxs-lookup"><span data-stu-id="53e69-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="53e69-133">Les valeurs par défaut suggérées à l’utilisateur pour tous les autres objets de message sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="53e69-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="53e69-134">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="53e69-134">**Value**</span></span>|<span data-ttu-id="53e69-135">**Chaîne anglaise**</span><span class="sxs-lookup"><span data-stu-id="53e69-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53e69-136">0x00000000 ou non présent</span><span class="sxs-lookup"><span data-stu-id="53e69-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="53e69-137">Suivez les instructions relatives à l’affichage **de dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="53e69-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="53e69-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="53e69-138">0x00000001</span></span>  <br/> |<span data-ttu-id="53e69-139">« Appeler »</span><span class="sxs-lookup"><span data-stu-id="53e69-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="53e69-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="53e69-140">0x00000002</span></span>  <br/> |<span data-ttu-id="53e69-141">« Ne pas avancer »</span><span class="sxs-lookup"><span data-stu-id="53e69-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="53e69-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="53e69-142">0x00000003</span></span>  <br/> |<span data-ttu-id="53e69-143">« Suivi »</span><span class="sxs-lookup"><span data-stu-id="53e69-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="53e69-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="53e69-144">0x00000004</span></span>  <br/> |<span data-ttu-id="53e69-145">« Pour vos informations »</span><span class="sxs-lookup"><span data-stu-id="53e69-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="53e69-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="53e69-146">0x00000005</span></span>  <br/> |<span data-ttu-id="53e69-147">« Transférer »</span><span class="sxs-lookup"><span data-stu-id="53e69-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="53e69-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="53e69-148">0x00000006</span></span>  <br/> |<span data-ttu-id="53e69-149">« Aucune réponse nécessaire »</span><span class="sxs-lookup"><span data-stu-id="53e69-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="53e69-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="53e69-150">0x00000007</span></span>  <br/> |<span data-ttu-id="53e69-151">« Lecture »</span><span class="sxs-lookup"><span data-stu-id="53e69-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="53e69-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="53e69-152">0x00000008</span></span>  <br/> |<span data-ttu-id="53e69-153">« Répondre »</span><span class="sxs-lookup"><span data-stu-id="53e69-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="53e69-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="53e69-154">0x00000009</span></span>  <br/> |<span data-ttu-id="53e69-155">« Répondre à tous »</span><span class="sxs-lookup"><span data-stu-id="53e69-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="53e69-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="53e69-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="53e69-157">« Révision »</span><span class="sxs-lookup"><span data-stu-id="53e69-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="53e69-158">Toutes les chaînes spécifiées ci-dessus peuvent être traduites dans la langue de l’utilisateur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="53e69-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="53e69-159">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="53e69-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53e69-160">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="53e69-160">Protocol specifications</span></span>

<span data-ttu-id="53e69-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53e69-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53e69-162">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="53e69-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53e69-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53e69-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53e69-164">Spécifie les propriétés et les opérations liées au marquage.</span><span class="sxs-lookup"><span data-stu-id="53e69-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53e69-165">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="53e69-165">Header files</span></span>

<span data-ttu-id="53e69-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53e69-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="53e69-167">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="53e69-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53e69-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53e69-168">See also</span></span>



[<span data-ttu-id="53e69-169">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="53e69-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53e69-170">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="53e69-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53e69-171">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="53e69-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53e69-172">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="53e69-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

