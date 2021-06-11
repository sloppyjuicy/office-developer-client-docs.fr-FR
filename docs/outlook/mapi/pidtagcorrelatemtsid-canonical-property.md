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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426834"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="aa34a-103">Propriété canonique PidTagCorrelateMtsid</span><span class="sxs-lookup"><span data-stu-id="aa34a-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="aa34a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa34a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa34a-105">Contient l’identificateur du système de transfert de messages (MTS) utilisé dans la corrélation de rapports avec des messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="aa34a-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa34a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="aa34a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aa34a-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="aa34a-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="aa34a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="aa34a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aa34a-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="aa34a-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="aa34a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="aa34a-110">Data type:</span></span>  <br/> |<span data-ttu-id="aa34a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aa34a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="aa34a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="aa34a-112">Area:</span></span>  <br/> |<span data-ttu-id="aa34a-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="aa34a-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa34a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="aa34a-114">Remarks</span></span>

<span data-ttu-id="aa34a-115">Lorsqu’un fournisseur de transport rencontre un message envoyé avec cette propriété définie sur TRUE, il définit cette propriété sur l’identificateur MTS pour ce message.</span><span class="sxs-lookup"><span data-stu-id="aa34a-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="aa34a-116">Après la transmission, cette propriété est stockée avec le message dans le dossier Éléments envoyés du message interpersonnel (IPM).</span><span class="sxs-lookup"><span data-stu-id="aa34a-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="aa34a-117">Les systèmes de messagerie qui supportent la corrélation par l’identificateur MTS, comme X.400, conservent l’identificateur dans l’enveloppe de transport du message d’origine, ainsi que dans tous les rapports générés en réponse à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="aa34a-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="aa34a-118">Lorsqu’un état est remis à partir d’un tel système de messagerie, le fournisseur de transport définit cette propriété sur l’identificateur MTS d’origine à partir de l’enveloppe de transport de l’état.</span><span class="sxs-lookup"><span data-stu-id="aa34a-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="aa34a-119">Cette propriété est ensuite stockée avec l’état.</span><span class="sxs-lookup"><span data-stu-id="aa34a-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="aa34a-120">Une application cliente peut gérer un dossier de résultats de recherche de tous les messages ayant cette propriété.</span><span class="sxs-lookup"><span data-stu-id="aa34a-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="aa34a-121">Lorsqu’un rapport intervient pour un tel message, le client peut appliquer des restrictions au dossier de résultats de recherche, trouver la version d’origine du message et mettre en corrélation les informations du message d’origine avec les nouvelles informations.</span><span class="sxs-lookup"><span data-stu-id="aa34a-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aa34a-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="aa34a-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="aa34a-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="aa34a-123">Header files</span></span>

<span data-ttu-id="aa34a-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa34a-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="aa34a-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="aa34a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="aa34a-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aa34a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="aa34a-127">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="aa34a-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa34a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa34a-128">See also</span></span>



[<span data-ttu-id="aa34a-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="aa34a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aa34a-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="aa34a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aa34a-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="aa34a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aa34a-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="aa34a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

