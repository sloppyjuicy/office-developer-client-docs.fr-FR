---
title: Type complexe AutoLinkComparison_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: bb1b07a59fbe3fc706bc67db58e67c5b0ec14033
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788034"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="fcb89-102">Type complexe AutoLinkComparison_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="fcb89-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fcb89-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="fcb89-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcb89-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="fcb89-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fcb89-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fcb89-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fcb89-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fcb89-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fcb89-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="fcb89-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fcb89-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="fcb89-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fcb89-109">Définition</span><span class="sxs-lookup"><span data-stu-id="fcb89-109">Definition</span></span>

```XML
      <xs:complexType name="AutoLinkComparison_Type">
    <xs:attribute name="ColumnName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ContextType"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ContextTypeLabel"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fcb89-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fcb89-110">Elements and attributes</span></span>

<span data-ttu-id="fcb89-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="fcb89-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fcb89-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fcb89-112">Child elements</span></span>

<span data-ttu-id="fcb89-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fcb89-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fcb89-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="fcb89-114">Attributes</span></span>

|<span data-ttu-id="fcb89-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fcb89-115">**Attribute**</span></span>|<span data-ttu-id="fcb89-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="fcb89-116">**Type**</span></span>|<span data-ttu-id="fcb89-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="fcb89-117">**Required**</span></span>|<span data-ttu-id="fcb89-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="fcb89-118">**Description**</span></span>|<span data-ttu-id="fcb89-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="fcb89-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fcb89-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="fcb89-120">ColumnName</span></span>  <br/> |<span data-ttu-id="fcb89-121">XSD : String</span><span class="sxs-lookup"><span data-stu-id="fcb89-121">xsd:string</span></span>  <br/> |<span data-ttu-id="fcb89-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fcb89-122">required</span></span>  <br/> ||<span data-ttu-id="fcb89-123">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="fcb89-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fcb89-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="fcb89-124">ContextType</span></span>  <br/> |<span data-ttu-id="fcb89-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fcb89-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fcb89-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fcb89-126">required</span></span>  <br/> ||<span data-ttu-id="fcb89-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fcb89-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fcb89-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="fcb89-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="fcb89-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="fcb89-129">xsd:string</span></span>  <br/> |<span data-ttu-id="fcb89-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="fcb89-130">optional</span></span>  <br/> ||<span data-ttu-id="fcb89-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="fcb89-131">Values of the xsd:string type.</span></span>  <br/> |
   

