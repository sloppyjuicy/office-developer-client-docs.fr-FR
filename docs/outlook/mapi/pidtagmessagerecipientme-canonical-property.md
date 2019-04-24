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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325619"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="d6f93-103">Propriété canonique PidTagMessageRecipientMe</span><span class="sxs-lookup"><span data-stu-id="d6f93-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="d6f93-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6f93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6f93-105">Contient la valeur TRUE si cet utilisateur de messagerie est spécifiquement nommé en tant que destinataire principal (to), copie carbone (CC) ou copie carbone invisible (CCI) de ce message et ne fait pas partie d'une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="d6f93-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6f93-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d6f93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6f93-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="d6f93-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="d6f93-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d6f93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6f93-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="d6f93-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="d6f93-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d6f93-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6f93-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d6f93-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d6f93-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d6f93-112">Area:</span></span>  <br/> |<span data-ttu-id="d6f93-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="d6f93-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6f93-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6f93-114">Remarks</span></span>

<span data-ttu-id="d6f93-115">Cette propriété offre un moyen pratique de déterminer si le nom d'utilisateur apparaît explicitement dans la liste des destinataires, sans examiner toutes les entrées de la liste.</span><span class="sxs-lookup"><span data-stu-id="d6f93-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="d6f93-116">La valeur représente l'opération logique **or** des propriétés **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) et **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), et les informations CCI (qui n'apparaissent pas dans une propriété).</span><span class="sxs-lookup"><span data-stu-id="d6f93-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="d6f93-117">Cette propriété facilite le traitement automatisé des messages reçus au moment de l'accusé de réception.</span><span class="sxs-lookup"><span data-stu-id="d6f93-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="d6f93-118">À l'option du fournisseur de transport, cette propriété contient soit la valeur FALSe, soit elle n'est pas incluse si l'utilisateur de messagerie n'est pas répertorié directement dans la table des destinataires.</span><span class="sxs-lookup"><span data-stu-id="d6f93-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="d6f93-119">La remise des messages résultant de l'expansion de la liste de distribution n'entraîne pas la définition de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d6f93-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="d6f93-120">Le destinataire doit être nommé explicitement.</span><span class="sxs-lookup"><span data-stu-id="d6f93-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="d6f93-121">Les messages non envoyés ne définissent généralement pas cette propriété, **PR_MESSAGE_CC_ME**ou **PR_MESSAGE_TO_ME**.</span><span class="sxs-lookup"><span data-stu-id="d6f93-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="d6f93-122">S'ils sont présents dans les messages auxquels l'utilisateur peut accéder dans les banques de messages publics, dans les magasins privés des autres utilisateurs, dans les fichiers sur le disque ou dans d'autres messages reçus, ils contiennent généralement les valeurs auxquelles ils ont été définis lors de la dernière utilisation d'un fournisseur de transport. le message a été remis.</span><span class="sxs-lookup"><span data-stu-id="d6f93-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d6f93-123">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="d6f93-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6f93-124">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="d6f93-124">Protocol specifications</span></span>

<span data-ttu-id="d6f93-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6f93-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6f93-126">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="d6f93-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6f93-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6f93-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6f93-128">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="d6f93-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6f93-129">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="d6f93-129">Header files</span></span>

<span data-ttu-id="d6f93-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d6f93-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6f93-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d6f93-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6f93-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d6f93-132">Mapitags.h</span></span>
  
> <span data-ttu-id="d6f93-133">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="d6f93-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6f93-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6f93-134">See also</span></span>



[<span data-ttu-id="d6f93-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d6f93-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6f93-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d6f93-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6f93-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d6f93-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6f93-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d6f93-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

