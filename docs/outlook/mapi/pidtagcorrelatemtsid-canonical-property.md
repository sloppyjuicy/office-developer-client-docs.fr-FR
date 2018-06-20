---
title: Propriété canonique PidTagCorrelateMtsid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 57da2d4c78914323b5dafa4f5ba5b7628d0e2f2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785899"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="08505-103">Propriété canonique PidTagCorrelateMtsid</span><span class="sxs-lookup"><span data-stu-id="08505-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="08505-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08505-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08505-105">Contient l’identificateur de système (MTS) de transfert de message utilisé en corrélation des rapports avec les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="08505-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08505-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="08505-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08505-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="08505-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="08505-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="08505-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08505-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="08505-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="08505-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="08505-110">Data type:</span></span>  <br/> |<span data-ttu-id="08505-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="08505-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="08505-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="08505-112">Area:</span></span>  <br/> |<span data-ttu-id="08505-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="08505-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08505-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="08505-114">Remarks</span></span>

<span data-ttu-id="08505-115">Lorsqu’un fournisseur de transport rencontre un message envoyé à cette propriété la valeur True, elle définit cette propriété sur l’identificateur MTS pour ce message.</span><span class="sxs-lookup"><span data-stu-id="08505-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="08505-116">Après transmission, cette propriété est stockée avec le message dans le dossier éléments envoyés de message interpersonnel (IPM).</span><span class="sxs-lookup"><span data-stu-id="08505-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="08505-117">Systèmes de messagerie qui prennent en charge la corrélation par identificateur MTS, tels que X.400, conservent l’identificateur dans le cadre de l’enveloppe de transport du message d’origine et de tous les rapports générés en réponse à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="08505-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="08505-118">Lorsqu’un rapport est remis à partir d’un tel système de messagerie, le fournisseur de transport définit cette propriété sur l’identificateur MTS d’origine à partir de l’enveloppe de transport de l’état.</span><span class="sxs-lookup"><span data-stu-id="08505-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="08505-119">Cette propriété est ensuite stockée avec le rapport.</span><span class="sxs-lookup"><span data-stu-id="08505-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="08505-120">Une application cliente peut maintenir un dossier de résultats de recherche de tous les messages ayant cette propriété.</span><span class="sxs-lookup"><span data-stu-id="08505-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="08505-121">Lorsqu’un rapport entre pour ce type de message, le client peut appliquer des restrictions dans le dossier de résultats de recherche, recherchez la version d’origine du message et corréler les informations du message d’origine avec les nouvelles informations.</span><span class="sxs-lookup"><span data-stu-id="08505-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08505-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="08505-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="08505-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="08505-123">Header files</span></span>

<span data-ttu-id="08505-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08505-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="08505-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="08505-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="08505-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="08505-126">Mapitags.h</span></span>
  
> <span data-ttu-id="08505-127">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="08505-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08505-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08505-128">See also</span></span>



[<span data-ttu-id="08505-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="08505-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08505-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="08505-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08505-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="08505-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08505-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="08505-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

