---
title: Type complexe ColorEntry_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: 58a0abdd4f7f8c2014ec8c6763441840a07b93db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788263"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="fc0cd-102">Type complexe ColorEntry_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="fc0cd-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fc0cd-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="fc0cd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc0cd-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="fc0cd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fc0cd-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fc0cd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fc0cd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fc0cd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fc0cd-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="fc0cd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fc0cd-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="fc0cd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fc0cd-109">Définition</span><span class="sxs-lookup"><span data-stu-id="fc0cd-109">Definition</span></span>

```XML
      <xs:complexType name="ColorEntry_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RGB"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fc0cd-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fc0cd-110">Elements and attributes</span></span>

<span data-ttu-id="fc0cd-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="fc0cd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fc0cd-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fc0cd-112">Child elements</span></span>

<span data-ttu-id="fc0cd-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fc0cd-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc0cd-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="fc0cd-114">Attributes</span></span>

|<span data-ttu-id="fc0cd-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fc0cd-115">**Attribute**</span></span>|<span data-ttu-id="fc0cd-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="fc0cd-116">**Type**</span></span>|<span data-ttu-id="fc0cd-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="fc0cd-117">**Required**</span></span>|<span data-ttu-id="fc0cd-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="fc0cd-118">**Description**</span></span>|<span data-ttu-id="fc0cd-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="fc0cd-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fc0cd-120">IX</span><span class="sxs-lookup"><span data-stu-id="fc0cd-120">IX</span></span>  <br/> |<span data-ttu-id="fc0cd-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fc0cd-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fc0cd-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fc0cd-122">required</span></span>  <br/> ||<span data-ttu-id="fc0cd-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fc0cd-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fc0cd-124">RVB</span><span class="sxs-lookup"><span data-stu-id="fc0cd-124">RGB</span></span>  <br/> |<span data-ttu-id="fc0cd-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="fc0cd-125">xsd:string</span></span>  <br/> |<span data-ttu-id="fc0cd-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fc0cd-126">required</span></span>  <br/> ||<span data-ttu-id="fc0cd-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="fc0cd-127">Values of the xsd:string type.</span></span>  <br/> |
   

