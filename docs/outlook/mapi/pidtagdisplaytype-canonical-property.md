---
title: Propriété canonique PidTagDisplayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360780"
---
# <a name="pidtagdisplaytype-canonical-property"></a><span data-ttu-id="cd263-103">Propriété canonique PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="cd263-103">PidTagDisplayType Canonical Property</span></span>

  
  
<span data-ttu-id="cd263-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd263-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd263-105">Contient une valeur utilisée pour associer une icône à une ligne particulière d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="cd263-105">Contains a value used to associate an icon with a particular row of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd263-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cd263-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd263-107">PR_DISPLAY_TYPE</span><span class="sxs-lookup"><span data-stu-id="cd263-107">PR_DISPLAY_TYPE</span></span>  <br/> |
|<span data-ttu-id="cd263-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="cd263-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd263-109">0x3900</span><span class="sxs-lookup"><span data-stu-id="cd263-109">0x3900</span></span>  <br/> |
|<span data-ttu-id="cd263-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cd263-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd263-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cd263-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cd263-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="cd263-112">Area:</span></span>  <br/> |<span data-ttu-id="cd263-113">Carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="cd263-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd263-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cd263-114">Remarks</span></span>

<span data-ttu-id="cd263-115">Cette propriété contient un nombre long qui facilite un traitement spécial de l’entrée de table en fonction de son type.</span><span class="sxs-lookup"><span data-stu-id="cd263-115">This property contains a long integer that facilitates special treatment of the table entry based on its type.</span></span> <span data-ttu-id="cd263-116">Ce traitement spécial consiste généralement à afficher une icône ou un autre élément d’affichage associé au type d’affichage.</span><span class="sxs-lookup"><span data-stu-id="cd263-116">This special treatment typically consists of displaying an icon, or other display element, associated with the display type.</span></span> 
  
<span data-ttu-id="cd263-117">Cette propriété n’est pas utilisée dans les tables de contenu de dossier.</span><span class="sxs-lookup"><span data-stu-id="cd263-117">This property is not used in folder contents tables.</span></span> <span data-ttu-id="cd263-118">Les applications clientes doivent utiliser la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) d’un message et l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) appropriée pour obtenir les propriétés **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) et **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) pour ce message.</span><span class="sxs-lookup"><span data-stu-id="cd263-118">Client applications should use a message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property and appropriate [IMAPIFormInfo](imapiforminfoimapiprop.md) interface to get the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties for that message.</span></span> 
  
<span data-ttu-id="cd263-119">Cette propriété peut avoir exactement l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cd263-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="cd263-120">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="cd263-120">DT_AGENT</span></span> 
  
> <span data-ttu-id="cd263-121">Un agent automatisé, tel qu’un guillemet du jour ou un affichage de graphique météo.</span><span class="sxs-lookup"><span data-stu-id="cd263-121">An automated agent, such as Quote-Of-The-Day or a weather chart display.</span></span>
    
<span data-ttu-id="cd263-122">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="cd263-122">DT_DISTLIST</span></span> 
  
> <span data-ttu-id="cd263-123">Liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="cd263-123">A distribution list.</span></span>
    
<span data-ttu-id="cd263-124">DT_FOLDER</span><span class="sxs-lookup"><span data-stu-id="cd263-124">DT_FOLDER</span></span> 
  
> <span data-ttu-id="cd263-125">Affiche l’icône de dossier par défaut en adjacent au dossier.</span><span class="sxs-lookup"><span data-stu-id="cd263-125">Display default folder icon adjacent to folder.</span></span>
    
<span data-ttu-id="cd263-126">DT_FOLDER_LINK</span><span class="sxs-lookup"><span data-stu-id="cd263-126">DT_FOLDER_LINK</span></span> 
  
> <span data-ttu-id="cd263-127">Affiche l’icône de lien de dossier par défaut adjacente au dossier plutôt que l’icône de dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd263-127">Display default folder link icon adjacent to folder rather than the default folder icon.</span></span>
    
<span data-ttu-id="cd263-128">DT_FOLDER_SPECIAL</span><span class="sxs-lookup"><span data-stu-id="cd263-128">DT_FOLDER_SPECIAL</span></span> 
  
> <span data-ttu-id="cd263-129">Icône d’affichage d’un dossier avec une distinction spécifique à l’application, telle qu’un type spécial de dossier public.</span><span class="sxs-lookup"><span data-stu-id="cd263-129">Display icon for a folder with an application-specific distinction, such as a special type of public folder.</span></span>
    
<span data-ttu-id="cd263-130">DT_FORUM</span><span class="sxs-lookup"><span data-stu-id="cd263-130">DT_FORUM</span></span> 
  
> <span data-ttu-id="cd263-131">Forum, tel qu’un service de forum ou un dossier public ou partagé.</span><span class="sxs-lookup"><span data-stu-id="cd263-131">A forum, such as a bulletin board service or a public or shared folder.</span></span>
    
<span data-ttu-id="cd263-132">DT_GLOBAL</span><span class="sxs-lookup"><span data-stu-id="cd263-132">DT_GLOBAL</span></span> 
  
> <span data-ttu-id="cd263-133">Un carnet d’adresses global.</span><span class="sxs-lookup"><span data-stu-id="cd263-133">A global address book.</span></span>
    
<span data-ttu-id="cd263-134">DT_LOCAL</span><span class="sxs-lookup"><span data-stu-id="cd263-134">DT_LOCAL</span></span> 
  
> <span data-ttu-id="cd263-135">Carnet d’adresses local que vous partagez avec un petit groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="cd263-135">A local address book that you share with a small workgroup.</span></span>
    
<span data-ttu-id="cd263-136">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="cd263-136">DT_MAILUSER</span></span> 
  
> <span data-ttu-id="cd263-137">Un utilisateur de messagerie classique.</span><span class="sxs-lookup"><span data-stu-id="cd263-137">A typical messaging user.</span></span>
    
<span data-ttu-id="cd263-138">DT_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="cd263-138">DT_MODIFIABLE</span></span> 
  
> <span data-ttu-id="cd263-139">Modifiable ; le conteneur doit être noté comme modifiable dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cd263-139">Modifiable; the container should be denoted as modifiable in the user interface.</span></span>
    
<span data-ttu-id="cd263-140">DT_NOT_SPECIFIC</span><span class="sxs-lookup"><span data-stu-id="cd263-140">DT_NOT_SPECIFIC</span></span> 
  
> <span data-ttu-id="cd263-141">Ne correspond à aucun des autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="cd263-141">Does not match any of the other settings.</span></span>
    
<span data-ttu-id="cd263-142">DT_ORGANIZATION</span><span class="sxs-lookup"><span data-stu-id="cd263-142">DT_ORGANIZATION</span></span> 
  
> <span data-ttu-id="cd263-143">Alias spécial défini pour un grand groupe, tel que le coordinateur de service d’aide, de comptabilité ou de disque dur.</span><span class="sxs-lookup"><span data-stu-id="cd263-143">A special alias defined for a large group, such as helpdesk, accounting, or blood-drive coordinator.</span></span>
    
<span data-ttu-id="cd263-144">DT_PRIVATE_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="cd263-144">DT_PRIVATE_DISTLIST</span></span> 
  
> <span data-ttu-id="cd263-145">Liste de distribution privée, gérée par des personnes.</span><span class="sxs-lookup"><span data-stu-id="cd263-145">A private, personally administered distribution list.</span></span>
    
<span data-ttu-id="cd263-146">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="cd263-146">DT_REMOTE_MAILUSER</span></span> 
  
> <span data-ttu-id="cd263-147">Destinataire connu d’un système de messagerie étranger ou distant.</span><span class="sxs-lookup"><span data-stu-id="cd263-147">A recipient known to be from a foreign or remote messaging system.</span></span>
    
<span data-ttu-id="cd263-148">DT_WAN</span><span class="sxs-lookup"><span data-stu-id="cd263-148">DT_WAN</span></span> 
  
> <span data-ttu-id="cd263-149">Un carnet d’adresses réseau large.</span><span class="sxs-lookup"><span data-stu-id="cd263-149">A wide area network address book.</span></span>
    
<span data-ttu-id="cd263-150">Les tables de contenu de carnet d’adresses utilisent les valeurs DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST et DT_REMOTE_MAILUSER de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="cd263-150">Address book contents tables use the DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST, and DT_REMOTE_MAILUSER values.</span></span> <span data-ttu-id="cd263-151">Les tables de hiérarchie de carnet d’adresses et les tables DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC et DT_WAN de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="cd263-151">Address book hierarchy tables and one-off tables use the DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC, and DT_WAN values.</span></span> <span data-ttu-id="cd263-152">Les tables de hiérarchie de dossiers utilisent DT_FOLDER, DT_FOLDER_LINK et DT_FOLDER_SPECIAL valeurs.</span><span class="sxs-lookup"><span data-stu-id="cd263-152">Folder hierarchy tables use the DT_FOLDER, DT_FOLDER_LINK, and DT_FOLDER_SPECIAL values.</span></span> 
  
<span data-ttu-id="cd263-153">Si cette propriété n’est pas définie, le client doit supposer le type par défaut approprié pour la table, généralement DT_FOLDER, DT_LOCAL ou DT_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="cd263-153">If this property is not set, the client should assume the default type appropriate for the table, typically DT_FOLDER, DT_LOCAL, or DT_MAILUSER.</span></span> 
  
 <span data-ttu-id="cd263-154">**Remarque** Toutes les valeurs non documentées sont réservées à MAPI.</span><span class="sxs-lookup"><span data-stu-id="cd263-154">**Note** All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="cd263-155">Les applications clientes ne doivent pas définir de nouvelles valeurs et doivent être prêtes à traiter une valeur nondocumentée.</span><span class="sxs-lookup"><span data-stu-id="cd263-155">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cd263-156">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cd263-156">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd263-157">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="cd263-157">Protocol specifications</span></span>

<span data-ttu-id="cd263-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd263-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd263-159">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="cd263-159">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cd263-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd263-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd263-161">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="cd263-161">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="cd263-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd263-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd263-163">Spécifie les propriétés et opérations autorisées pour les modèles de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="cd263-163">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="cd263-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd263-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd263-165">Active l’accès à l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="cd263-165">Enables directory access.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd263-166">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cd263-166">Header files</span></span>

<span data-ttu-id="cd263-167">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd263-167">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd263-168">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cd263-168">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd263-169">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cd263-169">Mapitags.h</span></span>
  
> <span data-ttu-id="cd263-170">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="cd263-170">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd263-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd263-171">See also</span></span>



[<span data-ttu-id="cd263-172">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cd263-172">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd263-173">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cd263-173">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd263-174">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cd263-174">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd263-175">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="cd263-175">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

