---
title: Élément MasterContents (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Spécifie des informations sur les formes d’une forme de base dans un dessin.
ms.openlocfilehash: 26bc86aedeb96544f61f53052ab723b13b29500d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538038"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="19063-103">Élément MasterContents (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="19063-103">MasterContents element (Visio XML)</span></span>

<span data-ttu-id="19063-104">Spécifie des informations sur les formes d’une forme de base dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="19063-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="19063-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="19063-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19063-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="19063-106">**Element type**</span></span> <br/> |[<span data-ttu-id="19063-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="19063-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="19063-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="19063-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="19063-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="19063-109">**Schema file**</span></span> <br/> |<span data-ttu-id="19063-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="19063-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="19063-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="19063-111">**Document parts**</span></span> <br/> |<span data-ttu-id="19063-112">master#.xml</span><span class="sxs-lookup"><span data-stu-id="19063-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="19063-113">Définition</span><span class="sxs-lookup"><span data-stu-id="19063-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="19063-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="19063-114">Elements and attributes</span></span>

<span data-ttu-id="19063-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="19063-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="19063-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="19063-116">Parent elements</span></span>

<span data-ttu-id="19063-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="19063-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19063-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="19063-118">Child elements</span></span>

|<span data-ttu-id="19063-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="19063-119">**Element**</span></span>|<span data-ttu-id="19063-120">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="19063-120">**Type**</span></span>|<span data-ttu-id="19063-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="19063-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="19063-122">Connects</span><span class="sxs-lookup"><span data-stu-id="19063-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19063-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="19063-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="19063-124">Contient un **Connecter** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="19063-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="19063-125">Formes</span><span class="sxs-lookup"><span data-stu-id="19063-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19063-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="19063-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="19063-127">Contient une collection **d’éléments Shape.**</span><span class="sxs-lookup"><span data-stu-id="19063-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="19063-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="19063-128">Attributes</span></span>

<span data-ttu-id="19063-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="19063-129">None.</span></span>
  

