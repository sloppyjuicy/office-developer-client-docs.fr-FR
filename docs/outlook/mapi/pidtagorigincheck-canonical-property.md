---
title: Propriété canonique PidTagOriginCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435760"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="8a0c2-103">Propriété canonique PidTagOriginCheck</span><span class="sxs-lookup"><span data-stu-id="8a0c2-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="8a0c2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a0c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a0c2-105">Contient une valeur de vérification binaire qui permet à un destinataire de rapport de remise de vérifier l'origine du message d'origine.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a0c2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8a0c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a0c2-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="8a0c2-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="8a0c2-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8a0c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a0c2-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="8a0c2-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="8a0c2-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8a0c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a0c2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8a0c2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8a0c2-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8a0c2-112">Area:</span></span>  <br/> |<span data-ttu-id="8a0c2-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="8a0c2-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a0c2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a0c2-114">Remarks</span></span>

<span data-ttu-id="8a0c2-115">Cette propriété permet à un tiers, tel qu'un agent de transfert des messages (MTA) ou un utilisateur de messagerie qui reçoit un rapport de remise, de vérifier l'origine du message soumis.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="8a0c2-116">S'il est présent sur un message reçu, cette propriété doit être copiée dans n'importe quel rapport de remise généré en réponse au message.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8a0c2-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8a0c2-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8a0c2-118">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="8a0c2-118">Header files</span></span>

<span data-ttu-id="8a0c2-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8a0c2-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a0c2-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a0c2-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8a0c2-121">Mapitags.h</span></span>
  
> <span data-ttu-id="8a0c2-122">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="8a0c2-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a0c2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a0c2-123">See also</span></span>



[<span data-ttu-id="8a0c2-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8a0c2-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a0c2-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8a0c2-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a0c2-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8a0c2-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a0c2-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8a0c2-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

