---
title: Propriété canonique PidTagIdentityEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e724cc727292158fab26495e5d627b42dfe00daa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786073"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="9d5ee-103">Propriété canonique PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="9d5ee-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="9d5ee-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d5ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d5ee-105">Contient l’identificateur d’entrée pour l’identité d’un fournisseur de services au sein d’un système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9d5ee-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d5ee-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9d5ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d5ee-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9d5ee-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="9d5ee-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9d5ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d5ee-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="9d5ee-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="9d5ee-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9d5ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d5ee-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d5ee-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9d5ee-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="9d5ee-112">Area:</span></span>  <br/> |<span data-ttu-id="9d5ee-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="9d5ee-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d5ee-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d5ee-114">Remarks</span></span>

<span data-ttu-id="9d5ee-115">Cette propriété n’apparaît pas en tant que propriété sur n’importe quel objet, mais uniquement en tant que colonne dans une table d’état.</span><span class="sxs-lookup"><span data-stu-id="9d5ee-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="9d5ee-116">Il fait partie de l’identité du fournisseur de services exposition de la ligne de table d’état.</span><span class="sxs-lookup"><span data-stu-id="9d5ee-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="9d5ee-117">Identité du fournisseur est généralement fait référence à son compte sur le serveur, mais peut faire référence à une représentation que le fournisseur définit dans le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9d5ee-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="9d5ee-118">Cette propriété est généralement définie sur l’identificateur d’entrée de livre adresse appropriée.</span><span class="sxs-lookup"><span data-stu-id="9d5ee-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="9d5ee-119">Un fournisseur de services fournissant les propriétés identity doit fournir chacun d'entre eux.</span><span class="sxs-lookup"><span data-stu-id="9d5ee-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="9d5ee-120">Fournisseurs qui appartiennent au même service de message doivent exposer les mêmes valeurs pour les propriétés d’identité.</span><span class="sxs-lookup"><span data-stu-id="9d5ee-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d5ee-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9d5ee-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9d5ee-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9d5ee-122">Header files</span></span>

<span data-ttu-id="9d5ee-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d5ee-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d5ee-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9d5ee-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d5ee-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9d5ee-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9d5ee-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="9d5ee-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d5ee-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d5ee-127">See also</span></span>



[<span data-ttu-id="9d5ee-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="9d5ee-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="9d5ee-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9d5ee-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d5ee-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9d5ee-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d5ee-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9d5ee-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d5ee-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="9d5ee-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

