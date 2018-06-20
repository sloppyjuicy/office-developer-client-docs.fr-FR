---
title: Type complexe IssueTarget_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: b9e69edc5bd30ede969bc77d43501a4473e9f69e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788870"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="d7d6f-102">Type complexe IssueTarget_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="d7d6f-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d7d6f-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="d7d6f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7d6f-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="d7d6f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d7d6f-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d7d6f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d7d6f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d7d6f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d7d6f-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="d7d6f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d7d6f-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="d7d6f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d7d6f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="d7d6f-109">Definition</span></span>

```XML
      <xs:complexType name="IssueTarget_Type">
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d7d6f-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d7d6f-110">Elements and attributes</span></span>

<span data-ttu-id="d7d6f-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="d7d6f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d7d6f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d7d6f-112">Child elements</span></span>

<span data-ttu-id="d7d6f-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d7d6f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7d6f-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="d7d6f-114">Attributes</span></span>

|<span data-ttu-id="d7d6f-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d7d6f-115">**Attribute**</span></span>|<span data-ttu-id="d7d6f-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="d7d6f-116">**Type**</span></span>|<span data-ttu-id="d7d6f-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d7d6f-117">**Required**</span></span>|<span data-ttu-id="d7d6f-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="d7d6f-118">**Description**</span></span>|<span data-ttu-id="d7d6f-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="d7d6f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d7d6f-120">PageID</span><span class="sxs-lookup"><span data-stu-id="d7d6f-120">PageID</span></span>  <br/> |<span data-ttu-id="d7d6f-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d7d6f-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d7d6f-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d7d6f-122">required</span></span>  <br/> ||<span data-ttu-id="d7d6f-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d7d6f-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d7d6f-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="d7d6f-124">ShapeID</span></span>  <br/> |<span data-ttu-id="d7d6f-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d7d6f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d7d6f-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d7d6f-126">required</span></span>  <br/> ||<span data-ttu-id="d7d6f-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d7d6f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

