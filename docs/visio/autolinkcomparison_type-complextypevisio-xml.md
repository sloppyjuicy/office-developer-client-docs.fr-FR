---
title: Type complexe AutoLinkComparison_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: 235b63777d21955a2f2062757d6a54e899b169ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389749"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="0bd82-102">Type complexe AutoLinkComparison_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="0bd82-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0bd82-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="0bd82-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0bd82-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="0bd82-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0bd82-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0bd82-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0bd82-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0bd82-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0bd82-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="0bd82-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0bd82-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="0bd82-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0bd82-109">Définition</span><span class="sxs-lookup"><span data-stu-id="0bd82-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0bd82-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0bd82-110">Elements and attributes</span></span>

<span data-ttu-id="0bd82-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="0bd82-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0bd82-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0bd82-112">Child elements</span></span>

<span data-ttu-id="0bd82-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0bd82-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0bd82-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="0bd82-114">Attributes</span></span>

|<span data-ttu-id="0bd82-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0bd82-115">**Attribute**</span></span>|<span data-ttu-id="0bd82-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="0bd82-116">**Type**</span></span>|<span data-ttu-id="0bd82-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="0bd82-117">**Required**</span></span>|<span data-ttu-id="0bd82-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="0bd82-118">**Description**</span></span>|<span data-ttu-id="0bd82-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="0bd82-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0bd82-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="0bd82-120">ColumnName</span></span>  <br/> |<span data-ttu-id="0bd82-121">XSD : String</span><span class="sxs-lookup"><span data-stu-id="0bd82-121">xsd:string</span></span>  <br/> |<span data-ttu-id="0bd82-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="0bd82-122">required</span></span>  <br/> ||<span data-ttu-id="0bd82-123">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="0bd82-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0bd82-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="0bd82-124">ContextType</span></span>  <br/> |<span data-ttu-id="0bd82-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0bd82-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0bd82-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="0bd82-126">required</span></span>  <br/> ||<span data-ttu-id="0bd82-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0bd82-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0bd82-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="0bd82-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="0bd82-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="0bd82-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0bd82-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="0bd82-130">optional</span></span>  <br/> ||<span data-ttu-id="0bd82-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="0bd82-131">Values of the xsd:string type.</span></span>  <br/> |
   

