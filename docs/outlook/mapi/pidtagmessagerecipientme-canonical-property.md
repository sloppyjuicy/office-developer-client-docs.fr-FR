---
title: Propriété canonique PidTagMessageRecipientMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325619"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="d2ecb-103">Propriété canonique PidTagMessageRecipientMe</span><span class="sxs-lookup"><span data-stu-id="d2ecb-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="d2ecb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2ecb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2ecb-105">Contient TRUE si cet utilisateur de messagerie est spécifiquement nommé comme destinataire principal (À), Copie carbone (CC) ou Copie carbone non voyante (Cci) de ce message et ne fait pas partie d’une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2ecb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d2ecb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d2ecb-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="d2ecb-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="d2ecb-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d2ecb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d2ecb-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="d2ecb-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="d2ecb-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d2ecb-110">Data type:</span></span>  <br/> |<span data-ttu-id="d2ecb-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d2ecb-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d2ecb-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d2ecb-112">Area:</span></span>  <br/> |<span data-ttu-id="d2ecb-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="d2ecb-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2ecb-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2ecb-114">Remarks</span></span>

<span data-ttu-id="d2ecb-115">Cette propriété fournit un moyen pratique de déterminer si le nom d’utilisateur apparaît explicitement dans la liste des destinataires, sans examiner toutes les entrées de la liste.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="d2ecb-116">La valeur représente l’opération **logique OR** des propriétés **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) et **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), et les informations CCI (qui n’apparaissent pas dans une propriété).</span><span class="sxs-lookup"><span data-stu-id="d2ecb-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="d2ecb-117">Cette propriété permet la gestion automatisée des messages reçus au moment de la réception.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="d2ecb-118">À l’option du fournisseur de transport, cette propriété contient false ou n’est pas incluse si l’utilisateur de messagerie n’est pas répertorié directement dans la table des destinataires.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="d2ecb-119">La remise des messages qui résulte de l’extension de la liste de distribution ne provoque pas la mise en place de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="d2ecb-120">Le destinataire doit être nommé explicitement.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="d2ecb-121">Les messages non envoyés ne définissent généralement pas cette **propriété, PR_MESSAGE_CC_ME** ou **PR_MESSAGE_TO_ME**.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="d2ecb-122">S’ils sont présents dans des messages accessibles par l’utilisateur dans des magasins de messages publics, dans des magasins privés d’autres utilisateurs, dans des fichiers sur disque ou incorporés à d’autres messages reçus, ils contiennent généralement les valeurs à laquelle ils ont été fixés la dernière fois qu’un fournisseur de transport a remis le message.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d2ecb-123">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d2ecb-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d2ecb-124">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="d2ecb-124">Protocol specifications</span></span>

<span data-ttu-id="d2ecb-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2ecb-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2ecb-126">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d2ecb-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2ecb-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2ecb-128">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d2ecb-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d2ecb-129">Header files</span></span>

<span data-ttu-id="d2ecb-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2ecb-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2ecb-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="d2ecb-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d2ecb-132">Mapitags.h</span></span>
  
> <span data-ttu-id="d2ecb-133">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2ecb-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2ecb-134">See also</span></span>



[<span data-ttu-id="d2ecb-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d2ecb-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2ecb-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d2ecb-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2ecb-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d2ecb-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2ecb-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d2ecb-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

