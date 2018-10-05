---
title: élément CP (Text_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marque le début de des propriétés de caractère exécuter qui est mis en forme en fonction de l’élément de caractère correspondant. L’exécution est définie à la fin du texte ou jusqu'à ce que la balise suivante.
ms.openlocfilehash: eb7fd30c2314e159dc3649e87cd63bd4090ba283
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388195"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="21819-104">élément CP (Text_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="21819-104">cp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="21819-105">Marque le début de des propriétés de caractère exécuter qui est mis en forme en fonction de l’élément de caractère correspondant.</span><span class="sxs-lookup"><span data-stu-id="21819-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="21819-106">L’exécution est définie à la fin du texte ou jusqu'à ce que la balise suivante.</span><span class="sxs-lookup"><span data-stu-id="21819-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21819-107">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="21819-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21819-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="21819-108">**Element type**</span></span> <br/> |[<span data-ttu-id="21819-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="21819-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="21819-110">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="21819-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="21819-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="21819-111">**Schema file**</span></span> <br/> |<span data-ttu-id="21819-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="21819-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="21819-113">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="21819-113">**Document parts**</span></span> <br/> |<span data-ttu-id="21819-114">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="21819-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="21819-115">Définition</span><span class="sxs-lookup"><span data-stu-id="21819-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="21819-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="21819-116">Elements and attributes</span></span>

<span data-ttu-id="21819-117">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="21819-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="21819-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="21819-118">Parent elements</span></span>

|<span data-ttu-id="21819-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="21819-119">**Element**</span></span>|<span data-ttu-id="21819-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="21819-120">**Type**</span></span>|<span data-ttu-id="21819-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="21819-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="21819-122">Text</span><span class="sxs-lookup"><span data-stu-id="21819-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="21819-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="21819-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="21819-124">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="21819-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="21819-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="21819-125">Child elements</span></span>

<span data-ttu-id="21819-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="21819-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21819-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="21819-127">Attributes</span></span>

|<span data-ttu-id="21819-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="21819-128">**Attribute**</span></span>|<span data-ttu-id="21819-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="21819-129">**Type**</span></span>|<span data-ttu-id="21819-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="21819-130">**Required**</span></span>|<span data-ttu-id="21819-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="21819-131">**Description**</span></span>|<span data-ttu-id="21819-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="21819-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="21819-133">IX</span><span class="sxs-lookup"><span data-stu-id="21819-133">IX</span></span>  <br/> |<span data-ttu-id="21819-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="21819-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="21819-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="21819-135">required</span></span>  <br/> |<span data-ttu-id="21819-136">Index de l’élément de caractère qui représente cette propriété à exécuter.</span><span class="sxs-lookup"><span data-stu-id="21819-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="21819-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="21819-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

