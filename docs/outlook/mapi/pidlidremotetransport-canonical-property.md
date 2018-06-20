---
title: Propriété canonique PidLidRemoteTransport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b0f86b2260299d2d0294598628f2895c50ed9452
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785393"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="30914-103">Propriété canonique PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="30914-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="30914-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30914-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30914-105">Identifie le compte de l’élément d’en-tête est associé, principalement pour implémenter le congé POP sur les fonctionnalités du serveur.</span><span class="sxs-lookup"><span data-stu-id="30914-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30914-106">Propriétés associées</span><span class="sxs-lookup"><span data-stu-id="30914-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="30914-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="30914-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="30914-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="30914-108">Property set:</span></span>  <br/> |<span data-ttu-id="30914-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="30914-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="30914-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="30914-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="30914-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="30914-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="30914-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="30914-112">Data type:</span></span>  <br/> |<span data-ttu-id="30914-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="30914-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="30914-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="30914-114">Area:</span></span>  <br/> |<span data-ttu-id="30914-115">Message à distance</span><span class="sxs-lookup"><span data-stu-id="30914-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30914-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="30914-116">Remarks</span></span>

<span data-ttu-id="30914-117">Cette propriété s’applique uniquement sur les messages qui ont une classe de message IPM. À distance.</span><span class="sxs-lookup"><span data-stu-id="30914-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="30914-118">Microsoft Outlook gère un mappage des différents comptes téléchargez sur une banque donnée dans un message de dossier associé informations (FAI), mais peut également ces informations dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="30914-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="30914-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="30914-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30914-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="30914-120">Protocol specifications</span></span>

<span data-ttu-id="30914-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="30914-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="30914-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="30914-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30914-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="30914-123">Header files</span></span>

<span data-ttu-id="30914-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30914-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="30914-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="30914-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30914-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30914-126">See also</span></span>



[<span data-ttu-id="30914-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="30914-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30914-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="30914-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30914-129">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="30914-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30914-130">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="30914-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

