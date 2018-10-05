---
title: Type complexe StyleSheet_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 19440ab1365ff82bd37d705115fd123dcb630aba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396000"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="a8cde-102">Type complexe StyleSheet_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="a8cde-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a8cde-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a8cde-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8cde-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="a8cde-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a8cde-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a8cde-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a8cde-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a8cde-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a8cde-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a8cde-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a8cde-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="a8cde-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a8cde-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a8cde-109">Definition</span></span>

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
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
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a8cde-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a8cde-110">Elements and attributes</span></span>

<span data-ttu-id="a8cde-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="a8cde-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a8cde-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a8cde-112">Child elements</span></span>

<span data-ttu-id="a8cde-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a8cde-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8cde-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="a8cde-114">Attributes</span></span>

|<span data-ttu-id="a8cde-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a8cde-115">**Attribute**</span></span>|<span data-ttu-id="a8cde-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="a8cde-116">**Type**</span></span>|<span data-ttu-id="a8cde-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a8cde-117">**Required**</span></span>|<span data-ttu-id="a8cde-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8cde-118">**Description**</span></span>|<span data-ttu-id="a8cde-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a8cde-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8cde-120">ID</span><span class="sxs-lookup"><span data-stu-id="a8cde-120">ID</span></span>  <br/> |<span data-ttu-id="a8cde-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8cde-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a8cde-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8cde-122">required</span></span>  <br/> ||<span data-ttu-id="a8cde-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a8cde-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a8cde-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="a8cde-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="a8cde-125">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="a8cde-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a8cde-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8cde-126">optional</span></span>  <br/> ||<span data-ttu-id="a8cde-127">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="a8cde-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a8cde-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="a8cde-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="a8cde-129">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="a8cde-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a8cde-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8cde-130">optional</span></span>  <br/> ||<span data-ttu-id="a8cde-131">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="a8cde-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a8cde-132">Nom</span><span class="sxs-lookup"><span data-stu-id="a8cde-132">Name</span></span>  <br/> |<span data-ttu-id="a8cde-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="a8cde-133">xsd:string</span></span>  <br/> |<span data-ttu-id="a8cde-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8cde-134">optional</span></span>  <br/> ||<span data-ttu-id="a8cde-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="a8cde-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a8cde-136">NameU</span><span class="sxs-lookup"><span data-stu-id="a8cde-136">NameU</span></span>  <br/> |<span data-ttu-id="a8cde-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="a8cde-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a8cde-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="a8cde-138">optional</span></span>  <br/> ||<span data-ttu-id="a8cde-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="a8cde-139">Values of the xsd:string type.</span></span>  <br/> |
   

