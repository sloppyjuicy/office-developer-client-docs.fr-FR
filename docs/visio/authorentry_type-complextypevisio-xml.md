---
title: ComplexType AuthorEntry_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 7d43d34559f212e3de1a91291cbf14b75a3b2e0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341383"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="ff859-102">ComplexType AuthorEntry_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ff859-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ff859-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="ff859-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff859-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ff859-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ff859-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ff859-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ff859-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ff859-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ff859-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="ff859-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ff859-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="ff859-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ff859-109">Définition</span><span class="sxs-lookup"><span data-stu-id="ff859-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ff859-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ff859-110">Elements and attributes</span></span>

<span data-ttu-id="ff859-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="ff859-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ff859-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ff859-112">Child elements</span></span>

<span data-ttu-id="ff859-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ff859-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff859-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="ff859-114">Attributes</span></span>

|<span data-ttu-id="ff859-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ff859-115">**Attribute**</span></span>|<span data-ttu-id="ff859-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="ff859-116">**Type**</span></span>|<span data-ttu-id="ff859-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ff859-117">**Required**</span></span>|<span data-ttu-id="ff859-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="ff859-118">**Description**</span></span>|<span data-ttu-id="ff859-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ff859-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ff859-120">ID</span><span class="sxs-lookup"><span data-stu-id="ff859-120">ID</span></span>  <br/> |<span data-ttu-id="ff859-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff859-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff859-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ff859-122">required</span></span>  <br/> ||<span data-ttu-id="ff859-123">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff859-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff859-124">Initiales</span><span class="sxs-lookup"><span data-stu-id="ff859-124">Initials</span></span>  <br/> |<span data-ttu-id="ff859-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ff859-125">xsd:string</span></span>  <br/> |<span data-ttu-id="ff859-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff859-126">optional</span></span>  <br/> ||<span data-ttu-id="ff859-127">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff859-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff859-128">Nom</span><span class="sxs-lookup"><span data-stu-id="ff859-128">Name</span></span>  <br/> |<span data-ttu-id="ff859-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ff859-129">xsd:string</span></span>  <br/> |<span data-ttu-id="ff859-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff859-130">optional</span></span>  <br/> ||<span data-ttu-id="ff859-131">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff859-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff859-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="ff859-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="ff859-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ff859-133">xsd:string</span></span>  <br/> |<span data-ttu-id="ff859-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff859-134">optional</span></span>  <br/> ||<span data-ttu-id="ff859-135">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff859-135">Values of the xsd:string type.</span></span>  <br/> |
   

