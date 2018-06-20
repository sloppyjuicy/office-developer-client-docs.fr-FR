---
title: Type complexe AuthorEntry_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 39cf47915230b18d22db78f5470fd9c26b9c77ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788019"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="50986-102">Type complexe AuthorEntry_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="50986-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="50986-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="50986-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50986-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="50986-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="50986-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="50986-105">**Schema file**</span></span> <br/> |<span data-ttu-id="50986-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="50986-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="50986-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="50986-107">**Extension base**</span></span> <br/> |<span data-ttu-id="50986-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="50986-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="50986-109">Définition</span><span class="sxs-lookup"><span data-stu-id="50986-109">Definition</span></span>

```XML
      <xs:complexType name="AuthorEntry_Type">
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="Initials"
  type="xsd:string"
    />
    <xs:attribute name="ResolutionID"
  type="xsd:string"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="50986-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="50986-110">Elements and attributes</span></span>

<span data-ttu-id="50986-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="50986-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="50986-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="50986-112">Child elements</span></span>

<span data-ttu-id="50986-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="50986-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50986-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="50986-114">Attributes</span></span>

|<span data-ttu-id="50986-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="50986-115">**Attribute**</span></span>|<span data-ttu-id="50986-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="50986-116">**Type**</span></span>|<span data-ttu-id="50986-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="50986-117">**Required**</span></span>|<span data-ttu-id="50986-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="50986-118">**Description**</span></span>|<span data-ttu-id="50986-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="50986-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="50986-120">ID</span><span class="sxs-lookup"><span data-stu-id="50986-120">ID</span></span>  <br/> |<span data-ttu-id="50986-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="50986-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="50986-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="50986-122">required</span></span>  <br/> ||<span data-ttu-id="50986-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="50986-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="50986-124">Initiales</span><span class="sxs-lookup"><span data-stu-id="50986-124">Initials</span></span>  <br/> |<span data-ttu-id="50986-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="50986-125">xsd:string</span></span>  <br/> |<span data-ttu-id="50986-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="50986-126">optional</span></span>  <br/> ||<span data-ttu-id="50986-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="50986-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="50986-128">Nom</span><span class="sxs-lookup"><span data-stu-id="50986-128">Name</span></span>  <br/> |<span data-ttu-id="50986-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="50986-129">xsd:string</span></span>  <br/> |<span data-ttu-id="50986-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="50986-130">optional</span></span>  <br/> ||<span data-ttu-id="50986-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="50986-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="50986-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="50986-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="50986-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="50986-133">xsd:string</span></span>  <br/> |<span data-ttu-id="50986-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="50986-134">optional</span></span>  <br/> ||<span data-ttu-id="50986-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="50986-135">Values of the xsd:string type.</span></span>  <br/> |
   

