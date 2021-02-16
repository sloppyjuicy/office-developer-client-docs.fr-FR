---
title: Propri t canonique PidLidRemoteTransport
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439442"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="db97e-103">Propri t canonique PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="db97e-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="db97e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db97e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db97e-105">Identifie le compte à quel compte l’élément d’en-tête est associé, principalement pour implémenter la fonctionnalité POP Leave on Server.</span><span class="sxs-lookup"><span data-stu-id="db97e-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db97e-106">Propriétés associées</span><span class="sxs-lookup"><span data-stu-id="db97e-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="db97e-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="db97e-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="db97e-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="db97e-108">Property set:</span></span>  <br/> |<span data-ttu-id="db97e-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="db97e-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="db97e-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="db97e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="db97e-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="db97e-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="db97e-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="db97e-112">Data type:</span></span>  <br/> |<span data-ttu-id="db97e-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="db97e-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="db97e-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="db97e-114">Area:</span></span>  <br/> |<span data-ttu-id="db97e-115">Message distant</span><span class="sxs-lookup"><span data-stu-id="db97e-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db97e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="db97e-116">Remarks</span></span>

<span data-ttu-id="db97e-117">Cette propriété n’est pertinente que pour les messages qui ont une classe de message IPM. Distant.</span><span class="sxs-lookup"><span data-stu-id="db97e-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="db97e-118">Microsoft Outlook conserve un mappage de différents comptes qui sont téléchargés vers une banque donnée dans un message FAI (Folder Associated Information), mais il peut également conserver ces informations dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="db97e-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="db97e-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="db97e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db97e-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="db97e-120">Protocol specifications</span></span>

<span data-ttu-id="db97e-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="db97e-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="db97e-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="db97e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db97e-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="db97e-123">Header files</span></span>

<span data-ttu-id="db97e-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db97e-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="db97e-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="db97e-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db97e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db97e-126">See also</span></span>



[<span data-ttu-id="db97e-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="db97e-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db97e-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="db97e-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db97e-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="db97e-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db97e-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="db97e-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

