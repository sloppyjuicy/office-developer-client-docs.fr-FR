---
title: Propriété canonique PidLidFlagRequest
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: df2e474206559dadf250bdf9a078c69da61187c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785220"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="487bc-103">Propriété canonique PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="487bc-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="487bc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="487bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="487bc-105">Représente l’état d’une demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="487bc-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="487bc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="487bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="487bc-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="487bc-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="487bc-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="487bc-108">Property set:</span></span>  <br/> |<span data-ttu-id="487bc-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="487bc-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="487bc-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="487bc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="487bc-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="487bc-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="487bc-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="487bc-112">Data type:</span></span>  <br/> |<span data-ttu-id="487bc-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="487bc-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="487bc-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="487bc-114">Area:</span></span>  <br/> |<span data-ttu-id="487bc-115">Marquage</span><span class="sxs-lookup"><span data-stu-id="487bc-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="487bc-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="487bc-116">Remarks</span></span>

<span data-ttu-id="487bc-117">Dans Microsoft Office Outlook, une demande de réunion est un élément de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="487bc-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="487bc-118">Cette propriété contient du texte pouvant être précisés pour un utilisateur à associer à l’indicateur et doit être définie si l’objet du message est marqué ou terminé, mais ne doit pas exister pour un objet liées à la réunion.</span><span class="sxs-lookup"><span data-stu-id="487bc-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="487bc-119">Clients peuvent choisir de ne pas prendre en charge cette propriété et toujours écrire « Suivi » (traduit à la langue de l’utilisateur le cas échéant) comme valeur de la chaîne lors de cette propriété doit être définie.</span><span class="sxs-lookup"><span data-stu-id="487bc-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="487bc-120">Cette propriété doit être ignorée de manière conditionnelle basée sur les valeurs des propriétés de **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) et **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="487bc-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="487bc-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="487bc-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="487bc-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="487bc-122">Protocol specifications</span></span>

<span data-ttu-id="487bc-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="487bc-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="487bc-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="487bc-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="487bc-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="487bc-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="487bc-126">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="487bc-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="487bc-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="487bc-127">Header files</span></span>

<span data-ttu-id="487bc-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="487bc-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="487bc-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="487bc-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="487bc-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="487bc-130">See also</span></span>



[<span data-ttu-id="487bc-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="487bc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="487bc-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="487bc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="487bc-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="487bc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="487bc-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="487bc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

