---
title: Type complexe RefBy_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 5042a618420a72284e0ef75c5d624c6f5464e162
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789397"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="09636-102">Type complexe RefBy_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="09636-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="09636-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="09636-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09636-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="09636-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="09636-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="09636-105">**Schema file**</span></span> <br/> |<span data-ttu-id="09636-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="09636-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="09636-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="09636-107">**Extension base**</span></span> <br/> |<span data-ttu-id="09636-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="09636-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="09636-109">Définition</span><span class="sxs-lookup"><span data-stu-id="09636-109">Definition</span></span>

```XML
      <xs:complexType name="RefBy_Type">
    <xs:attribute name="T"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="09636-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="09636-110">Elements and attributes</span></span>

<span data-ttu-id="09636-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="09636-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="09636-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="09636-112">Child elements</span></span>

<span data-ttu-id="09636-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="09636-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09636-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="09636-114">Attributes</span></span>

|<span data-ttu-id="09636-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="09636-115">**Attribute**</span></span>|<span data-ttu-id="09636-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="09636-116">**Type**</span></span>|<span data-ttu-id="09636-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="09636-117">**Required**</span></span>|<span data-ttu-id="09636-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="09636-118">**Description**</span></span>|<span data-ttu-id="09636-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="09636-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="09636-120">ID</span><span class="sxs-lookup"><span data-stu-id="09636-120">ID</span></span>  <br/> |<span data-ttu-id="09636-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09636-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09636-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="09636-122">required</span></span>  <br/> ||<span data-ttu-id="09636-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="09636-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09636-124">T</span><span class="sxs-lookup"><span data-stu-id="09636-124">T</span></span>  <br/> |<span data-ttu-id="09636-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="09636-125">xsd:string</span></span>  <br/> |<span data-ttu-id="09636-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="09636-126">required</span></span>  <br/> ||<span data-ttu-id="09636-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="09636-127">Values of the xsd:string type.</span></span>  <br/> |
   

