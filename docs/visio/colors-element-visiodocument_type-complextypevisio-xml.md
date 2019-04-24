---
title: Colors, élément (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Contient la table des couleurs du document.
ms.openlocfilehash: bd46f58dfbb8a596717662b9a0524d59bb508270
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358757"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="3e380-103">Colors, élément (VisioDocument_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="3e380-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3e380-104">Contient la table des couleurs du document.</span><span class="sxs-lookup"><span data-stu-id="3e380-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e380-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="3e380-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e380-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="3e380-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3e380-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="3e380-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3e380-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3e380-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3e380-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="3e380-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3e380-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="3e380-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3e380-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="3e380-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3e380-112">document. Xml</span><span class="sxs-lookup"><span data-stu-id="3e380-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3e380-113">Définition</span><span class="sxs-lookup"><span data-stu-id="3e380-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3e380-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="3e380-114">Elements and attributes</span></span>

<span data-ttu-id="3e380-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="3e380-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3e380-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3e380-116">Parent elements</span></span>

|<span data-ttu-id="3e380-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3e380-117">**Element**</span></span>|<span data-ttu-id="3e380-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="3e380-118">**Type**</span></span>|<span data-ttu-id="3e380-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="3e380-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3e380-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="3e380-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="3e380-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="3e380-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3e380-122">Élément racine d'un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="3e380-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3e380-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3e380-123">Child elements</span></span>

|<span data-ttu-id="3e380-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3e380-124">**Element**</span></span>|<span data-ttu-id="3e380-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="3e380-125">**Type**</span></span>|<span data-ttu-id="3e380-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="3e380-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3e380-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="3e380-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3e380-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="3e380-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3e380-129">Contient une entrée de table de couleurs.</span><span class="sxs-lookup"><span data-stu-id="3e380-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3e380-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="3e380-130">Attributes</span></span>

<span data-ttu-id="3e380-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3e380-131">None.</span></span>
  

