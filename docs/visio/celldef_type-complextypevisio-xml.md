---
title: Type complexe CellDef_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: bdcfadc36f278fc97b8589b2989d214e5f4b3333
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399983"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="3cbca-102">Type complexe CellDef_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="3cbca-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3cbca-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="3cbca-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3cbca-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="3cbca-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3cbca-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="3cbca-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3cbca-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3cbca-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3cbca-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="3cbca-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3cbca-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="3cbca-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3cbca-109">Définition</span><span class="sxs-lookup"><span data-stu-id="3cbca-109">Definition</span></span>

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3cbca-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="3cbca-110">Elements and attributes</span></span>

<span data-ttu-id="3cbca-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="3cbca-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3cbca-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3cbca-112">Child elements</span></span>

<span data-ttu-id="3cbca-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3cbca-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3cbca-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="3cbca-114">Attributes</span></span>

|<span data-ttu-id="3cbca-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3cbca-115">**Attribute**</span></span>|<span data-ttu-id="3cbca-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="3cbca-116">**Type**</span></span>|<span data-ttu-id="3cbca-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="3cbca-117">**Required**</span></span>|<span data-ttu-id="3cbca-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="3cbca-118">**Description**</span></span>|<span data-ttu-id="3cbca-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="3cbca-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3cbca-120">F</span><span class="sxs-lookup"><span data-stu-id="3cbca-120">F</span></span>  <br/> |<span data-ttu-id="3cbca-121">XSD : String</span><span class="sxs-lookup"><span data-stu-id="3cbca-121">xsd:string</span></span>  <br/> |<span data-ttu-id="3cbca-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="3cbca-122">optional</span></span>  <br/> ||<span data-ttu-id="3cbca-123">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="3cbca-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3cbca-124">IX</span><span class="sxs-lookup"><span data-stu-id="3cbca-124">IX</span></span>  <br/> |<span data-ttu-id="3cbca-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="3cbca-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="3cbca-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="3cbca-126">optional</span></span>  <br/> ||<span data-ttu-id="3cbca-127">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="3cbca-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="3cbca-128">N</span><span class="sxs-lookup"><span data-stu-id="3cbca-128">N</span></span>  <br/> |<span data-ttu-id="3cbca-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="3cbca-129">xsd:string</span></span>  <br/> |<span data-ttu-id="3cbca-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="3cbca-130">required</span></span>  <br/> ||<span data-ttu-id="3cbca-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="3cbca-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3cbca-132">S</span><span class="sxs-lookup"><span data-stu-id="3cbca-132">S</span></span>  <br/> |<span data-ttu-id="3cbca-133">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="3cbca-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="3cbca-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="3cbca-134">optional</span></span>  <br/> ||<span data-ttu-id="3cbca-135">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="3cbca-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="3cbca-136">T</span><span class="sxs-lookup"><span data-stu-id="3cbca-136">T</span></span>  <br/> |<span data-ttu-id="3cbca-137">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="3cbca-137">xsd:token</span></span>  <br/> |<span data-ttu-id="3cbca-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="3cbca-138">required</span></span>  <br/> ||<span data-ttu-id="3cbca-139">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="3cbca-139">Values of the xsd:token type.</span></span>  <br/> |
   

