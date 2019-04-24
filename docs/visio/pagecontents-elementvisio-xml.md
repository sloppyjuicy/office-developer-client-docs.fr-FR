---
title: Élément PageContents ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Cette énumération spécifie les informations relatives aux formes d'une forme de base ou d'une page de dessin d'un dessin.
ms.openlocfilehash: aec860f4135e15f18436dba50986b0ad0e6ee9e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334509"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="deb82-103">Élément PageContents ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="deb82-103">PageContents element ('Visio XML')</span></span>

<span data-ttu-id="deb82-104">Cette énumération spécifie les informations relatives aux formes d'une forme de base ou d'une page de dessin d'un dessin.</span><span class="sxs-lookup"><span data-stu-id="deb82-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="deb82-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="deb82-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="deb82-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="deb82-106">**Element type**</span></span> <br/> |[<span data-ttu-id="deb82-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="deb82-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="deb82-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="deb82-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="deb82-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="deb82-109">**Schema file**</span></span> <br/> |<span data-ttu-id="deb82-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="deb82-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="deb82-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="deb82-111">**Document parts**</span></span> <br/> |<span data-ttu-id="deb82-112">page #. Xml</span><span class="sxs-lookup"><span data-stu-id="deb82-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="deb82-113">Définition</span><span class="sxs-lookup"><span data-stu-id="deb82-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="deb82-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="deb82-114">Elements and attributes</span></span>

<span data-ttu-id="deb82-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="deb82-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="deb82-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="deb82-116">Parent elements</span></span>

<span data-ttu-id="deb82-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="deb82-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="deb82-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="deb82-118">Child elements</span></span>

|<span data-ttu-id="deb82-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="deb82-119">**Element**</span></span>|<span data-ttu-id="deb82-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="deb82-120">**Type**</span></span>|<span data-ttu-id="deb82-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="deb82-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="deb82-122">Connects</span><span class="sxs-lookup"><span data-stu-id="deb82-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="deb82-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="deb82-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="deb82-124">Contient un élément **Connect** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="deb82-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="deb82-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="deb82-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="deb82-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="deb82-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="deb82-127">Spécifie une collection de formes.</span><span class="sxs-lookup"><span data-stu-id="deb82-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="deb82-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="deb82-128">Attributes</span></span>

<span data-ttu-id="deb82-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="deb82-129">None.</span></span>
  

