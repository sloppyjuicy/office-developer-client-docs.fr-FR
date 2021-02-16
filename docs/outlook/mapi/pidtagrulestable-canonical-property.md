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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428500"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="a3c48-103">Propriété canonique PidTagRulesTable</span><span class="sxs-lookup"><span data-stu-id="a3c48-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="a3c48-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3c48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3c48-105">Contient une table avec toutes les règles appliquées à un dossier.</span><span class="sxs-lookup"><span data-stu-id="a3c48-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a3c48-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a3c48-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3c48-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="a3c48-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="a3c48-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a3c48-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a3c48-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="a3c48-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="a3c48-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a3c48-110">Data type:</span></span>  <br/> |<span data-ttu-id="a3c48-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="a3c48-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="a3c48-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a3c48-112">Area:</span></span>  <br/> |<span data-ttu-id="a3c48-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="a3c48-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3c48-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3c48-114">Remarks</span></span>

<span data-ttu-id="a3c48-115">Cette propriété est présente sur tous les objets de dossier sur une Exchange Server qui ont des règles.</span><span class="sxs-lookup"><span data-stu-id="a3c48-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="a3c48-116">Les valeurs incluses dans cette propriété sont utilisées pour lire et modifier des règles.</span><span class="sxs-lookup"><span data-stu-id="a3c48-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="a3c48-117">Vous pouvez utiliser la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec l’identificateur d’interface **IID_IExchangeModifyTable** pour obtenir une interface [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) dans la table de règles d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="a3c48-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="a3c48-118">Vous pouvez utiliser cette interface pour lire et modifier ces règles.</span><span class="sxs-lookup"><span data-stu-id="a3c48-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a3c48-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a3c48-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a3c48-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a3c48-120">Header files</span></span>

<span data-ttu-id="a3c48-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3c48-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3c48-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a3c48-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a3c48-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a3c48-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a3c48-124">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="a3c48-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a3c48-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3c48-125">See also</span></span>



[<span data-ttu-id="a3c48-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3c48-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="a3c48-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="a3c48-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="a3c48-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a3c48-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3c48-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a3c48-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3c48-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a3c48-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3c48-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a3c48-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

