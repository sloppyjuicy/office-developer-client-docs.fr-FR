---
title: Type complexe RefBy_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: ebfc84b2e7eb88078b3b8010f0a7001e90a9cb31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383482"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="7b5e7-102">Type complexe RefBy_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="7b5e7-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7b5e7-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7b5e7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b5e7-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="7b5e7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7b5e7-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7b5e7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7b5e7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7b5e7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7b5e7-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7b5e7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7b5e7-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="7b5e7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7b5e7-109">Définition</span><span class="sxs-lookup"><span data-stu-id="7b5e7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7b5e7-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7b5e7-110">Elements and attributes</span></span>

<span data-ttu-id="7b5e7-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7b5e7-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7b5e7-112">Child elements</span></span>

<span data-ttu-id="7b5e7-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b5e7-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="7b5e7-114">Attributes</span></span>

|<span data-ttu-id="7b5e7-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7b5e7-115">**Attribute**</span></span>|<span data-ttu-id="7b5e7-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="7b5e7-116">**Type**</span></span>|<span data-ttu-id="7b5e7-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="7b5e7-117">**Required**</span></span>|<span data-ttu-id="7b5e7-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="7b5e7-118">**Description**</span></span>|<span data-ttu-id="7b5e7-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="7b5e7-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7b5e7-120">ID</span><span class="sxs-lookup"><span data-stu-id="7b5e7-120">ID</span></span>  <br/> |<span data-ttu-id="7b5e7-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7b5e7-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7b5e7-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7b5e7-122">required</span></span>  <br/> ||<span data-ttu-id="7b5e7-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7b5e7-124">T</span><span class="sxs-lookup"><span data-stu-id="7b5e7-124">T</span></span>  <br/> |<span data-ttu-id="7b5e7-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="7b5e7-125">xsd:string</span></span>  <br/> |<span data-ttu-id="7b5e7-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7b5e7-126">required</span></span>  <br/> ||<span data-ttu-id="7b5e7-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="7b5e7-127">Values of the xsd:string type.</span></span>  <br/> |
   

