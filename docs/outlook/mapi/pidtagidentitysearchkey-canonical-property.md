---
title: Propriété canonique PidTagIdentitySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 12226039457782162eb74a19713fa77936332f80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565143"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="070c4-103">Propriété canonique PidTagIdentitySearchKey</span><span class="sxs-lookup"><span data-stu-id="070c4-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="070c4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="070c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="070c4-105">Contient la clé de recherche pour l’identité d’un fournisseur de services au sein d’un système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="070c4-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="070c4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="070c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="070c4-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="070c4-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="070c4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="070c4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="070c4-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="070c4-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="070c4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="070c4-110">Data type:</span></span>  <br/> |<span data-ttu-id="070c4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="070c4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="070c4-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="070c4-112">Area:</span></span>  <br/> |<span data-ttu-id="070c4-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="070c4-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="070c4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="070c4-114">Remarks</span></span>

<span data-ttu-id="070c4-115">Cette propriété n’apparaît pas en tant que propriété sur n’importe quel objet, mais uniquement en tant que colonne dans une table d’état.</span><span class="sxs-lookup"><span data-stu-id="070c4-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="070c4-116">Il fait partie de l’identité du fournisseur de services exposition de la ligne de table d’état.</span><span class="sxs-lookup"><span data-stu-id="070c4-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="070c4-117">Identité du fournisseur est généralement fait référence à son compte sur le serveur, mais peut faire référence à une représentation que le fournisseur définit dans le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="070c4-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="070c4-118">Un fournisseur de services fournissant les propriétés identity doit fournir chacun d'entre eux.</span><span class="sxs-lookup"><span data-stu-id="070c4-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="070c4-119">Fournisseurs qui appartiennent au même service de message doivent exposer les mêmes valeurs pour les propriétés d’identité.</span><span class="sxs-lookup"><span data-stu-id="070c4-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="070c4-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="070c4-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="070c4-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="070c4-121">Header files</span></span>

<span data-ttu-id="070c4-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="070c4-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="070c4-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="070c4-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="070c4-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="070c4-124">Mapitags.h</span></span>
  
> <span data-ttu-id="070c4-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="070c4-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="070c4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="070c4-126">See also</span></span>



[<span data-ttu-id="070c4-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="070c4-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="070c4-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="070c4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="070c4-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="070c4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="070c4-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="070c4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="070c4-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="070c4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

