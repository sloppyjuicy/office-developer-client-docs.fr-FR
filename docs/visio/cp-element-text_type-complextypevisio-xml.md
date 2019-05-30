---
title: CP, élément (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marque le début d’une exécution de propriétés de caractère qui est mise en forme en fonction de l’élément char correspondant. L’exécution est définie à la fin du texte ou jusqu’à la balise suivante.
ms.openlocfilehash: 70f7d3f8333ff0f2c109862455fbd8cc3b340bf4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540559"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="a3507-104">CP, élément (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a3507-104">cp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a3507-105">Marque le début d’une exécution de propriétés de caractère qui est mise en forme en fonction de l’élément char correspondant.</span><span class="sxs-lookup"><span data-stu-id="a3507-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="a3507-106">L’exécution est définie à la fin du texte ou jusqu’à la balise suivante.</span><span class="sxs-lookup"><span data-stu-id="a3507-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3507-107">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="a3507-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3507-108">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="a3507-108">**Element type**</span></span> <br/> |[<span data-ttu-id="a3507-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="a3507-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a3507-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a3507-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a3507-111">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a3507-111">**Schema file**</span></span> <br/> |<span data-ttu-id="a3507-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a3507-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a3507-113">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="a3507-113">**Document parts**</span></span> <br/> |<span data-ttu-id="a3507-114">page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="a3507-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a3507-115">Définition</span><span class="sxs-lookup"><span data-stu-id="a3507-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a3507-116">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a3507-116">Elements and attributes</span></span>

<span data-ttu-id="a3507-117">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="a3507-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a3507-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a3507-118">Parent elements</span></span>

|<span data-ttu-id="a3507-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a3507-119">**Element**</span></span>|<span data-ttu-id="a3507-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="a3507-120">**Type**</span></span>|<span data-ttu-id="a3507-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="a3507-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a3507-122">Text</span><span class="sxs-lookup"><span data-stu-id="a3507-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3507-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="a3507-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a3507-124">Contient le texte d’une forme.</span><span class="sxs-lookup"><span data-stu-id="a3507-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a3507-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a3507-125">Child elements</span></span>

<span data-ttu-id="a3507-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a3507-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3507-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="a3507-127">Attributes</span></span>

|<span data-ttu-id="a3507-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a3507-128">**Attribute**</span></span>|<span data-ttu-id="a3507-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="a3507-129">**Type**</span></span>|<span data-ttu-id="a3507-130">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a3507-130">**Required**</span></span>|<span data-ttu-id="a3507-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="a3507-131">**Description**</span></span>|<span data-ttu-id="a3507-132">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a3507-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a3507-133">IX</span><span class="sxs-lookup"><span data-stu-id="a3507-133">IX</span></span>  <br/> |<span data-ttu-id="a3507-134">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a3507-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a3507-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a3507-135">required</span></span>  <br/> |<span data-ttu-id="a3507-136">Index de l’élément char représenté par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="a3507-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="a3507-137">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a3507-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

