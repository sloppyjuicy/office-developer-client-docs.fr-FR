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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1980e3bd815b370f125f4449dd7b7f340a7dcb9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786903"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="5f547-103">Propriété canonique PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="5f547-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5f547-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f547-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f547-105">Contient l’identificateur d’entrée du dossier vues définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5f547-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f547-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5f547-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f547-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5f547-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5f547-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5f547-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f547-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="5f547-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="5f547-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5f547-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f547-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5f547-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5f547-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="5f547-112">Area:</span></span>  <br/> |<span data-ttu-id="5f547-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="5f547-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f547-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5f547-114">Remarks</span></span>

<span data-ttu-id="5f547-115">Le dossier d’affichage communs contient un ensemble prédéfini des spécificateurs d’affichage standard, tandis que le dossier d’affichage contient des spécificateurs définis par un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="5f547-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="5f547-116">Ces dossiers, qui ne sont pas visibles dans la hiérarchie de message interpersonnel (IPM), peuvent contenir plusieurs spécificateurs d’affichage, chacune étant stockées sous forme de message.</span><span class="sxs-lookup"><span data-stu-id="5f547-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="5f547-117">La possibilité de l’application cliente à fusionner les deux jeux de spécificateurs et les divulguer les deux.</span><span class="sxs-lookup"><span data-stu-id="5f547-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f547-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5f547-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5f547-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5f547-119">Header files</span></span>

<span data-ttu-id="5f547-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f547-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f547-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5f547-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f547-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5f547-122">Mapitags.h</span></span>
  
> <span data-ttu-id="5f547-123">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="5f547-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f547-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f547-124">See also</span></span>



[<span data-ttu-id="5f547-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5f547-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f547-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5f547-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f547-127">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5f547-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f547-128">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="5f547-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

