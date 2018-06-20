---
title: Élément FaceNames (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Contient une collection d’éléments de nom de la police.
ms.openlocfilehash: 1c031d589883f34bbf9d69a3d537b82e1ecf3129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788607"
---
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="8cd43-103">Élément FaceNames (VisioDocument_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="8cd43-103">FaceNames element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8cd43-104">Contient une collection d’éléments de **nom de la police** .</span><span class="sxs-lookup"><span data-stu-id="8cd43-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8cd43-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="8cd43-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8cd43-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="8cd43-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8cd43-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="8cd43-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8cd43-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="8cd43-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8cd43-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="8cd43-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8cd43-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8cd43-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8cd43-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="8cd43-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8cd43-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="8cd43-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8cd43-113">Définition</span><span class="sxs-lookup"><span data-stu-id="8cd43-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8cd43-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="8cd43-114">Elements and attributes</span></span>

<span data-ttu-id="8cd43-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="8cd43-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8cd43-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8cd43-116">Parent elements</span></span>

|<span data-ttu-id="8cd43-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8cd43-117">**Element**</span></span>|<span data-ttu-id="8cd43-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="8cd43-118">**Type**</span></span>|<span data-ttu-id="8cd43-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="8cd43-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8cd43-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="8cd43-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="8cd43-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="8cd43-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8cd43-122">L’élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="8cd43-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8cd43-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8cd43-123">Child elements</span></span>

|<span data-ttu-id="8cd43-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8cd43-124">**Element**</span></span>|<span data-ttu-id="8cd43-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="8cd43-125">**Type**</span></span>|<span data-ttu-id="8cd43-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="8cd43-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8cd43-127">Nom de la police</span><span class="sxs-lookup"><span data-stu-id="8cd43-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8cd43-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="8cd43-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8cd43-129">Contient des informations sur une police.</span><span class="sxs-lookup"><span data-stu-id="8cd43-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8cd43-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="8cd43-130">Attributes</span></span>

<span data-ttu-id="8cd43-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8cd43-131">None.</span></span>
  

