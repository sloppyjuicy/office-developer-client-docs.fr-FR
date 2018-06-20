---
title: Élément MasterContents (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Spécifie des informations sur les formes dans une forme de base dans un dessin.
ms.openlocfilehash: d1ba67a414ac80be9da2beebb93acc89faf71172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789072"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="0ce2c-103">Élément MasterContents (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="0ce2c-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="0ce2c-104">Spécifie des informations sur les formes dans une forme de base dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="0ce2c-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="0ce2c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ce2c-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="0ce2c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0ce2c-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="0ce2c-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0ce2c-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="0ce2c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0ce2c-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0ce2c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0ce2c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0ce2c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0ce2c-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="0ce2c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0ce2c-112">maître # .xml</span><span class="sxs-lookup"><span data-stu-id="0ce2c-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0ce2c-113">Définition</span><span class="sxs-lookup"><span data-stu-id="0ce2c-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0ce2c-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0ce2c-114">Elements and attributes</span></span>

<span data-ttu-id="0ce2c-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0ce2c-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0ce2c-116">Parent elements</span></span>

<span data-ttu-id="0ce2c-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ce2c-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0ce2c-118">Child elements</span></span>

|<span data-ttu-id="0ce2c-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0ce2c-119">**Element**</span></span>|<span data-ttu-id="0ce2c-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="0ce2c-120">**Type**</span></span>|<span data-ttu-id="0ce2c-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="0ce2c-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0ce2c-122">Se connecte</span><span class="sxs-lookup"><span data-stu-id="0ce2c-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ce2c-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="0ce2c-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0ce2c-124">Contient un élément de **connexion** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="0ce2c-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="0ce2c-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ce2c-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="0ce2c-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0ce2c-127">Contient une collection d’éléments de la **forme** .</span><span class="sxs-lookup"><span data-stu-id="0ce2c-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0ce2c-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="0ce2c-128">Attributes</span></span>

<span data-ttu-id="0ce2c-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0ce2c-129">None.</span></span>
  

