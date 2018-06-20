---
title: Type complexe RuleSets_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9bd05541-7cd8-321b-8dd6-fa885c269057
ms.openlocfilehash: 795864810c5d79f6328339009ddc84410caa4e62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789574"
---
# <a name="rulesetstype-complextype-visio-xml"></a><span data-ttu-id="83d36-102">Type complexe RuleSets_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="83d36-102">RuleSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="83d36-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="83d36-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83d36-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="83d36-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="83d36-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="83d36-105">**Schema file**</span></span> <br/> |<span data-ttu-id="83d36-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="83d36-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="83d36-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="83d36-107">**Extension base**</span></span> <br/> |<span data-ttu-id="83d36-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="83d36-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="83d36-109">Définition</span><span class="sxs-lookup"><span data-stu-id="83d36-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="83d36-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="83d36-110">Elements and attributes</span></span>

<span data-ttu-id="83d36-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="83d36-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="83d36-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="83d36-112">Child elements</span></span>

|<span data-ttu-id="83d36-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="83d36-113">**Element**</span></span>|<span data-ttu-id="83d36-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="83d36-114">**Type**</span></span>|<span data-ttu-id="83d36-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="83d36-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="83d36-116">Ensemble de règles</span><span class="sxs-lookup"><span data-stu-id="83d36-116">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="83d36-117">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="83d36-117">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="83d36-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="83d36-118">Attributes</span></span>

<span data-ttu-id="83d36-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="83d36-119">None.</span></span>
  

