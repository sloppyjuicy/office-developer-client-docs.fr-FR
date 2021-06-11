---
title: Élément PageContents (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Spécifie les informations sur les formes d’une forme de base ou d’une page de dessin d’un dessin.
ms.openlocfilehash: 23ff6c74007adc5764007e34c1b2ac92c522b121
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537996"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="acd91-103">Élément PageContents (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="acd91-103">PageContents element (Visio XML)</span></span>

<span data-ttu-id="acd91-104">Spécifie les informations sur les formes d’une forme de base ou d’une page de dessin d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="acd91-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acd91-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="acd91-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acd91-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="acd91-106">**Element type**</span></span> <br/> |[<span data-ttu-id="acd91-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="acd91-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="acd91-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="acd91-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="acd91-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="acd91-109">**Schema file**</span></span> <br/> |<span data-ttu-id="acd91-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="acd91-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="acd91-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="acd91-111">**Document parts**</span></span> <br/> |<span data-ttu-id="acd91-112">page#.xml</span><span class="sxs-lookup"><span data-stu-id="acd91-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="acd91-113">Définition</span><span class="sxs-lookup"><span data-stu-id="acd91-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="acd91-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="acd91-114">Elements and attributes</span></span>

<span data-ttu-id="acd91-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="acd91-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="acd91-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="acd91-116">Parent elements</span></span>

<span data-ttu-id="acd91-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="acd91-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="acd91-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="acd91-118">Child elements</span></span>

|<span data-ttu-id="acd91-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="acd91-119">**Element**</span></span>|<span data-ttu-id="acd91-120">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="acd91-120">**Type**</span></span>|<span data-ttu-id="acd91-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="acd91-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="acd91-122">Connects</span><span class="sxs-lookup"><span data-stu-id="acd91-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acd91-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="acd91-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acd91-124">Contient un **Connecter** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="acd91-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="acd91-125">Formes</span><span class="sxs-lookup"><span data-stu-id="acd91-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acd91-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="acd91-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acd91-127">Spécifie une collection de formes.</span><span class="sxs-lookup"><span data-stu-id="acd91-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="acd91-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="acd91-128">Attributes</span></span>

<span data-ttu-id="acd91-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="acd91-129">None.</span></span>
  

