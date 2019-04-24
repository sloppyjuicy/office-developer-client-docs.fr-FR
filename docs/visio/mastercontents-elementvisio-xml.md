---
title: Élément MasterContents ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Cette énumération spécifie les informations relatives aux formes d'une forme de base dans un dessin.
ms.openlocfilehash: 381afe288864553dc56bdf8bb6dc19861abdcc8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341355"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="c1c1f-103">Élément MasterContents ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c1c1f-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="c1c1f-104">Cette énumération spécifie les informations relatives aux formes d'une forme de base dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="c1c1f-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c1c1f-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="c1c1f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1c1f-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="c1c1f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c1c1f-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="c1c1f-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c1c1f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c1c1f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c1c1f-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c1c1f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c1c1f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c1c1f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c1c1f-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="c1c1f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c1c1f-112">Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="c1c1f-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1c1f-113">Définition</span><span class="sxs-lookup"><span data-stu-id="c1c1f-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c1c1f-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c1c1f-114">Elements and attributes</span></span>

<span data-ttu-id="c1c1f-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="c1c1f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c1c1f-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c1c1f-116">Parent elements</span></span>

<span data-ttu-id="c1c1f-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="c1c1f-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1c1f-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c1c1f-118">Child elements</span></span>

|<span data-ttu-id="c1c1f-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c1c1f-119">**Element**</span></span>|<span data-ttu-id="c1c1f-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="c1c1f-120">**Type**</span></span>|<span data-ttu-id="c1c1f-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="c1c1f-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1c1f-122">Connects</span><span class="sxs-lookup"><span data-stu-id="c1c1f-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1c1f-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="c1c1f-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1c1f-124">Contient un élément **Connect** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="c1c1f-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="c1c1f-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="c1c1f-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1c1f-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="c1c1f-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1c1f-127">Contient une collection d'éléments **Shape** .</span><span class="sxs-lookup"><span data-stu-id="c1c1f-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c1c1f-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="c1c1f-128">Attributes</span></span>

<span data-ttu-id="c1c1f-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c1c1f-129">None.</span></span>
  

