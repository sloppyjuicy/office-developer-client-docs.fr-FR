---
title: Élément ProtectShapes (DocumentSettings_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e3835fc6-0ae6-b8c3-b1d0-bf893d4a9470
description: Spécifie si l’utilisateur est empêché de sélection de formes qui ont leur élément LockSelect la valeur 1.
ms.openlocfilehash: 98bb9c565f0dccc2add4a03e3dd6cd82a52015c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789370"
---
# <a name="protectshapes-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="f0a9d-103">Élément ProtectShapes (DocumentSettings_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="f0a9d-103">ProtectShapes element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f0a9d-104">Spécifie si l’utilisateur est empêché de sélection de formes qui ont leur élément **LockSelect** la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="f0a9d-104">Specifies whether the user is prevented from selecting shapes that have their **LockSelect** element set to 1.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f0a9d-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="f0a9d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0a9d-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="f0a9d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f0a9d-107">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="f0a9d-107">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f0a9d-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="f0a9d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f0a9d-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f0a9d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f0a9d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f0a9d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f0a9d-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="f0a9d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f0a9d-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="f0a9d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f0a9d-113">Définition</span><span class="sxs-lookup"><span data-stu-id="f0a9d-113">Definition</span></span>

```XML
< xs:element name="ProtectShapes" type="ProtectShapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f0a9d-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f0a9d-114">Elements and attributes</span></span>

<span data-ttu-id="f0a9d-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="f0a9d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f0a9d-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f0a9d-116">Parent elements</span></span>

|<span data-ttu-id="f0a9d-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f0a9d-117">**Element**</span></span>|<span data-ttu-id="f0a9d-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="f0a9d-118">**Type**</span></span>|<span data-ttu-id="f0a9d-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="f0a9d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f0a9d-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="f0a9d-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f0a9d-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="f0a9d-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f0a9d-122">Contient des éléments qui spécifient les paramètres de document.</span><span class="sxs-lookup"><span data-stu-id="f0a9d-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f0a9d-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f0a9d-123">Child elements</span></span>

<span data-ttu-id="f0a9d-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f0a9d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0a9d-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="f0a9d-125">Attributes</span></span>

<span data-ttu-id="f0a9d-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f0a9d-126">None.</span></span>
  

