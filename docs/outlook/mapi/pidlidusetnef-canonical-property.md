---
title: Propriété canonique PidLidUseTnef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315420"
---
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="824b9-103">Propriété canonique PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="824b9-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="824b9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="824b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="824b9-105">Indique si le format TNEF (Transport Neutral Encapsulation Format) doit être inclus dans un message lors de la conversion de MAPI en format MIME (Multipurpose Internet Mail Extensions) ou SMTP (Simple Mail Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="824b9-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="824b9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="824b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="824b9-107">dispidUseTNEF</span><span class="sxs-lookup"><span data-stu-id="824b9-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="824b9-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="824b9-108">Property set:</span></span>  <br/> |<span data-ttu-id="824b9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="824b9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="824b9-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="824b9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="824b9-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="824b9-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="824b9-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="824b9-112">Data type:</span></span>  <br/> |<span data-ttu-id="824b9-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="824b9-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="824b9-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="824b9-114">Area:</span></span>  <br/> |<span data-ttu-id="824b9-115">Configuration de l'exécution</span><span class="sxs-lookup"><span data-stu-id="824b9-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="824b9-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="824b9-116">Remarks</span></span>

<span data-ttu-id="824b9-117">Cette propriété spécifie si TNEF doit être inclus dans un message lors de la conversion du format TNEF au format MIME ou SMTP.</span><span class="sxs-lookup"><span data-stu-id="824b9-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="824b9-118">Cette propriété peut être absente et, si tel est le cas, TNEF ne doit pas être inclus dans le message.</span><span class="sxs-lookup"><span data-stu-id="824b9-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="824b9-119">Cette propriété s'applique uniquement lorsque le message est envoyé à partir d'un compte de messagerie POP3/SMTP et ne s'applique pas lorsque le message est envoyé par d'autres fournisseurs, tels que Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="824b9-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="824b9-120">Dans certaines circonstances, par exemple lorsque les boutons de vote sont activés ou qu'un objet incorporé OLE est attaché à un message, Outlook peut définir cette propriété afin de forcer l'utilisation de TNEF.</span><span class="sxs-lookup"><span data-stu-id="824b9-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="824b9-121">La propriété **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) peut être utilisée pour appliquer uniquement du texte brut, et non au format TNEF, lors de l'envoi d'un message.</span><span class="sxs-lookup"><span data-stu-id="824b9-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="824b9-122">Étant donné que **PidLidUseTNEF** remplace le paramètre dans **PR_MSG_EDITOR_FORMAT**, une application qui souhaite forcer le texte brut sur un message sortant doit également rechercher **PIDLIDUSETNEF** et la réinitialiser sur false.</span><span class="sxs-lookup"><span data-stu-id="824b9-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="824b9-123">En outre, le complément doit supprimer les fonctionnalités de message qui nécessitaient le format TNEF pour éviter que les pièces jointes inutilisables du message soient finalement envoyées.</span><span class="sxs-lookup"><span data-stu-id="824b9-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="824b9-124">Utilisez l'indicateur **CCSF_USE_TNEF** lors de l'appel de [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md) pour convertir un message MAPI sortant en flux MIME peut également appliquer le format TNEF.</span><span class="sxs-lookup"><span data-stu-id="824b9-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="824b9-125">Cela s'applique même si **PidLidUseTNEF** n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="824b9-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="824b9-126">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="824b9-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="824b9-127">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="824b9-127">Protocol specifications</span></span>

<span data-ttu-id="824b9-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="824b9-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="824b9-129">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="824b9-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="824b9-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="824b9-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="824b9-131">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="824b9-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="824b9-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="824b9-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="824b9-133">Encode et décode les objets message et Attachment en une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="824b9-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="824b9-134">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="824b9-134">Header files</span></span>

<span data-ttu-id="824b9-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="824b9-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="824b9-136">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="824b9-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="824b9-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="824b9-137">See also</span></span>



[<span data-ttu-id="824b9-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="824b9-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="824b9-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="824b9-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="824b9-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="824b9-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="824b9-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="824b9-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

