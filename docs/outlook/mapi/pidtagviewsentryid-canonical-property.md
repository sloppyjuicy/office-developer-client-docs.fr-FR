---
title: Propriété canonique PidTagViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 73ed7213ea2bd5079458ccc237b65590f06e8d53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586262"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="15f91-103">Propriété canonique PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="15f91-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="15f91-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15f91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15f91-105">Contient l’identificateur d’entrée du dossier vues définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="15f91-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15f91-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="15f91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15f91-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="15f91-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="15f91-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="15f91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15f91-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="15f91-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="15f91-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="15f91-110">Data type:</span></span>  <br/> |<span data-ttu-id="15f91-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="15f91-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="15f91-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="15f91-112">Area:</span></span>  <br/> |<span data-ttu-id="15f91-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="15f91-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15f91-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="15f91-114">Remarks</span></span>

<span data-ttu-id="15f91-115">Le dossier d’affichage communs contient un ensemble prédéfini des spécificateurs d’affichage standard, tandis que le dossier d’affichage contient des spécificateurs définis par un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="15f91-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="15f91-116">Ces dossiers, qui ne sont pas visibles dans la hiérarchie de message interpersonnel (IPM), peuvent contenir plusieurs spécificateurs d’affichage, chacune étant stockées sous forme de message.</span><span class="sxs-lookup"><span data-stu-id="15f91-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="15f91-117">La possibilité de l’application cliente à fusionner les deux jeux de spécificateurs et les divulguer les deux.</span><span class="sxs-lookup"><span data-stu-id="15f91-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="15f91-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="15f91-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="15f91-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="15f91-119">Header files</span></span>

<span data-ttu-id="15f91-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15f91-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="15f91-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="15f91-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="15f91-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="15f91-122">Mapitags.h</span></span>
  
> <span data-ttu-id="15f91-123">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="15f91-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15f91-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15f91-124">See also</span></span>



[<span data-ttu-id="15f91-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="15f91-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15f91-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="15f91-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15f91-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="15f91-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15f91-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="15f91-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

