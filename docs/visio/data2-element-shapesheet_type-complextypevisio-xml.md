---
title: Données2, élément (ShapeSheet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e823797e-dde9-6ee7-b5e4-9e57cef90b08
description: Contient une valeur de chaîne arbitraire qui est utilisée pour fournir des informations supplémentaires sur une forme.
ms.openlocfilehash: ebd70fc0f83bd7cbf0bd6465c5e06276675a8022
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344617"
---
# <a name="data2-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="e1a0b-103">Données2, élément (ShapeSheet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e1a0b-103">Data2 element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e1a0b-104">Contient une valeur de chaîne arbitraire qui est utilisée pour fournir des informations supplémentaires sur une forme.</span><span class="sxs-lookup"><span data-stu-id="e1a0b-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e1a0b-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="e1a0b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1a0b-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="e1a0b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e1a0b-107">Type_de_données</span><span class="sxs-lookup"><span data-stu-id="e1a0b-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e1a0b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e1a0b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e1a0b-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e1a0b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e1a0b-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="e1a0b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e1a0b-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="e1a0b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e1a0b-112">page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="e1a0b-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e1a0b-113">Définition</span><span class="sxs-lookup"><span data-stu-id="e1a0b-113">Definition</span></span>

```XML
< xs:element name="Data2" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e1a0b-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e1a0b-114">Elements and attributes</span></span>

<span data-ttu-id="e1a0b-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="e1a0b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e1a0b-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e1a0b-116">Parent elements</span></span>

|<span data-ttu-id="e1a0b-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e1a0b-117">**Element**</span></span>|<span data-ttu-id="e1a0b-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="e1a0b-118">**Type**</span></span>|<span data-ttu-id="e1a0b-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="e1a0b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e1a0b-120">Forme</span><span class="sxs-lookup"><span data-stu-id="e1a0b-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e1a0b-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="e1a0b-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e1a0b-122">Contient des éléments qui définissent une forme dans un élément de forme de forme de **base**, de **page**ou de groupe.</span><span class="sxs-lookup"><span data-stu-id="e1a0b-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e1a0b-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e1a0b-123">Child elements</span></span>

<span data-ttu-id="e1a0b-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e1a0b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e1a0b-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="e1a0b-125">Attributes</span></span>

<span data-ttu-id="e1a0b-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e1a0b-126">None.</span></span>
  

