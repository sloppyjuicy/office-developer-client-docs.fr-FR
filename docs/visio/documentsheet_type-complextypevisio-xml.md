---
title: Type complexe DocumentSheet_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 47378b039d11294dcb566f61cf20b0ed1ed7fed8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788509"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="33381-102">Type complexe DocumentSheet_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="33381-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="33381-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="33381-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33381-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="33381-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="33381-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="33381-105">**Schema file**</span></span> <br/> |<span data-ttu-id="33381-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="33381-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="33381-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="33381-107">**Extension base**</span></span> <br/> |<span data-ttu-id="33381-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="33381-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="33381-109">Définition</span><span class="sxs-lookup"><span data-stu-id="33381-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="33381-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="33381-110">Elements and attributes</span></span>

<span data-ttu-id="33381-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="33381-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="33381-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="33381-112">Child elements</span></span>

<span data-ttu-id="33381-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="33381-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33381-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="33381-114">Attributes</span></span>

|<span data-ttu-id="33381-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="33381-115">**Attribute**</span></span>|<span data-ttu-id="33381-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="33381-116">**Type**</span></span>|<span data-ttu-id="33381-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="33381-117">**Required**</span></span>|<span data-ttu-id="33381-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="33381-118">**Description**</span></span>|<span data-ttu-id="33381-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="33381-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="33381-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="33381-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="33381-121">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="33381-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="33381-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="33381-122">optional</span></span>  <br/> ||<span data-ttu-id="33381-123">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="33381-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="33381-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="33381-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="33381-125">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="33381-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="33381-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="33381-126">optional</span></span>  <br/> ||<span data-ttu-id="33381-127">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="33381-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="33381-128">Nom</span><span class="sxs-lookup"><span data-stu-id="33381-128">Name</span></span>  <br/> |<span data-ttu-id="33381-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="33381-129">xsd:string</span></span>  <br/> |<span data-ttu-id="33381-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="33381-130">optional</span></span>  <br/> ||<span data-ttu-id="33381-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="33381-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="33381-132">NameU</span><span class="sxs-lookup"><span data-stu-id="33381-132">NameU</span></span>  <br/> |<span data-ttu-id="33381-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="33381-133">xsd:string</span></span>  <br/> |<span data-ttu-id="33381-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="33381-134">optional</span></span>  <br/> ||<span data-ttu-id="33381-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="33381-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="33381-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="33381-136">UniqueID</span></span>  <br/> |<span data-ttu-id="33381-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="33381-137">xsd:string</span></span>  <br/> |<span data-ttu-id="33381-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="33381-138">optional</span></span>  <br/> ||<span data-ttu-id="33381-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="33381-139">Values of the xsd:string type.</span></span>  <br/> |
   

