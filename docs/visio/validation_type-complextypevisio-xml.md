---
title: Type complexe Validation_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bc106ec-879a-0a4b-8c04-a5734eb0097a
ms.openlocfilehash: 6f751db1566e39d919fd0a456d3aab72559ceeba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385591"
---
# <a name="validationtype-complextype-visio-xml"></a><span data-ttu-id="3458b-102">Type complexe Validation_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="3458b-102">Validation_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3458b-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="3458b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3458b-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="3458b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3458b-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="3458b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3458b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3458b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3458b-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="3458b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3458b-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="3458b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3458b-109">Définition</span><span class="sxs-lookup"><span data-stu-id="3458b-109">Definition</span></span>

```XML
          <xs:complexType name="Validation_Type">
          
          <xs:sequence>
    <xs:element name="ValidationProperties"  type="ValidationProperties_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleSets"  type="RuleSets_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Issues"  type="Issues_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3458b-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="3458b-110">Elements and attributes</span></span>

<span data-ttu-id="3458b-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="3458b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3458b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3458b-112">Child elements</span></span>

|<span data-ttu-id="3458b-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3458b-113">**Element**</span></span>|<span data-ttu-id="3458b-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="3458b-114">**Type**</span></span>|<span data-ttu-id="3458b-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="3458b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3458b-116">Problèmes</span><span class="sxs-lookup"><span data-stu-id="3458b-116">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3458b-117">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="3458b-117">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3458b-118">Groupes de règles</span><span class="sxs-lookup"><span data-stu-id="3458b-118">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3458b-119">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="3458b-119">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3458b-120">Propriétésla</span><span class="sxs-lookup"><span data-stu-id="3458b-120">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3458b-121">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="3458b-121">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3458b-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="3458b-122">Attributes</span></span>

<span data-ttu-id="3458b-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3458b-123">None.</span></span>
  

