---
title: Type complexe AuthorEntry_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 7d43d34559f212e3de1a91291cbf14b75a3b2e0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386837"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="43cb9-102">Type complexe AuthorEntry_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="43cb9-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="43cb9-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="43cb9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43cb9-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="43cb9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="43cb9-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="43cb9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="43cb9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="43cb9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="43cb9-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="43cb9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="43cb9-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="43cb9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43cb9-109">Définition</span><span class="sxs-lookup"><span data-stu-id="43cb9-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="43cb9-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="43cb9-110">Elements and attributes</span></span>

<span data-ttu-id="43cb9-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="43cb9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="43cb9-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="43cb9-112">Child elements</span></span>

<span data-ttu-id="43cb9-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="43cb9-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43cb9-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="43cb9-114">Attributes</span></span>

|<span data-ttu-id="43cb9-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="43cb9-115">**Attribute**</span></span>|<span data-ttu-id="43cb9-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="43cb9-116">**Type**</span></span>|<span data-ttu-id="43cb9-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="43cb9-117">**Required**</span></span>|<span data-ttu-id="43cb9-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="43cb9-118">**Description**</span></span>|<span data-ttu-id="43cb9-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="43cb9-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="43cb9-120">ID</span><span class="sxs-lookup"><span data-stu-id="43cb9-120">ID</span></span>  <br/> |<span data-ttu-id="43cb9-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="43cb9-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="43cb9-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="43cb9-122">required</span></span>  <br/> ||<span data-ttu-id="43cb9-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="43cb9-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="43cb9-124">Initials</span><span class="sxs-lookup"><span data-stu-id="43cb9-124">Initials</span></span>  <br/> |<span data-ttu-id="43cb9-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="43cb9-125">xsd:string</span></span>  <br/> |<span data-ttu-id="43cb9-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="43cb9-126">optional</span></span>  <br/> ||<span data-ttu-id="43cb9-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="43cb9-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="43cb9-128">Nom</span><span class="sxs-lookup"><span data-stu-id="43cb9-128">Name</span></span>  <br/> |<span data-ttu-id="43cb9-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="43cb9-129">xsd:string</span></span>  <br/> |<span data-ttu-id="43cb9-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="43cb9-130">optional</span></span>  <br/> ||<span data-ttu-id="43cb9-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="43cb9-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="43cb9-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="43cb9-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="43cb9-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="43cb9-133">xsd:string</span></span>  <br/> |<span data-ttu-id="43cb9-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="43cb9-134">optional</span></span>  <br/> ||<span data-ttu-id="43cb9-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="43cb9-135">Values of the xsd:string type.</span></span>  <br/> |
   

