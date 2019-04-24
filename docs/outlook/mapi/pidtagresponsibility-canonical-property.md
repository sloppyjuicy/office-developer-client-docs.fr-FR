---
title: Propriété canonique PidTagResponsibility
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330120"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="87ef5-103">Propriété canonique PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="87ef5-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="87ef5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87ef5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87ef5-105">Contient la valeur TRUE si un fournisseur de transport a déjà accepté la responsabilité de la remise du message à ce destinataire, et FALSe si le spouleur MAPI considère que ce fournisseur de transport doit accepter la responsabilité.</span><span class="sxs-lookup"><span data-stu-id="87ef5-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87ef5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="87ef5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87ef5-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="87ef5-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="87ef5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="87ef5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87ef5-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="87ef5-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="87ef5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="87ef5-110">Data type:</span></span>  <br/> |<span data-ttu-id="87ef5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="87ef5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="87ef5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="87ef5-112">Area:</span></span>  <br/> |<span data-ttu-id="87ef5-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="87ef5-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87ef5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="87ef5-114">Remarks</span></span>

<span data-ttu-id="87ef5-115">Lorsque le spouleur MAPI présente un message sortant à un fournisseur de transport, via [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md), il définit cette propriété sur false pour tous les destinataires pour lesquels le spouleur MAPI considère que le fournisseur de transport est responsable et true pour tous les autres destinataires.</span><span class="sxs-lookup"><span data-stu-id="87ef5-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="87ef5-116">Le fournisseur de transport doit tenter de gérer tous les destinataires avec **PR_RESPONSIBILITY** défini sur false.</span><span class="sxs-lookup"><span data-stu-id="87ef5-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="87ef5-117">Après l'envoi ou l'échec concluant de l'envoi à un destinataire, le fournisseur de transport doit définir cette propriété sur TRUE dans le message source pour indiquer qu'il a accepté la responsabilité pour ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="87ef5-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="87ef5-118">Si, après avoir examiné un destinataire, un fournisseur de transport décide qu'il ne peut pas ou ne doit pas le gérer, le fournisseur de transport doit laisser **PR_RESPONSIBILITY** défini sur false.</span><span class="sxs-lookup"><span data-stu-id="87ef5-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="87ef5-119">Le spouleur MAPI recherche alors un autre fournisseur de transport pouvant gérer ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="87ef5-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="87ef5-120">Le spouleur MAPI crée finalement un rapport de non-remise pour les destinataires pour lesquels aucun fournisseur de transport n'accepte la responsabilité.</span><span class="sxs-lookup"><span data-stu-id="87ef5-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="87ef5-121">Si le fournisseur de transport tente de remettre le message et ne le remet pas, il doit appeler la méthode [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) pour indiquer à MAPI les raisons de l'échec, afin que MAPI puisse générer un rapport de non-remise.</span><span class="sxs-lookup"><span data-stu-id="87ef5-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="87ef5-122">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="87ef5-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87ef5-123">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="87ef5-123">Protocol specifications</span></span>

<span data-ttu-id="87ef5-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87ef5-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87ef5-125">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="87ef5-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87ef5-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87ef5-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87ef5-127">Gère l'ordre et le flux de transfert de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="87ef5-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87ef5-128">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="87ef5-128">Header files</span></span>

<span data-ttu-id="87ef5-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="87ef5-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="87ef5-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="87ef5-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="87ef5-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="87ef5-131">Mapitags.h</span></span>
  
> <span data-ttu-id="87ef5-132">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="87ef5-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87ef5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87ef5-133">See also</span></span>



[<span data-ttu-id="87ef5-134">Propri�t� canonique PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="87ef5-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="87ef5-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="87ef5-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87ef5-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="87ef5-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87ef5-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="87ef5-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87ef5-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="87ef5-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

