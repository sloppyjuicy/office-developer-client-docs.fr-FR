---
title: StyleSheets, élément (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da26de4b-3e5b-326b-de46-e8c542b74f02
description: Contient une collection d’éléments de feuille de style pour le document.
ms.openlocfilehash: fdecd1ee6a22b4ffb918ff39f3806cf18c56654b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789838"
---
# <a name="stylesheets-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="9c408-103">StyleSheets, élément (VisioDocument_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="9c408-103">StyleSheets element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9c408-104">Contient une collection d’éléments de feuille de style pour le document.</span><span class="sxs-lookup"><span data-stu-id="9c408-104">Contains a collection of StyleSheet elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c408-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="9c408-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c408-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="9c408-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9c408-107">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="9c408-107">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9c408-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="9c408-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9c408-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9c408-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9c408-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9c408-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9c408-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="9c408-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9c408-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="9c408-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9c408-113">Définition</span><span class="sxs-lookup"><span data-stu-id="9c408-113">Definition</span></span>

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9c408-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9c408-114">Elements and attributes</span></span>

<span data-ttu-id="9c408-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="9c408-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9c408-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9c408-116">Parent elements</span></span>

|<span data-ttu-id="9c408-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9c408-117">**Element**</span></span>|<span data-ttu-id="9c408-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="9c408-118">**Type**</span></span>|<span data-ttu-id="9c408-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="9c408-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9c408-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="9c408-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="9c408-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="9c408-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9c408-122">L’élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="9c408-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9c408-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9c408-123">Child elements</span></span>

|<span data-ttu-id="9c408-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9c408-124">**Element**</span></span>|<span data-ttu-id="9c408-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="9c408-125">**Type**</span></span>|<span data-ttu-id="9c408-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="9c408-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9c408-127">Feuille de style</span><span class="sxs-lookup"><span data-stu-id="9c408-127">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c408-128">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9c408-128">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9c408-129">Représente un style défini dans un document.</span><span class="sxs-lookup"><span data-stu-id="9c408-129">Represents a style defined in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9c408-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="9c408-130">Attributes</span></span>

<span data-ttu-id="9c408-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9c408-131">None.</span></span>
  

