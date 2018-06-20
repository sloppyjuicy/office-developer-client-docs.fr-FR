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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bbf09cb841c633b6f13ae12ec20e120ea3fd7ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786368"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="9a428-103">Propriété canonique PidTagOriginCheck</span><span class="sxs-lookup"><span data-stu-id="9a428-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="9a428-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a428-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a428-105">Contient une valeur binaire de vérification qui permet à un destinataire de rapport de remise vérifier l’origine du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="9a428-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a428-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9a428-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9a428-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="9a428-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="9a428-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9a428-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9a428-109">forme0x0027</span><span class="sxs-lookup"><span data-stu-id="9a428-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="9a428-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9a428-110">Data type:</span></span>  <br/> |<span data-ttu-id="9a428-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9a428-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9a428-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="9a428-112">Area:</span></span>  <br/> |<span data-ttu-id="9a428-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="9a428-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a428-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a428-114">Remarks</span></span>

<span data-ttu-id="9a428-115">Cette propriété fournit un moyen d’un fournisseur tiers, comme un message transfert agent d’ou recevoir un rapport de remise d’un utilisateur de messagerie pour vérifier l’origine du message envoyé.</span><span class="sxs-lookup"><span data-stu-id="9a428-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="9a428-116">S’il est présent sur un message reçu, cette propriété doit être copiée sur un rapport de remise généré en réponse au message.</span><span class="sxs-lookup"><span data-stu-id="9a428-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9a428-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9a428-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9a428-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9a428-118">Header files</span></span>

<span data-ttu-id="9a428-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9a428-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9a428-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9a428-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9a428-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9a428-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9a428-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="9a428-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a428-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a428-123">See also</span></span>



[<span data-ttu-id="9a428-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9a428-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9a428-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9a428-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9a428-126">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9a428-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9a428-127">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="9a428-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

