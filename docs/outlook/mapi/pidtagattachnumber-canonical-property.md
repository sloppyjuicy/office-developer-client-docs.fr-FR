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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c4a46710311f2c4d26ec3d667c7bf535df69f595
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785734"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="71436-103">Propriété canonique PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="71436-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="71436-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="71436-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="71436-105">Contient un numéro qui identifie de manière unique la pièce jointe dans un message de son parent.</span><span class="sxs-lookup"><span data-stu-id="71436-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71436-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="71436-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71436-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="71436-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="71436-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="71436-108">Identifier:</span></span>  <br/> |<span data-ttu-id="71436-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="71436-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="71436-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="71436-110">Data type:</span></span>  <br/> |<span data-ttu-id="71436-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="71436-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="71436-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="71436-112">Area:</span></span>  <br/> |<span data-ttu-id="71436-113">Pièce jointe du message</span><span class="sxs-lookup"><span data-stu-id="71436-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71436-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="71436-114">Remarks</span></span>

<span data-ttu-id="71436-115">Banques de messages génèrent et mettre à jour de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="71436-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="71436-116">Le nombre de pièces jointes est la clé de tri secondaire, après la position de rendu dans le tableau des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="71436-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="71436-117">**PR_ATTACH_NUM** est utilisée pour ouvrir la pièce jointe avec la méthode [IMessage::OpenAttach](imessage-openattach.md) .</span><span class="sxs-lookup"><span data-stu-id="71436-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="71436-118">Dans la session d’une application client, la propriété **PR_ATTACH_NUM** d’une pièce jointe du message reste constante dans la mesure où la table de la pièce jointe est ouverte.</span><span class="sxs-lookup"><span data-stu-id="71436-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="71436-119">La banque de messages propage les modifications à la table à l’aide des méthodes **IMessage::CreateAttach** et **IMessage::DeleteAttach** .</span><span class="sxs-lookup"><span data-stu-id="71436-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="71436-120">À son la banque de messages peut générer des notifications de table sur les tables d’ouvrir une pièce jointe afin que les clients peuvent resynchroniser à ces modifications.</span><span class="sxs-lookup"><span data-stu-id="71436-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="71436-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="71436-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="71436-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="71436-122">Protocol specifications</span></span>

<span data-ttu-id="71436-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71436-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71436-124">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="71436-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="71436-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="71436-125">Header files</span></span>

<span data-ttu-id="71436-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71436-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="71436-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="71436-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="71436-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="71436-128">Mapitags.h</span></span>
  
> <span data-ttu-id="71436-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="71436-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71436-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71436-130">See also</span></span>



[<span data-ttu-id="71436-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="71436-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71436-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="71436-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71436-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="71436-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71436-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="71436-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

