---
title: Type complexe RowMap_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 18f573a480e3ae057074a219def192f6b1b2829b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789553"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="fcf52-102">Type complexe RowMap_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="fcf52-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fcf52-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="fcf52-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcf52-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="fcf52-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fcf52-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fcf52-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fcf52-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fcf52-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fcf52-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="fcf52-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fcf52-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="fcf52-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fcf52-109">Définition</span><span class="sxs-lookup"><span data-stu-id="fcf52-109">Definition</span></span>

```XML
      <xs:complexType name="RowMap_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
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

## <a name="elements-and-attributes"></a><span data-ttu-id="fcf52-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fcf52-110">Elements and attributes</span></span>

<span data-ttu-id="fcf52-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="fcf52-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fcf52-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fcf52-112">Child elements</span></span>

<span data-ttu-id="fcf52-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fcf52-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fcf52-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="fcf52-114">Attributes</span></span>

|<span data-ttu-id="fcf52-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fcf52-115">**Attribute**</span></span>|<span data-ttu-id="fcf52-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="fcf52-116">**Type**</span></span>|<span data-ttu-id="fcf52-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="fcf52-117">**Required**</span></span>|<span data-ttu-id="fcf52-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="fcf52-118">**Description**</span></span>|<span data-ttu-id="fcf52-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="fcf52-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fcf52-120">PageID</span><span class="sxs-lookup"><span data-stu-id="fcf52-120">PageID</span></span>  <br/> |<span data-ttu-id="fcf52-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fcf52-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fcf52-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fcf52-122">required</span></span>  <br/> ||<span data-ttu-id="fcf52-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fcf52-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fcf52-124">RowID</span><span class="sxs-lookup"><span data-stu-id="fcf52-124">RowID</span></span>  <br/> |<span data-ttu-id="fcf52-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fcf52-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fcf52-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fcf52-126">required</span></span>  <br/> ||<span data-ttu-id="fcf52-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fcf52-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fcf52-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="fcf52-128">ShapeID</span></span>  <br/> |<span data-ttu-id="fcf52-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fcf52-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fcf52-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fcf52-130">required</span></span>  <br/> ||<span data-ttu-id="fcf52-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fcf52-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

