---
title: Propriété canonique PidTagMessageToMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToMe
api_type:
- HeaderDef
ms.assetid: aeb0fa71-f471-46c5-ad9c-f8afb3fed533
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96a0b010a8ba26a0c1b0cb409f1aaabb308a1c01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356195"
---
# <a name="pidtagmessagetome-canonical-property"></a><span data-ttu-id="86c9c-103">Propriété canonique PidTagMessageToMe</span><span class="sxs-lookup"><span data-stu-id="86c9c-103">PidTagMessageToMe Canonical Property</span></span>

  
  
<span data-ttu-id="86c9c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86c9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86c9c-105">Contient TRUE si cet utilisateur de messagerie est spécifiquement nommé comme destinataire principal (À) de ce message et ne fait pas partie d’une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="86c9c-105">Contains TRUE if this messaging user is specifically named as a primary (To) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86c9c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="86c9c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86c9c-107">PR_MESSAGE_TO_ME</span><span class="sxs-lookup"><span data-stu-id="86c9c-107">PR_MESSAGE_TO_ME</span></span>  <br/> |
|<span data-ttu-id="86c9c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="86c9c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="86c9c-109">0x0057</span><span class="sxs-lookup"><span data-stu-id="86c9c-109">0x0057</span></span>  <br/> |
|<span data-ttu-id="86c9c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="86c9c-110">Data type:</span></span>  <br/> |<span data-ttu-id="86c9c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="86c9c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="86c9c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="86c9c-112">Area:</span></span>  <br/> |<span data-ttu-id="86c9c-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="86c9c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86c9c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="86c9c-114">Remarks</span></span>

<span data-ttu-id="86c9c-115">Cette propriété fournit un moyen pratique de déterminer si le nom d’utilisateur apparaît explicitement dans la liste des destinataires principaux, sans examiner toutes les entrées de la liste.</span><span class="sxs-lookup"><span data-stu-id="86c9c-115">This property provides a convenient way to determine whether the user name appears explicitly in the primary recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="86c9c-116">Cette propriété permet également la gestion automatisée des messages reçus au moment de la réception.</span><span class="sxs-lookup"><span data-stu-id="86c9c-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="86c9c-117">À l’option du fournisseur de transport, cette propriété contient false ou n’est pas incluse si l’utilisateur de messagerie n’est pas répertorié directement dans la table des destinataires.</span><span class="sxs-lookup"><span data-stu-id="86c9c-117">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="86c9c-118">La remise des messages résultant de l’extension de la liste de distribution ou d’une désignation de copie carbone non voyante n’entraîne pas la mise en place de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="86c9c-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="86c9c-119">Le destinataire doit être nommé explicitement.</span><span class="sxs-lookup"><span data-stu-id="86c9c-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="86c9c-120">Les messages non envoyés ne définissent généralement pas **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) ou cette propriété.</span><span class="sxs-lookup"><span data-stu-id="86c9c-120">Unsent messages generally do not set the **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or this property.</span></span> <span data-ttu-id="86c9c-121">S’ils sont présents dans des messages accessibles par l’utilisateur dans des magasins de messages publics, dans des magasins privés d’autres utilisateurs, dans des fichiers sur disque ou incorporés à d’autres messages reçus, ils contiennent généralement les valeurs à laquelle ils ont été fixés la dernière fois qu’un fournisseur de transport a remis le message.</span><span class="sxs-lookup"><span data-stu-id="86c9c-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="86c9c-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="86c9c-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="86c9c-123">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="86c9c-123">Protocol specifications</span></span>

<span data-ttu-id="86c9c-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86c9c-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86c9c-125">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="86c9c-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="86c9c-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86c9c-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86c9c-127">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="86c9c-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="86c9c-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="86c9c-128">Header files</span></span>

<span data-ttu-id="86c9c-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86c9c-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="86c9c-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="86c9c-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="86c9c-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="86c9c-131">Mapitags.h</span></span>
  
> <span data-ttu-id="86c9c-132">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="86c9c-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86c9c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86c9c-133">See also</span></span>



[<span data-ttu-id="86c9c-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="86c9c-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86c9c-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="86c9c-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86c9c-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="86c9c-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86c9c-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="86c9c-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

