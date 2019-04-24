---
title: ComplexType IssueTarget_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: d7b8309bb6dac9648d379c89687dc89165f44edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314923"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="19a02-102">ComplexType IssueTarget_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="19a02-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="19a02-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="19a02-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19a02-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="19a02-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="19a02-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="19a02-105">**Schema file**</span></span> <br/> |<span data-ttu-id="19a02-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="19a02-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="19a02-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="19a02-107">**Extension base**</span></span> <br/> |<span data-ttu-id="19a02-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="19a02-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="19a02-109">Définition</span><span class="sxs-lookup"><span data-stu-id="19a02-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="19a02-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="19a02-110">Elements and attributes</span></span>

<span data-ttu-id="19a02-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="19a02-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="19a02-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="19a02-112">Child elements</span></span>

<span data-ttu-id="19a02-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="19a02-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19a02-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="19a02-114">Attributes</span></span>

|<span data-ttu-id="19a02-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="19a02-115">**Attribute**</span></span>|<span data-ttu-id="19a02-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="19a02-116">**Type**</span></span>|<span data-ttu-id="19a02-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="19a02-117">**Required**</span></span>|<span data-ttu-id="19a02-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="19a02-118">**Description**</span></span>|<span data-ttu-id="19a02-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="19a02-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="19a02-120">PageID</span><span class="sxs-lookup"><span data-stu-id="19a02-120">PageID</span></span>  <br/> |<span data-ttu-id="19a02-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19a02-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19a02-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="19a02-122">required</span></span>  <br/> ||<span data-ttu-id="19a02-123">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19a02-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19a02-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="19a02-124">ShapeID</span></span>  <br/> |<span data-ttu-id="19a02-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19a02-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19a02-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="19a02-126">required</span></span>  <br/> ||<span data-ttu-id="19a02-127">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19a02-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

