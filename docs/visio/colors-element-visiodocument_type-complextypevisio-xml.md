---
title: Élément de couleurs (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Contient la table des couleurs du document.
ms.openlocfilehash: bd46f58dfbb8a596717662b9a0524d59bb508270
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400529"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="0f4b6-103">Élément de couleurs (VisioDocument_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="0f4b6-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0f4b6-104">Contient la table des couleurs du document.</span><span class="sxs-lookup"><span data-stu-id="0f4b6-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f4b6-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="0f4b6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f4b6-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="0f4b6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0f4b6-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="0f4b6-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0f4b6-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="0f4b6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0f4b6-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0f4b6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0f4b6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0f4b6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0f4b6-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="0f4b6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0f4b6-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="0f4b6-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0f4b6-113">Définition</span><span class="sxs-lookup"><span data-stu-id="0f4b6-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0f4b6-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0f4b6-114">Elements and attributes</span></span>

<span data-ttu-id="0f4b6-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="0f4b6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0f4b6-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0f4b6-116">Parent elements</span></span>

|<span data-ttu-id="0f4b6-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0f4b6-117">**Element**</span></span>|<span data-ttu-id="0f4b6-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="0f4b6-118">**Type**</span></span>|<span data-ttu-id="0f4b6-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="0f4b6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f4b6-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="0f4b6-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="0f4b6-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="0f4b6-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0f4b6-122">L’élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="0f4b6-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0f4b6-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f4b6-123">Child elements</span></span>

|<span data-ttu-id="0f4b6-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0f4b6-124">**Element**</span></span>|<span data-ttu-id="0f4b6-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="0f4b6-125">**Type**</span></span>|<span data-ttu-id="0f4b6-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="0f4b6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f4b6-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="0f4b6-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f4b6-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="0f4b6-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0f4b6-129">Contient une entrée de table de couleur.</span><span class="sxs-lookup"><span data-stu-id="0f4b6-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0f4b6-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="0f4b6-130">Attributes</span></span>

<span data-ttu-id="0f4b6-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0f4b6-131">None.</span></span>
  

