---
title: Type complexe RuleInfo_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0a0ac32729b83a5d648b2826bffe5a9df4d9fc0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789562"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="c35d5-102">Type complexe RuleInfo_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="c35d5-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c35d5-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c35d5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c35d5-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c35d5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c35d5-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c35d5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c35d5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c35d5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c35d5-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c35d5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c35d5-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="c35d5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c35d5-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c35d5-109">Definition</span></span>

```XML
      <xs:complexType name="RuleInfo_Type">
    <xs:attribute name="RuleSetID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RuleID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c35d5-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c35d5-110">Elements and attributes</span></span>

<span data-ttu-id="c35d5-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c35d5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c35d5-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c35d5-112">Child elements</span></span>

<span data-ttu-id="c35d5-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c35d5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c35d5-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="c35d5-114">Attributes</span></span>

|<span data-ttu-id="c35d5-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c35d5-115">**Attribute**</span></span>|<span data-ttu-id="c35d5-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="c35d5-116">**Type**</span></span>|<span data-ttu-id="c35d5-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c35d5-117">**Required**</span></span>|<span data-ttu-id="c35d5-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="c35d5-118">**Description**</span></span>|<span data-ttu-id="c35d5-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c35d5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c35d5-120">ID de la règle</span><span class="sxs-lookup"><span data-stu-id="c35d5-120">RuleID</span></span>  <br/> |<span data-ttu-id="c35d5-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c35d5-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c35d5-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c35d5-122">required</span></span>  <br/> ||<span data-ttu-id="c35d5-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c35d5-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c35d5-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="c35d5-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="c35d5-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c35d5-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c35d5-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c35d5-126">required</span></span>  <br/> ||<span data-ttu-id="c35d5-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c35d5-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

