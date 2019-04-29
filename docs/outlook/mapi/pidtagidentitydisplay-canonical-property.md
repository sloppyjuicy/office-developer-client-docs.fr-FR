---
title: Propriété canonique PidTagIdentityDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityDisplay
api_type:
- HeaderDef
ms.assetid: ad9756c1-c1f9-4ab3-a58a-31e574dd9530
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d6e189f78dec2fc92f1804be93e7885b61734b03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431420"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="4e5c1-103">Propriété canonique PidTagIdentityDisplay</span><span class="sxs-lookup"><span data-stu-id="4e5c1-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="4e5c1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e5c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e5c1-105">Contient le nom complet de l'identité d'un fournisseur de services, tel qu'il est défini dans un système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4e5c1-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e5c1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4e5c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e5c1-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="4e5c1-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="4e5c1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4e5c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e5c1-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="4e5c1-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="4e5c1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4e5c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e5c1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4e5c1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4e5c1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4e5c1-112">Area:</span></span>  <br/> |<span data-ttu-id="4e5c1-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="4e5c1-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e5c1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e5c1-114">Remarks</span></span>

<span data-ttu-id="4e5c1-115">Ces propriétés ne s'affichent pas sous forme de propriétés sur un objet, mais uniquement sous forme de colonne dans une table d'État.</span><span class="sxs-lookup"><span data-stu-id="4e5c1-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="4e5c1-116">Il fait partie de l'identité du fournisseur de services exposant la ligne du tableau d'État.</span><span class="sxs-lookup"><span data-stu-id="4e5c1-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="4e5c1-117">L'identité du fournisseur fait généralement référence à son compte sur le serveur, mais peut faire référence à toute représentation définie par le fournisseur dans le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4e5c1-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="4e5c1-118">Un fournisseur de services qui fournit l'une des propriétés d'identité doit en fournir toutes les.</span><span class="sxs-lookup"><span data-stu-id="4e5c1-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="4e5c1-119">Les fournisseurs qui appartiennent au même service de messagerie doivent exposer les mêmes valeurs pour les propriétés d'identité.</span><span class="sxs-lookup"><span data-stu-id="4e5c1-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4e5c1-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4e5c1-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4e5c1-121">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="4e5c1-121">Header files</span></span>

<span data-ttu-id="4e5c1-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4e5c1-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e5c1-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4e5c1-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e5c1-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4e5c1-124">Mapitags.h</span></span>
  
> <span data-ttu-id="4e5c1-125">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="4e5c1-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e5c1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e5c1-126">See also</span></span>



[<span data-ttu-id="4e5c1-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="4e5c1-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="4e5c1-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4e5c1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e5c1-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4e5c1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e5c1-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4e5c1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e5c1-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4e5c1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

