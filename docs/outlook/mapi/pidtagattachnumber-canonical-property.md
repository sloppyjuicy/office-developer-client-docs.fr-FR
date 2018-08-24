---
title: Propriété canonique PidTagAttachNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f6de157864bff5be41b6e030d555be7b60dcda5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594753"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="bb77c-103">Propriété canonique PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="bb77c-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="bb77c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb77c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb77c-105">Contient un numéro qui identifie de manière unique la pièce jointe dans un message de son parent.</span><span class="sxs-lookup"><span data-stu-id="bb77c-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb77c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bb77c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb77c-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="bb77c-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="bb77c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bb77c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb77c-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="bb77c-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="bb77c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bb77c-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb77c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bb77c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bb77c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="bb77c-112">Area:</span></span>  <br/> |<span data-ttu-id="bb77c-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="bb77c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb77c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb77c-114">Remarks</span></span>

<span data-ttu-id="bb77c-115">Banques de messages génèrent et mettre à jour de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="bb77c-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="bb77c-116">Le nombre de pièces jointes est la clé de tri secondaire, après la position de rendu dans le tableau des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="bb77c-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="bb77c-117">**PR_ATTACH_NUM** est utilisée pour ouvrir la pièce jointe avec la méthode [IMessage::OpenAttach](imessage-openattach.md) .</span><span class="sxs-lookup"><span data-stu-id="bb77c-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="bb77c-118">Dans la session d’une application client, la propriété **PR_ATTACH_NUM** d’une pièce jointe du message reste constante dans la mesure où la table de la pièce jointe est ouverte.</span><span class="sxs-lookup"><span data-stu-id="bb77c-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="bb77c-119">La banque de messages propage les modifications à la table à l’aide des méthodes **IMessage::CreateAttach** et **IMessage::DeleteAttach** .</span><span class="sxs-lookup"><span data-stu-id="bb77c-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="bb77c-120">À son la banque de messages peut générer des notifications de table sur les tables d’ouvrir une pièce jointe afin que les clients peuvent resynchroniser à ces modifications.</span><span class="sxs-lookup"><span data-stu-id="bb77c-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bb77c-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="bb77c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb77c-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="bb77c-122">Protocol specifications</span></span>

<span data-ttu-id="bb77c-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb77c-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb77c-124">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="bb77c-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb77c-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="bb77c-125">Header files</span></span>

<span data-ttu-id="bb77c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb77c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb77c-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bb77c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb77c-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="bb77c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="bb77c-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="bb77c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb77c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb77c-130">See also</span></span>



[<span data-ttu-id="bb77c-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bb77c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb77c-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bb77c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb77c-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bb77c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb77c-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="bb77c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

