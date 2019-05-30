---
title: ComplexType ColorEntry_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: f5ada3fef8d50c2e53f63c797601980f88349868
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540146"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="55d03-102">ComplexType ColorEntry_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="55d03-102">ColorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="55d03-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="55d03-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55d03-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="55d03-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="55d03-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="55d03-105">**Schema file**</span></span> <br/> |<span data-ttu-id="55d03-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="55d03-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="55d03-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="55d03-107">**Extension base**</span></span> <br/> |<span data-ttu-id="55d03-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="55d03-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="55d03-109">Définition</span><span class="sxs-lookup"><span data-stu-id="55d03-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="55d03-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="55d03-110">Elements and attributes</span></span>

<span data-ttu-id="55d03-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="55d03-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="55d03-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="55d03-112">Child elements</span></span>

<span data-ttu-id="55d03-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="55d03-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55d03-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="55d03-114">Attributes</span></span>

|<span data-ttu-id="55d03-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="55d03-115">**Attribute**</span></span>|<span data-ttu-id="55d03-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="55d03-116">**Type**</span></span>|<span data-ttu-id="55d03-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="55d03-117">**Required**</span></span>|<span data-ttu-id="55d03-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="55d03-118">**Description**</span></span>|<span data-ttu-id="55d03-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="55d03-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="55d03-120">IX</span><span class="sxs-lookup"><span data-stu-id="55d03-120">IX</span></span>  <br/> |<span data-ttu-id="55d03-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="55d03-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="55d03-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="55d03-122">required</span></span>  <br/> ||<span data-ttu-id="55d03-123">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="55d03-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="55d03-124">RVB</span><span class="sxs-lookup"><span data-stu-id="55d03-124">RGB</span></span>  <br/> |<span data-ttu-id="55d03-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="55d03-125">xsd:string</span></span>  <br/> |<span data-ttu-id="55d03-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="55d03-126">required</span></span>  <br/> ||<span data-ttu-id="55d03-127">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="55d03-127">Values of the xsd:string type.</span></span>  <br/> |
   

