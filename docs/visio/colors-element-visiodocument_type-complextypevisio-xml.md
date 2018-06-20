---
title: Élément de couleurs (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Contient la table des couleurs du document.
ms.openlocfilehash: d13690ce6e1772ab1a43e697e8b99c0776a204b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788275"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="29e27-103">Élément de couleurs (VisioDocument_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="29e27-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="29e27-104">Contient la table des couleurs du document.</span><span class="sxs-lookup"><span data-stu-id="29e27-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29e27-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="29e27-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29e27-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="29e27-106">**Element type**</span></span> <br/> |[<span data-ttu-id="29e27-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="29e27-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="29e27-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="29e27-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="29e27-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="29e27-109">**Schema file**</span></span> <br/> |<span data-ttu-id="29e27-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="29e27-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="29e27-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="29e27-111">**Document parts**</span></span> <br/> |<span data-ttu-id="29e27-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="29e27-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="29e27-113">Définition</span><span class="sxs-lookup"><span data-stu-id="29e27-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="29e27-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="29e27-114">Elements and attributes</span></span>

<span data-ttu-id="29e27-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="29e27-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="29e27-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="29e27-116">Parent elements</span></span>

|<span data-ttu-id="29e27-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="29e27-117">**Element**</span></span>|<span data-ttu-id="29e27-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="29e27-118">**Type**</span></span>|<span data-ttu-id="29e27-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="29e27-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="29e27-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="29e27-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="29e27-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="29e27-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="29e27-122">L’élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="29e27-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="29e27-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="29e27-123">Child elements</span></span>

|<span data-ttu-id="29e27-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="29e27-124">**Element**</span></span>|<span data-ttu-id="29e27-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="29e27-125">**Type**</span></span>|<span data-ttu-id="29e27-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="29e27-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="29e27-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="29e27-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="29e27-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="29e27-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="29e27-129">Contient une entrée de table de couleur.</span><span class="sxs-lookup"><span data-stu-id="29e27-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="29e27-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="29e27-130">Attributes</span></span>

<span data-ttu-id="29e27-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="29e27-131">None.</span></span>
  

