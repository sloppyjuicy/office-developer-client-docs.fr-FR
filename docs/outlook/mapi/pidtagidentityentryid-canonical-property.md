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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 099df2211e87e253ab1be520378b3a2b2ca7d4c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423334"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="c228d-103">Propriété canonique PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="c228d-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c228d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c228d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c228d-105">Contient l’identificateur d’entrée pour l’identité d’un fournisseur de services telle que définie dans un système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c228d-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c228d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c228d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c228d-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c228d-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c228d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c228d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c228d-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="c228d-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="c228d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c228d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c228d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c228d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c228d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c228d-112">Area:</span></span>  <br/> |<span data-ttu-id="c228d-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="c228d-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c228d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c228d-114">Remarks</span></span>

<span data-ttu-id="c228d-115">Cette propriété n’apparaît pas en tant que propriété sur un objet, mais uniquement en tant que colonne dans un tableau d’état.</span><span class="sxs-lookup"><span data-stu-id="c228d-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="c228d-116">Elle fait partie de l’identité du fournisseur de services qui expose la ligne de table d’état.</span><span class="sxs-lookup"><span data-stu-id="c228d-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="c228d-117">L’identité du fournisseur fait généralement référence à son compte sur le serveur, mais peut faire référence à n’importe quelle représentation définie par le fournisseur dans le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c228d-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="c228d-118">Cette proprerty est généralement définie sur l’identificateur d’entrée de carnet d’adresses approprié.</span><span class="sxs-lookup"><span data-stu-id="c228d-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="c228d-119">Un fournisseur de services qui fournit l’une des propriétés d’identité doit toutes les fournir.</span><span class="sxs-lookup"><span data-stu-id="c228d-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="c228d-120">Les fournisseurs qui appartiennent au même service de messagerie doivent exposer les mêmes valeurs pour les propriétés d’identité.</span><span class="sxs-lookup"><span data-stu-id="c228d-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c228d-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c228d-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c228d-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c228d-122">Header files</span></span>

<span data-ttu-id="c228d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c228d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c228d-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c228d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c228d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c228d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c228d-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="c228d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c228d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c228d-127">See also</span></span>



[<span data-ttu-id="c228d-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="c228d-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="c228d-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c228d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c228d-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c228d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c228d-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c228d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c228d-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c228d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

