---
title: Propriété canonique PidTagRulesTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 945dabec4ee34d38d2474c918e779d894f4a917c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786673"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="25c64-103">Propriété canonique PidTagRulesTable</span><span class="sxs-lookup"><span data-stu-id="25c64-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="25c64-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25c64-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25c64-105">Contient un tableau avec toutes les règles sont appliquées à un dossier.</span><span class="sxs-lookup"><span data-stu-id="25c64-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25c64-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="25c64-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25c64-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="25c64-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="25c64-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="25c64-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25c64-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="25c64-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="25c64-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="25c64-110">Data type:</span></span>  <br/> |<span data-ttu-id="25c64-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="25c64-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="25c64-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="25c64-112">Area:</span></span>  <br/> |<span data-ttu-id="25c64-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="25c64-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25c64-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="25c64-114">Remarks</span></span>

<span data-ttu-id="25c64-115">Cette propriété est présente sur tous les objets de dossier sur un serveur Exchange qui possèdent des règles.</span><span class="sxs-lookup"><span data-stu-id="25c64-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="25c64-116">Valeurs inclus dans cette propriété sont utilisées pour la lecture et de modification des règles.</span><span class="sxs-lookup"><span data-stu-id="25c64-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="25c64-117">Vous pouvez utiliser la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec l’identificateur d’interface **IID_IExchangeModifyTable** pour obtenir un [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface à la table de règles dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="25c64-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="25c64-118">Vous pouvez utiliser cette interface pour lire et modifier les règles.</span><span class="sxs-lookup"><span data-stu-id="25c64-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="25c64-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="25c64-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="25c64-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="25c64-120">Header files</span></span>

<span data-ttu-id="25c64-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25c64-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="25c64-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="25c64-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="25c64-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="25c64-123">Mapitags.h</span></span>
  
> <span data-ttu-id="25c64-124">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="25c64-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="25c64-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25c64-125">See also</span></span>



[<span data-ttu-id="25c64-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="25c64-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="25c64-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="25c64-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="25c64-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="25c64-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25c64-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="25c64-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25c64-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="25c64-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25c64-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="25c64-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

