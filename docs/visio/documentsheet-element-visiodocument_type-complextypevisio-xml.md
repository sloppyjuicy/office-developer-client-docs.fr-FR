---
title: Élément DocumentSheet (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Spécifie une structure de feuille de document.
ms.openlocfilehash: 279fca457163d5bcbdda885c11c589bfcde0baa9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540041"
---
# <a name="documentsheet-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="27ae2-103">Élément DocumentSheet (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="27ae2-103">DocumentSheet element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="27ae2-104">Spécifie une structure de feuille de document.</span><span class="sxs-lookup"><span data-stu-id="27ae2-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27ae2-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="27ae2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27ae2-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="27ae2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="27ae2-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="27ae2-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="27ae2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="27ae2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="27ae2-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="27ae2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="27ae2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="27ae2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="27ae2-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="27ae2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="27ae2-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="27ae2-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="27ae2-113">Définition</span><span class="sxs-lookup"><span data-stu-id="27ae2-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="27ae2-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="27ae2-114">Elements and attributes</span></span>

<span data-ttu-id="27ae2-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="27ae2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="27ae2-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="27ae2-116">Parent elements</span></span>

|<span data-ttu-id="27ae2-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="27ae2-117">**Element**</span></span>|<span data-ttu-id="27ae2-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="27ae2-118">**Type**</span></span>|<span data-ttu-id="27ae2-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="27ae2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="27ae2-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="27ae2-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="27ae2-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="27ae2-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="27ae2-122">Élément racine d’un document Microsoft Visio document.</span><span class="sxs-lookup"><span data-stu-id="27ae2-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="27ae2-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="27ae2-123">Child elements</span></span>

|<span data-ttu-id="27ae2-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="27ae2-124">**Element**</span></span>|<span data-ttu-id="27ae2-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="27ae2-125">**Type**</span></span>|<span data-ttu-id="27ae2-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="27ae2-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="27ae2-127">Cell</span><span class="sxs-lookup"><span data-stu-id="27ae2-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="27ae2-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="27ae2-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="27ae2-129">Spécifie une cellule dans une feuille de document.</span><span class="sxs-lookup"><span data-stu-id="27ae2-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="27ae2-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="27ae2-130">Attributes</span></span>

|<span data-ttu-id="27ae2-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="27ae2-131">**Attribute**</span></span>|<span data-ttu-id="27ae2-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="27ae2-132">**Type**</span></span>|<span data-ttu-id="27ae2-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="27ae2-133">**Required**</span></span>|<span data-ttu-id="27ae2-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="27ae2-134">**Description**</span></span>|<span data-ttu-id="27ae2-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="27ae2-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="27ae2-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="27ae2-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="27ae2-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="27ae2-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="27ae2-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="27ae2-138">optional</span></span>  <br/> |<span data-ttu-id="27ae2-139">Indique si le nom a été personnalisé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="27ae2-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="27ae2-140">Valeurs du type xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="27ae2-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="27ae2-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="27ae2-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="27ae2-142">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="27ae2-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="27ae2-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="27ae2-143">optional</span></span>  <br/> |<span data-ttu-id="27ae2-144">Indique si le nom universel a été personnalisé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="27ae2-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="27ae2-145">Valeurs du type xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="27ae2-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="27ae2-146">Nom</span><span class="sxs-lookup"><span data-stu-id="27ae2-146">Name</span></span>  <br/> |<span data-ttu-id="27ae2-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="27ae2-147">xsd:string</span></span>  <br/> |<span data-ttu-id="27ae2-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="27ae2-148">optional</span></span>  <br/> |<span data-ttu-id="27ae2-149">Spécifie le nom dépendant de la langue de la feuille de document.</span><span class="sxs-lookup"><span data-stu-id="27ae2-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="27ae2-150">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="27ae2-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="27ae2-151">NameU</span><span class="sxs-lookup"><span data-stu-id="27ae2-151">NameU</span></span>  <br/> |<span data-ttu-id="27ae2-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="27ae2-152">xsd:string</span></span>  <br/> |<span data-ttu-id="27ae2-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="27ae2-153">optional</span></span>  <br/> |<span data-ttu-id="27ae2-154">Spécifie le nom indépendant de la langue de la feuille de document.</span><span class="sxs-lookup"><span data-stu-id="27ae2-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="27ae2-155">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="27ae2-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="27ae2-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="27ae2-156">UniqueID</span></span>  <br/> |<span data-ttu-id="27ae2-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="27ae2-157">xsd:string</span></span>  <br/> |<span data-ttu-id="27ae2-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="27ae2-158">optional</span></span>  <br/> |<span data-ttu-id="27ae2-159">Chaîne facultative.</span><span class="sxs-lookup"><span data-stu-id="27ae2-159">Optional string.</span></span> <span data-ttu-id="27ae2-160">GUID (identificateur global unique) identifiant la forme.</span><span class="sxs-lookup"><span data-stu-id="27ae2-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="27ae2-161">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="27ae2-161">Values of the xsd:string type.</span></span>  <br/> |
   

