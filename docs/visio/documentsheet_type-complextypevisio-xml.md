---
title: Type complexe DocumentSheet_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: a1f51ef6f0340b4430860eabde3ad778e923fed0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396343"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="39fda-102">Type complexe DocumentSheet_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="39fda-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="39fda-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="39fda-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39fda-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="39fda-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="39fda-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="39fda-105">**Schema file**</span></span> <br/> |<span data-ttu-id="39fda-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="39fda-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="39fda-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="39fda-107">**Extension base**</span></span> <br/> |<span data-ttu-id="39fda-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="39fda-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="39fda-109">Définition</span><span class="sxs-lookup"><span data-stu-id="39fda-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="39fda-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="39fda-110">Elements and attributes</span></span>

<span data-ttu-id="39fda-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="39fda-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="39fda-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="39fda-112">Child elements</span></span>

<span data-ttu-id="39fda-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="39fda-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39fda-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="39fda-114">Attributes</span></span>

|<span data-ttu-id="39fda-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="39fda-115">**Attribute**</span></span>|<span data-ttu-id="39fda-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="39fda-116">**Type**</span></span>|<span data-ttu-id="39fda-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="39fda-117">**Required**</span></span>|<span data-ttu-id="39fda-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="39fda-118">**Description**</span></span>|<span data-ttu-id="39fda-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="39fda-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="39fda-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="39fda-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="39fda-121">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="39fda-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="39fda-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="39fda-122">optional</span></span>  <br/> ||<span data-ttu-id="39fda-123">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="39fda-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="39fda-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="39fda-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="39fda-125">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="39fda-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="39fda-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="39fda-126">optional</span></span>  <br/> ||<span data-ttu-id="39fda-127">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="39fda-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="39fda-128">Nom</span><span class="sxs-lookup"><span data-stu-id="39fda-128">Name</span></span>  <br/> |<span data-ttu-id="39fda-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="39fda-129">xsd:string</span></span>  <br/> |<span data-ttu-id="39fda-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="39fda-130">optional</span></span>  <br/> ||<span data-ttu-id="39fda-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="39fda-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="39fda-132">NameU</span><span class="sxs-lookup"><span data-stu-id="39fda-132">NameU</span></span>  <br/> |<span data-ttu-id="39fda-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="39fda-133">xsd:string</span></span>  <br/> |<span data-ttu-id="39fda-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="39fda-134">optional</span></span>  <br/> ||<span data-ttu-id="39fda-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="39fda-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="39fda-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="39fda-136">UniqueID</span></span>  <br/> |<span data-ttu-id="39fda-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="39fda-137">xsd:string</span></span>  <br/> |<span data-ttu-id="39fda-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="39fda-138">optional</span></span>  <br/> ||<span data-ttu-id="39fda-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="39fda-139">Values of the xsd:string type.</span></span>  <br/> |
   

