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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 124a0d8f23fcff9d1bca9d5debe4a9aa6fb6146c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587116"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="dd399-103">Propriété canonique PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="dd399-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="dd399-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd399-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd399-105">Identifie le compte de l’élément d’en-tête est associé, principalement pour implémenter le congé POP sur les fonctionnalités du serveur.</span><span class="sxs-lookup"><span data-stu-id="dd399-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd399-106">Propriétés associées</span><span class="sxs-lookup"><span data-stu-id="dd399-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="dd399-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="dd399-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="dd399-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="dd399-108">Property set:</span></span>  <br/> |<span data-ttu-id="dd399-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="dd399-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="dd399-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="dd399-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dd399-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="dd399-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="dd399-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="dd399-112">Data type:</span></span>  <br/> |<span data-ttu-id="dd399-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="dd399-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="dd399-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="dd399-114">Area:</span></span>  <br/> |<span data-ttu-id="dd399-115">Message à distance</span><span class="sxs-lookup"><span data-stu-id="dd399-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd399-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd399-116">Remarks</span></span>

<span data-ttu-id="dd399-117">Cette propriété s’applique uniquement sur les messages qui ont une classe de message IPM. À distance.</span><span class="sxs-lookup"><span data-stu-id="dd399-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="dd399-118">Microsoft Outlook gère un mappage des différents comptes téléchargez sur une banque donnée dans un message de dossier associé informations (FAI), mais peut également ces informations dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="dd399-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dd399-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="dd399-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dd399-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="dd399-120">Protocol specifications</span></span>

<span data-ttu-id="dd399-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="dd399-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="dd399-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="dd399-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dd399-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="dd399-123">Header files</span></span>

<span data-ttu-id="dd399-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dd399-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd399-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="dd399-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd399-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd399-126">See also</span></span>



[<span data-ttu-id="dd399-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="dd399-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd399-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="dd399-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd399-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="dd399-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd399-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="dd399-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

