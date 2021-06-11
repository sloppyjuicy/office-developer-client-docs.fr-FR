---
title: Propriété canonique PidTagMessageEditorFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325633"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a><span data-ttu-id="0905c-103">Propriété canonique PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="0905c-103">PidTagMessageEditorFormat Canonical Property</span></span>

  
  
<span data-ttu-id="0905c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0905c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0905c-105">Spécifie le format d’un éditeur à utiliser pour afficher un message.</span><span class="sxs-lookup"><span data-stu-id="0905c-105">Specifies the format for an editor to use to display a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0905c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0905c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0905c-107">PR_MSG_EDITOR_FORMAT</span><span class="sxs-lookup"><span data-stu-id="0905c-107">PR_MSG_EDITOR_FORMAT</span></span>  <br/> |
|<span data-ttu-id="0905c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0905c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0905c-109">0x5909</span><span class="sxs-lookup"><span data-stu-id="0905c-109">0x5909</span></span>  <br/> |
|<span data-ttu-id="0905c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0905c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0905c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0905c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0905c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0905c-112">Area:</span></span>  <br/> |<span data-ttu-id="0905c-113">Divers</span><span class="sxs-lookup"><span data-stu-id="0905c-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0905c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0905c-114">Remarks</span></span>

<span data-ttu-id="0905c-115">Les valeurs possibles **pour PR_MSG_EDITOR_FORMAT** peuvent être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="0905c-115">The possible values for **PR_MSG_EDITOR_FORMAT** can be one of the following:</span></span> 
  
|<span data-ttu-id="0905c-116">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="0905c-116">**Value**</span></span>|<span data-ttu-id="0905c-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="0905c-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0905c-118">**EDITOR_FORMAT_DONTKNOW**</span><span class="sxs-lookup"><span data-stu-id="0905c-118">**EDITOR_FORMAT_DONTKNOW**</span></span> <br/> |<span data-ttu-id="0905c-119">Le format de l’éditeur à utiliser est inconnu.</span><span class="sxs-lookup"><span data-stu-id="0905c-119">The format for the editor to use is unknown.</span></span>  <br/> |
|<span data-ttu-id="0905c-120">**EDITOR_FORMAT_PLAINTEXT**</span><span class="sxs-lookup"><span data-stu-id="0905c-120">**EDITOR_FORMAT_PLAINTEXT**</span></span> <br/> |<span data-ttu-id="0905c-121">L’éditeur doit afficher le message au format texte simple.</span><span class="sxs-lookup"><span data-stu-id="0905c-121">The editor should display the message in plain text format.</span></span>  <br/> |
|<span data-ttu-id="0905c-122">**EDITOR_FORMAT_HTML**</span><span class="sxs-lookup"><span data-stu-id="0905c-122">**EDITOR_FORMAT_HTML**</span></span> <br/> |<span data-ttu-id="0905c-123">L’éditeur doit afficher le message au format HTML.</span><span class="sxs-lookup"><span data-stu-id="0905c-123">The editor should display the message in HTML format.</span></span>  <br/> |
|<span data-ttu-id="0905c-124">**EDITOR_FORMAT_RTF**</span><span class="sxs-lookup"><span data-stu-id="0905c-124">**EDITOR_FORMAT_RTF**</span></span> <br/> |<span data-ttu-id="0905c-125">L’éditeur doit afficher le message au format Texte enrichi.</span><span class="sxs-lookup"><span data-stu-id="0905c-125">The editor should display the message in Rich Text Format.</span></span>  <br/> |
   
<span data-ttu-id="0905c-126">Par défaut, les messages électroniques (avec la classe de message **IPM. Remarque** ou avec une classe de message personnalisée dérivée **d’IPM. Remarque**) les messages envoyés à partir d’un compte de messagerie POP3/SMTP sont envoyés au format TNEF (Transport Neutral Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="0905c-126">By default, mail messages (with the message class **IPM.Note** or with a custom message class derived from **IPM.Note**) sent from a POP3/SMTP mail account are sent in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="0905c-127">La **PR_MSG_EDITOR_FORMAT** peut être utilisée pour appliquer uniquement le texte simple, et non le TNEF, lors de l’envoi d’un message.</span><span class="sxs-lookup"><span data-stu-id="0905c-127">The **PR_MSG_EDITOR_FORMAT** property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="0905c-128">Si **PR_MSG_EDITOR_FORMAT** est définie sur **EDITOR_FORMAT_PLAINTEXT,** le message est envoyé en texte simple sans TNEF.</span><span class="sxs-lookup"><span data-stu-id="0905c-128">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_PLAINTEXT**, the message is sent as plain text without TNEF.</span></span> <span data-ttu-id="0905c-129">Si **PR_MSG_EDITOR_FORMAT** est définie sur **EDITOR_FORMAT_RTF**, le codage TNEF est implicitement activé et le message est envoyé à l’aide du format Internet par défaut spécifié dans le client Outlook.</span><span class="sxs-lookup"><span data-stu-id="0905c-129">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_RTF**, TNEF encoding is implicitly enabled, and the message is sent by using the default Internet format that is specified in the Outlook client.</span></span>
  
<span data-ttu-id="0905c-130">Il existe deux autres façons d’appliquer l’utilisation du TNEF lors de l’envoi d’un message.</span><span class="sxs-lookup"><span data-stu-id="0905c-130">There are two other ways to enforce the use of TNEF when sending a message.</span></span>
  
- <span data-ttu-id="0905c-131">La définition de la propriété nommée **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) sur True dans un message indique que le TNEF doit être inclus lors de la conversion du message de MAPI en MIME/SMTP.</span><span class="sxs-lookup"><span data-stu-id="0905c-131">Setting the **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) named property to True on a message indicates TNEF should be included when converting the message from MAPI to MIME/SMTP.</span></span> <span data-ttu-id="0905c-132">Notez que **dispidUseTNEF** s’applique uniquement lorsque le message est envoyé à partir d’un compte de messagerie POP3/SMTP et ne s’applique pas lorsque le message est envoyé par d’autres fournisseurs, tels que Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0905c-132">Note that **dispidUseTNEF** only applies when the message is sent from a POP3/SMTP mail account, and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="0905c-133">**dispidUseTNEF** remplace le paramètre dans **PR_MSG_EDITOR_FORMAT**.</span><span class="sxs-lookup"><span data-stu-id="0905c-133">**dispidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**.</span></span>
    
- <span data-ttu-id="0905c-134">L’utilisation de l’indicateur **CCSF_USE_TNEF** lors de l’appel de [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) pour convertir un message MAPI sortant en flux MIME peut également appliquer le TNEF.</span><span class="sxs-lookup"><span data-stu-id="0905c-134">Using the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="0905c-135">Cela s’applique même **si dispidUseTNEF n’est** pas définie.</span><span class="sxs-lookup"><span data-stu-id="0905c-135">This applies even if **dispidUseTNEF** is not set.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="0905c-136">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0905c-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0905c-137">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="0905c-137">Protocol specifications</span></span>

<span data-ttu-id="0905c-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0905c-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0905c-139">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="0905c-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0905c-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0905c-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0905c-141">Définit les structures de données de base utilisées dans les opérations distantes.</span><span class="sxs-lookup"><span data-stu-id="0905c-141">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="0905c-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0905c-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0905c-143">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="0905c-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0905c-144">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0905c-144">Header files</span></span>

<span data-ttu-id="0905c-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0905c-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="0905c-146">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0905c-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="0905c-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0905c-147">Mapitags.h</span></span>
  
> <span data-ttu-id="0905c-148">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="0905c-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0905c-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0905c-149">See also</span></span>



[<span data-ttu-id="0905c-150">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0905c-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0905c-151">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0905c-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0905c-152">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0905c-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0905c-153">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0905c-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

