---
title: Élément de Windows (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Contient les éléments de la fenêtre d’un document.
ms.openlocfilehash: df4d4bc48db157bd05fd39177975c9dbeaa5de52
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386802"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="56422-103">Élément de Windows (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="56422-103">Windows element ('Visio XML')</span></span>

<span data-ttu-id="56422-104">Contient les éléments de la **fenêtre** d’un document.</span><span class="sxs-lookup"><span data-stu-id="56422-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="56422-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="56422-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56422-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="56422-106">**Element type**</span></span> <br/> |[<span data-ttu-id="56422-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="56422-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="56422-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="56422-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="56422-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="56422-109">**Schema file**</span></span> <br/> |<span data-ttu-id="56422-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="56422-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="56422-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="56422-111">**Document parts**</span></span> <br/> |<span data-ttu-id="56422-112">Windows.Xml</span><span class="sxs-lookup"><span data-stu-id="56422-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="56422-113">Définition</span><span class="sxs-lookup"><span data-stu-id="56422-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="56422-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="56422-114">Elements and attributes</span></span>

<span data-ttu-id="56422-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="56422-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="56422-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="56422-116">Parent elements</span></span>

<span data-ttu-id="56422-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="56422-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="56422-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="56422-118">Child elements</span></span>

|<span data-ttu-id="56422-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="56422-119">**Element**</span></span>|<span data-ttu-id="56422-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="56422-120">**Type**</span></span>|<span data-ttu-id="56422-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="56422-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="56422-122">Window</span><span class="sxs-lookup"><span data-stu-id="56422-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="56422-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="56422-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="56422-124">Représente une fenêtre ouverte dans une instance de Microsoft Visio.
</span><span class="sxs-lookup"><span data-stu-id="56422-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="56422-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="56422-125">Attributes</span></span>

|<span data-ttu-id="56422-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="56422-126">**Attribute**</span></span>|<span data-ttu-id="56422-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="56422-127">**Type**</span></span>|<span data-ttu-id="56422-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="56422-128">**Required**</span></span>|<span data-ttu-id="56422-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="56422-129">**Description**</span></span>|<span data-ttu-id="56422-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="56422-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="56422-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="56422-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="56422-132">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="56422-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="56422-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="56422-133">optional</span></span>  <br/> |<span data-ttu-id="56422-134">Représente la hauteur d’une zone d’affichage</span><span class="sxs-lookup"><span data-stu-id="56422-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="56422-135">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="56422-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="56422-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="56422-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="56422-137">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="56422-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="56422-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="56422-138">optional</span></span>  <br/> |<span data-ttu-id="56422-139">Représente la largeur d’une zone d’affichage</span><span class="sxs-lookup"><span data-stu-id="56422-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="56422-140">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="56422-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

