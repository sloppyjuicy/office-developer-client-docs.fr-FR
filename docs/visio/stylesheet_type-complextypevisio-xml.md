---
title: Type complexe StyleSheet_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 394712b65ee44a939a20fd3b65df504785f106ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789844"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="0997d-102">Type complexe StyleSheet_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="0997d-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0997d-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="0997d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0997d-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="0997d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0997d-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0997d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0997d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0997d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0997d-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="0997d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0997d-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="0997d-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0997d-109">Définition</span><span class="sxs-lookup"><span data-stu-id="0997d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0997d-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0997d-110">Elements and attributes</span></span>

<span data-ttu-id="0997d-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="0997d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0997d-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0997d-112">Child elements</span></span>

<span data-ttu-id="0997d-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0997d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0997d-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="0997d-114">Attributes</span></span>

|<span data-ttu-id="0997d-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0997d-115">**Attribute**</span></span>|<span data-ttu-id="0997d-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="0997d-116">**Type**</span></span>|<span data-ttu-id="0997d-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="0997d-117">**Required**</span></span>|<span data-ttu-id="0997d-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="0997d-118">**Description**</span></span>|<span data-ttu-id="0997d-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="0997d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0997d-120">ID</span><span class="sxs-lookup"><span data-stu-id="0997d-120">ID</span></span>  <br/> |<span data-ttu-id="0997d-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0997d-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0997d-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="0997d-122">required</span></span>  <br/> ||<span data-ttu-id="0997d-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0997d-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0997d-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="0997d-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="0997d-125">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="0997d-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0997d-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="0997d-126">optional</span></span>  <br/> ||<span data-ttu-id="0997d-127">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="0997d-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0997d-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="0997d-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="0997d-129">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="0997d-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0997d-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="0997d-130">optional</span></span>  <br/> ||<span data-ttu-id="0997d-131">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="0997d-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0997d-132">Nom</span><span class="sxs-lookup"><span data-stu-id="0997d-132">Name</span></span>  <br/> |<span data-ttu-id="0997d-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="0997d-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0997d-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="0997d-134">optional</span></span>  <br/> ||<span data-ttu-id="0997d-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="0997d-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0997d-136">NameU</span><span class="sxs-lookup"><span data-stu-id="0997d-136">NameU</span></span>  <br/> |<span data-ttu-id="0997d-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="0997d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0997d-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="0997d-138">optional</span></span>  <br/> ||<span data-ttu-id="0997d-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="0997d-139">Values of the xsd:string type.</span></span>  <br/> |
   

