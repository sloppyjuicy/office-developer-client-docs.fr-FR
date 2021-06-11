---
title: Élément FaceNames (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Contient une collection d’éléments FaceName.
ms.openlocfilehash: ce18847fdd46a0c703a0df5e8d8c7a877f864d35
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539712"
---
# <a name="facenames-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="3cab9-103">Élément FaceNames (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3cab9-103">FaceNames element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="3cab9-104">Contient une collection **d’éléments FaceName.**</span><span class="sxs-lookup"><span data-stu-id="3cab9-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3cab9-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="3cab9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3cab9-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="3cab9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3cab9-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="3cab9-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3cab9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3cab9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3cab9-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="3cab9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3cab9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3cab9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3cab9-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="3cab9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3cab9-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="3cab9-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3cab9-113">Définition</span><span class="sxs-lookup"><span data-stu-id="3cab9-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3cab9-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="3cab9-114">Elements and attributes</span></span>

<span data-ttu-id="3cab9-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="3cab9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3cab9-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3cab9-116">Parent elements</span></span>

|<span data-ttu-id="3cab9-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3cab9-117">**Element**</span></span>|<span data-ttu-id="3cab9-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="3cab9-118">**Type**</span></span>|<span data-ttu-id="3cab9-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="3cab9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3cab9-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="3cab9-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="3cab9-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="3cab9-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3cab9-122">Élément racine d’un document Microsoft Visio document.</span><span class="sxs-lookup"><span data-stu-id="3cab9-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3cab9-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3cab9-123">Child elements</span></span>

|<span data-ttu-id="3cab9-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3cab9-124">**Element**</span></span>|<span data-ttu-id="3cab9-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="3cab9-125">**Type**</span></span>|<span data-ttu-id="3cab9-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="3cab9-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3cab9-127">FaceName</span><span class="sxs-lookup"><span data-stu-id="3cab9-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3cab9-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="3cab9-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3cab9-129">Contient des informations sur une police.</span><span class="sxs-lookup"><span data-stu-id="3cab9-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3cab9-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="3cab9-130">Attributes</span></span>

<span data-ttu-id="3cab9-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3cab9-131">None.</span></span>
  

