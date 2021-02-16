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
# <a name="facenames-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="88ed4-103">Élément FaceNames (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="88ed4-103">FaceNames element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="88ed4-104">Contient une collection **d’éléments FaceName.**</span><span class="sxs-lookup"><span data-stu-id="88ed4-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="88ed4-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="88ed4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88ed4-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="88ed4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="88ed4-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="88ed4-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="88ed4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="88ed4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="88ed4-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="88ed4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="88ed4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="88ed4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="88ed4-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="88ed4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="88ed4-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="88ed4-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88ed4-113">Définition</span><span class="sxs-lookup"><span data-stu-id="88ed4-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="88ed4-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="88ed4-114">Elements and attributes</span></span>

<span data-ttu-id="88ed4-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="88ed4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="88ed4-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="88ed4-116">Parent elements</span></span>

|<span data-ttu-id="88ed4-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="88ed4-117">**Element**</span></span>|<span data-ttu-id="88ed4-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="88ed4-118">**Type**</span></span>|<span data-ttu-id="88ed4-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="88ed4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88ed4-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="88ed4-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="88ed4-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="88ed4-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="88ed4-122">Élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="88ed4-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="88ed4-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="88ed4-123">Child elements</span></span>

|<span data-ttu-id="88ed4-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="88ed4-124">**Element**</span></span>|<span data-ttu-id="88ed4-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="88ed4-125">**Type**</span></span>|<span data-ttu-id="88ed4-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="88ed4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88ed4-127">FaceName</span><span class="sxs-lookup"><span data-stu-id="88ed4-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="88ed4-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="88ed4-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="88ed4-129">Contient des informations sur une police.</span><span class="sxs-lookup"><span data-stu-id="88ed4-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="88ed4-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="88ed4-130">Attributes</span></span>

<span data-ttu-id="88ed4-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="88ed4-131">None.</span></span>
  

