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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397365"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="b79fb-103">Propriété canonique PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="b79fb-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="b79fb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b79fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b79fb-105">Représente l’état d’une demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="b79fb-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b79fb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b79fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b79fb-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="b79fb-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="b79fb-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="b79fb-108">Property set:</span></span>  <br/> |<span data-ttu-id="b79fb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b79fb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b79fb-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="b79fb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b79fb-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="b79fb-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="b79fb-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b79fb-112">Data type:</span></span>  <br/> |<span data-ttu-id="b79fb-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b79fb-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b79fb-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b79fb-114">Area:</span></span>  <br/> |<span data-ttu-id="b79fb-115">Marquage</span><span class="sxs-lookup"><span data-stu-id="b79fb-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b79fb-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b79fb-116">Remarks</span></span>

<span data-ttu-id="b79fb-117">Dans Microsoft Office Outlook, une demande de réunion est un élément de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="b79fb-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="b79fb-118">Cette propriété contient du texte pouvant être précisés pour un utilisateur à associer à l’indicateur et doit être définie si l’objet du message est marqué ou terminé, mais ne doit pas exister pour un objet liées à la réunion.</span><span class="sxs-lookup"><span data-stu-id="b79fb-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="b79fb-119">Clients peuvent choisir de ne pas prendre en charge cette propriété et toujours écrire « Suivi » (traduit à la langue de l’utilisateur le cas échéant) comme valeur de la chaîne lors de cette propriété doit être définie.</span><span class="sxs-lookup"><span data-stu-id="b79fb-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="b79fb-120">Cette propriété doit être ignorée de manière conditionnelle basée sur les valeurs des propriétés de **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) et **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b79fb-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b79fb-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b79fb-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b79fb-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b79fb-122">Protocol specifications</span></span>

<span data-ttu-id="b79fb-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b79fb-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b79fb-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="b79fb-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b79fb-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b79fb-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b79fb-126">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="b79fb-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b79fb-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b79fb-127">Header files</span></span>

<span data-ttu-id="b79fb-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b79fb-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b79fb-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b79fb-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b79fb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b79fb-130">See also</span></span>



[<span data-ttu-id="b79fb-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b79fb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b79fb-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b79fb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b79fb-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b79fb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b79fb-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b79fb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

