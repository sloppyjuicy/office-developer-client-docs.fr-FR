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
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327250"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="82476-103">Propriété canonique PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="82476-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="82476-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82476-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82476-105">Contient un nombre qui identifie de manière unique la pièce jointe dans son message parent.</span><span class="sxs-lookup"><span data-stu-id="82476-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82476-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="82476-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82476-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="82476-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="82476-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="82476-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82476-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="82476-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="82476-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="82476-110">Data type:</span></span>  <br/> |<span data-ttu-id="82476-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="82476-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="82476-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="82476-112">Area:</span></span>  <br/> |<span data-ttu-id="82476-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="82476-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82476-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="82476-114">Remarks</span></span>

<span data-ttu-id="82476-115">Les magasins de messages génèrent et conservent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="82476-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="82476-116">Le numéro de pièce jointe est la clé de tri secondaire, après la position de rendu, dans le tableau des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="82476-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="82476-117">**PR_ATTACH_NUM** permet d’ouvrir la pièce jointe avec la méthode [IMessage::OpenAttach.](imessage-openattach.md)</span><span class="sxs-lookup"><span data-stu-id="82476-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="82476-118">Dans la session d’une application cliente, la propriété **PR_ATTACH_NUM** d’une pièce jointe de message reste constante tant que la table de pièces jointes est ouverte.</span><span class="sxs-lookup"><span data-stu-id="82476-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="82476-119">La magasin de messages propage les modifications apportées à la table à l’aide des méthodes **IMessage::CreateAttach** et **IMessage::D eleteAttach.**</span><span class="sxs-lookup"><span data-stu-id="82476-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="82476-120">À son option, la boutique de messages peut générer des notifications de tableau sur les tables de pièces jointes ouvertes afin que les clients peuvent resynchroniser ces modifications.</span><span class="sxs-lookup"><span data-stu-id="82476-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="82476-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="82476-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="82476-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="82476-122">Protocol specifications</span></span>

<span data-ttu-id="82476-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82476-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82476-124">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="82476-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82476-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="82476-125">Header files</span></span>

<span data-ttu-id="82476-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82476-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="82476-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="82476-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="82476-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="82476-128">Mapitags.h</span></span>
  
> <span data-ttu-id="82476-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="82476-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82476-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82476-130">See also</span></span>



[<span data-ttu-id="82476-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="82476-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82476-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="82476-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82476-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="82476-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82476-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="82476-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

