---
title: AutoLinkComparison_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: eeb58a0e2f401c0e8a2bcf67147bc300bb8535ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537884"
---
# <a name="autolinkcomparison_type-complextype-visio-xml"></a><span data-ttu-id="af9ce-102">AutoLinkComparison_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="af9ce-102">AutoLinkComparison_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="af9ce-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="af9ce-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af9ce-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="af9ce-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="af9ce-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="af9ce-105">**Schema file**</span></span> <br/> |<span data-ttu-id="af9ce-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="af9ce-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="af9ce-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="af9ce-107">**Extension base**</span></span> <br/> |<span data-ttu-id="af9ce-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="af9ce-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="af9ce-109">Définition</span><span class="sxs-lookup"><span data-stu-id="af9ce-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="af9ce-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="af9ce-110">Elements and attributes</span></span>

<span data-ttu-id="af9ce-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="af9ce-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="af9ce-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="af9ce-112">Child elements</span></span>

<span data-ttu-id="af9ce-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="af9ce-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af9ce-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="af9ce-114">Attributes</span></span>

|<span data-ttu-id="af9ce-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="af9ce-115">**Attribute**</span></span>|<span data-ttu-id="af9ce-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="af9ce-116">**Type**</span></span>|<span data-ttu-id="af9ce-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="af9ce-117">**Required**</span></span>|<span data-ttu-id="af9ce-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="af9ce-118">**Description**</span></span>|<span data-ttu-id="af9ce-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="af9ce-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="af9ce-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="af9ce-120">ColumnName</span></span>  <br/> |<span data-ttu-id="af9ce-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="af9ce-121">xsd:string</span></span>  <br/> |<span data-ttu-id="af9ce-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="af9ce-122">required</span></span>  <br/> ||<span data-ttu-id="af9ce-123">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="af9ce-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="af9ce-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="af9ce-124">ContextType</span></span>  <br/> |<span data-ttu-id="af9ce-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="af9ce-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af9ce-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="af9ce-126">required</span></span>  <br/> ||<span data-ttu-id="af9ce-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="af9ce-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af9ce-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="af9ce-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="af9ce-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="af9ce-129">xsd:string</span></span>  <br/> |<span data-ttu-id="af9ce-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="af9ce-130">optional</span></span>  <br/> ||<span data-ttu-id="af9ce-131">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="af9ce-131">Values of the xsd:string type.</span></span>  <br/> |
   

