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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393807"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="1cc0c-103">Propriété canonique PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="1cc0c-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="1cc0c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cc0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cc0c-105">Contient la valeur TRUE si un fournisseur de transport a déjà accepté responsable de la remise du message à ce destinataire et FALSE si le spouleur MAPI estime que ce fournisseur de transport doit accepter la responsabilité.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cc0c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1cc0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cc0c-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="1cc0c-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="1cc0c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1cc0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1cc0c-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="1cc0c-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="1cc0c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1cc0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="1cc0c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1cc0c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1cc0c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1cc0c-112">Area:</span></span>  <br/> |<span data-ttu-id="1cc0c-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="1cc0c-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cc0c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1cc0c-114">Remarks</span></span>

<span data-ttu-id="1cc0c-115">Lorsque le spouleur MAPI présente un message sortant à un fournisseur de transport, par le biais [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), elle définit cette propriété sur FALSE pour tous les destinataires pour lesquels le spouleur MAPI considère ce fournisseur de transport chargé et la valeur TRUE pour tous les autres destinataires.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="1cc0c-116">Le fournisseur de transport doit essayer de gérer tous les destinataires avec **PR_RESPONSIBILITY** définie sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="1cc0c-117">Après avoir correctement l’envoi ou ait cessé d’envoyer, à un destinataire, le fournisseur de transport doit définir cette propriété sur TRUE dans le message source pour indiquer qu’il a accepté la responsabilité du destinataire.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="1cc0c-118">Si, après avoir examiné un destinataire, un fournisseur de transport décide qu’il ne peut pas ou qu’il ne doit pas gérer, le fournisseur de transport doit conserver la valeur **PR_RESPONSIBILITY** sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="1cc0c-119">Le spouleur MAPI recherchera ensuite un autre fournisseur de transport qui peut gérer ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="1cc0c-120">Finalement, le spouleur MAPI crée un rapport de non-remise pour tous les destinataires pour lesquels aucun fournisseur de transport n’accepte la responsabilité.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="1cc0c-121">Si le fournisseur de transport tente et ne parvient pas à remettre le message, il doit appeler la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour indiquer à MAPI les raisons de l’échec, afin que MAPI peut générer un rapport de non-remise.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1cc0c-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1cc0c-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1cc0c-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1cc0c-123">Protocol specifications</span></span>

<span data-ttu-id="1cc0c-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cc0c-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cc0c-125">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1cc0c-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cc0c-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cc0c-127">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1cc0c-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1cc0c-128">Header files</span></span>

<span data-ttu-id="1cc0c-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cc0c-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cc0c-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="1cc0c-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1cc0c-131">Mapitags.h</span></span>
  
> <span data-ttu-id="1cc0c-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1cc0c-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1cc0c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cc0c-133">See also</span></span>



[<span data-ttu-id="1cc0c-134">Propri�t� canonique PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="1cc0c-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="1cc0c-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1cc0c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cc0c-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1cc0c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cc0c-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1cc0c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cc0c-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1cc0c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

