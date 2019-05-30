---
title: Colors, élément (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Contient la table des couleurs du document.
ms.openlocfilehash: 6f18926961583e09f83dd7921ca140c07a60ecc3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540174"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="54e80-103">Colors, élément (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="54e80-103">Colors element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="54e80-104">Contient la table des couleurs du document.</span><span class="sxs-lookup"><span data-stu-id="54e80-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54e80-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="54e80-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54e80-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="54e80-106">**Element type**</span></span> <br/> |[<span data-ttu-id="54e80-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="54e80-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="54e80-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="54e80-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="54e80-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="54e80-109">**Schema file**</span></span> <br/> |<span data-ttu-id="54e80-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="54e80-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="54e80-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="54e80-111">**Document parts**</span></span> <br/> |<span data-ttu-id="54e80-112">document. Xml</span><span class="sxs-lookup"><span data-stu-id="54e80-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="54e80-113">Définition</span><span class="sxs-lookup"><span data-stu-id="54e80-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="54e80-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="54e80-114">Elements and attributes</span></span>

<span data-ttu-id="54e80-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="54e80-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="54e80-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="54e80-116">Parent elements</span></span>

|<span data-ttu-id="54e80-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="54e80-117">**Element**</span></span>|<span data-ttu-id="54e80-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="54e80-118">**Type**</span></span>|<span data-ttu-id="54e80-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="54e80-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="54e80-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="54e80-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="54e80-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="54e80-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="54e80-122">Élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="54e80-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="54e80-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="54e80-123">Child elements</span></span>

|<span data-ttu-id="54e80-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="54e80-124">**Element**</span></span>|<span data-ttu-id="54e80-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="54e80-125">**Type**</span></span>|<span data-ttu-id="54e80-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="54e80-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="54e80-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="54e80-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="54e80-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="54e80-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="54e80-129">Contient une entrée de table de couleurs.</span><span class="sxs-lookup"><span data-stu-id="54e80-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="54e80-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="54e80-130">Attributes</span></span>

<span data-ttu-id="54e80-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="54e80-131">None.</span></span>
  

