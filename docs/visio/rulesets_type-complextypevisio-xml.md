---
title: Type complexe RuleSets_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9bd05541-7cd8-321b-8dd6-fa885c269057
ms.openlocfilehash: 41172a4f15b0d9038fd0ffb0c0a7d8c3d4078798
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385920"
---
# <a name="rulesetstype-complextype-visio-xml"></a><span data-ttu-id="7e211-102">Type complexe RuleSets_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="7e211-102">RuleSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7e211-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7e211-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e211-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="7e211-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7e211-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7e211-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7e211-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7e211-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7e211-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7e211-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7e211-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="7e211-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7e211-109">Définition</span><span class="sxs-lookup"><span data-stu-id="7e211-109">Definition</span></span>

```XML
          <xs:complexType name="RuleSets_Type">
          
          <xs:sequence>
    <xs:element name="RuleSet"  type="RuleSet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7e211-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7e211-110">Elements and attributes</span></span>

<span data-ttu-id="7e211-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="7e211-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7e211-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7e211-112">Child elements</span></span>

|<span data-ttu-id="7e211-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7e211-113">**Element**</span></span>|<span data-ttu-id="7e211-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="7e211-114">**Type**</span></span>|<span data-ttu-id="7e211-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e211-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7e211-116">Ensemble de règles</span><span class="sxs-lookup"><span data-stu-id="7e211-116">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7e211-117">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="7e211-117">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7e211-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="7e211-118">Attributes</span></span>

<span data-ttu-id="7e211-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7e211-119">None.</span></span>
  

