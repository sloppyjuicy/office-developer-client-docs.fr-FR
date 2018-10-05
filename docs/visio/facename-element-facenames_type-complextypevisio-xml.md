---
title: Nom de la police, élément (FaceNames_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contient des informations sur une police.
ms.openlocfilehash: 4c8f047d655be167dc058b3e29ac62161887ce99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389777"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a><span data-ttu-id="664d8-103">Nom de la police, élément (FaceNames_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="664d8-103">FaceName element (FaceNames_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="664d8-104">Contient des informations sur une police.</span><span class="sxs-lookup"><span data-stu-id="664d8-104">Contains information about a font.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="664d8-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="664d8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="664d8-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="664d8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="664d8-107">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="664d8-107">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="664d8-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="664d8-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="664d8-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="664d8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="664d8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="664d8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="664d8-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="664d8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="664d8-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="664d8-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="664d8-113">Définition</span><span class="sxs-lookup"><span data-stu-id="664d8-113">Definition</span></span>

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="664d8-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="664d8-114">Elements and attributes</span></span>

<span data-ttu-id="664d8-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="664d8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="664d8-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="664d8-116">Parent elements</span></span>

|<span data-ttu-id="664d8-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="664d8-117">**Element**</span></span>|<span data-ttu-id="664d8-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="664d8-118">**Type**</span></span>|<span data-ttu-id="664d8-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="664d8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="664d8-120">FaceNames</span><span class="sxs-lookup"><span data-stu-id="664d8-120">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="664d8-121">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="664d8-121">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="664d8-122">Contient une collection d’éléments de **nom de la police** .</span><span class="sxs-lookup"><span data-stu-id="664d8-122">Contains a collection of **FaceName** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="664d8-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="664d8-123">Child elements</span></span>

<span data-ttu-id="664d8-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="664d8-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="664d8-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="664d8-125">Attributes</span></span>

|<span data-ttu-id="664d8-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="664d8-126">**Attribute**</span></span>|<span data-ttu-id="664d8-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="664d8-127">**Type**</span></span>|<span data-ttu-id="664d8-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="664d8-128">**Required**</span></span>|<span data-ttu-id="664d8-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="664d8-129">**Description**</span></span>|<span data-ttu-id="664d8-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="664d8-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="664d8-131">Jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="664d8-131">CharSets</span></span>  <br/> |<span data-ttu-id="664d8-132">XSD : String</span><span class="sxs-lookup"><span data-stu-id="664d8-132">xsd:string</span></span>  <br/> |<span data-ttu-id="664d8-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="664d8-133">optional</span></span>  <br/> |<span data-ttu-id="664d8-134">Les jeux de caractères pris en charge de la police.</span><span class="sxs-lookup"><span data-stu-id="664d8-134">The supported character sets of the font.</span></span>  <br/> |<span data-ttu-id="664d8-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="664d8-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="664d8-136">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="664d8-136">Flags</span></span>  <br/> |<span data-ttu-id="664d8-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="664d8-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="664d8-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="664d8-138">optional</span></span>  <br/> |<span data-ttu-id="664d8-139">Indicateurs qui influencent les éléments suivants : manque de police, la police par défaut, police de caractères asiatiques, police complexe, police verticale et type de police.</span><span class="sxs-lookup"><span data-stu-id="664d8-139">Flags that indicate the following: missing font, default font, asian font, complex font, vertical font, and font type.</span></span>  <br/> |<span data-ttu-id="664d8-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="664d8-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="664d8-141">NameU</span><span class="sxs-lookup"><span data-stu-id="664d8-141">NameU</span></span>  <br/> |<span data-ttu-id="664d8-142">XSD : String</span><span class="sxs-lookup"><span data-stu-id="664d8-142">xsd:string</span></span>  <br/> |<span data-ttu-id="664d8-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="664d8-143">required</span></span>  <br/> |<span data-ttu-id="664d8-144">Le nom de la police sous forme de chaîne Unicode UTF-16.</span><span class="sxs-lookup"><span data-stu-id="664d8-144">The name of the font as a UTF-16 Unicode string.</span></span>  <br/> ||
|<span data-ttu-id="664d8-145">Panos</span><span class="sxs-lookup"><span data-stu-id="664d8-145">Panos</span></span>  <br/> |<span data-ttu-id="664d8-146">XSD : String</span><span class="sxs-lookup"><span data-stu-id="664d8-146">xsd:string</span></span>  <br/> |<span data-ttu-id="664d8-147">facultatif</span><span class="sxs-lookup"><span data-stu-id="664d8-147">optional</span></span>  <br/> |<span data-ttu-id="664d8-148">La signature panose la police.</span><span class="sxs-lookup"><span data-stu-id="664d8-148">The panose signature for the font.</span></span> <span data-ttu-id="664d8-149">Panose est un système de classification de polices qui les classe en fonction de leurs caractéristiques visuelles.</span><span class="sxs-lookup"><span data-stu-id="664d8-149">Panose is a classification system for typefaces that categorizes them based upon their visual characteristics.</span></span>  <br/> |<span data-ttu-id="664d8-150">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="664d8-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="664d8-151">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="664d8-151">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="664d8-152">XSD : String</span><span class="sxs-lookup"><span data-stu-id="664d8-152">xsd:string</span></span>  <br/> |<span data-ttu-id="664d8-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="664d8-153">optional</span></span>  <br/> |<span data-ttu-id="664d8-154">Les plages Unicode pris en charge de la police.</span><span class="sxs-lookup"><span data-stu-id="664d8-154">The supported Unicode ranges of the font.</span></span>  <br/> |<span data-ttu-id="664d8-155">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="664d8-155">Values of the xsd:string type.</span></span>  <br/> |
   

