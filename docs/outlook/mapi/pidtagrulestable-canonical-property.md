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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4b4b60084b8cb53a0a245b502b8fe70241fb4eb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591687"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="13dc7-103">Propriété canonique PidTagRulesTable</span><span class="sxs-lookup"><span data-stu-id="13dc7-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="13dc7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13dc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13dc7-105">Contient un tableau avec toutes les règles sont appliquées à un dossier.</span><span class="sxs-lookup"><span data-stu-id="13dc7-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13dc7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="13dc7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13dc7-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="13dc7-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="13dc7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="13dc7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13dc7-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="13dc7-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="13dc7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="13dc7-110">Data type:</span></span>  <br/> |<span data-ttu-id="13dc7-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="13dc7-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="13dc7-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="13dc7-112">Area:</span></span>  <br/> |<span data-ttu-id="13dc7-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="13dc7-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13dc7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="13dc7-114">Remarks</span></span>

<span data-ttu-id="13dc7-115">Cette propriété est présente sur tous les objets de dossier sur un serveur Exchange qui possèdent des règles.</span><span class="sxs-lookup"><span data-stu-id="13dc7-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="13dc7-116">Valeurs inclus dans cette propriété sont utilisées pour la lecture et de modification des règles.</span><span class="sxs-lookup"><span data-stu-id="13dc7-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="13dc7-117">Vous pouvez utiliser la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec l’identificateur d’interface **IID_IExchangeModifyTable** pour obtenir un [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface à la table de règles dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="13dc7-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="13dc7-118">Vous pouvez utiliser cette interface pour lire et modifier les règles.</span><span class="sxs-lookup"><span data-stu-id="13dc7-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="13dc7-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="13dc7-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="13dc7-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="13dc7-120">Header files</span></span>

<span data-ttu-id="13dc7-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13dc7-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="13dc7-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="13dc7-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="13dc7-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="13dc7-123">Mapitags.h</span></span>
  
> <span data-ttu-id="13dc7-124">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="13dc7-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="13dc7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13dc7-125">See also</span></span>



[<span data-ttu-id="13dc7-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="13dc7-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="13dc7-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="13dc7-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="13dc7-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="13dc7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13dc7-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="13dc7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13dc7-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="13dc7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13dc7-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="13dc7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

