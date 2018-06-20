---
title: DocumentSheet, élément (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Spécifie une structure DocumentSheet.
ms.openlocfilehash: 50332759ff3bbe94887371d48c4a2e729243fb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788521"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="4efdd-103">DocumentSheet, élément (VisioDocument_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="4efdd-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4efdd-104">Spécifie une structure DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="4efdd-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4efdd-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="4efdd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4efdd-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="4efdd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4efdd-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="4efdd-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4efdd-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="4efdd-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4efdd-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4efdd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4efdd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4efdd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4efdd-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="4efdd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4efdd-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="4efdd-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4efdd-113">Définition</span><span class="sxs-lookup"><span data-stu-id="4efdd-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4efdd-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4efdd-114">Elements and attributes</span></span>

<span data-ttu-id="4efdd-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="4efdd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4efdd-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4efdd-116">Parent elements</span></span>

|<span data-ttu-id="4efdd-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4efdd-117">**Element**</span></span>|<span data-ttu-id="4efdd-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="4efdd-118">**Type**</span></span>|<span data-ttu-id="4efdd-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="4efdd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4efdd-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="4efdd-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="4efdd-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="4efdd-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4efdd-122">L’élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="4efdd-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4efdd-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4efdd-123">Child elements</span></span>

|<span data-ttu-id="4efdd-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4efdd-124">**Element**</span></span>|<span data-ttu-id="4efdd-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="4efdd-125">**Type**</span></span>|<span data-ttu-id="4efdd-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="4efdd-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4efdd-127">Cell</span><span class="sxs-lookup"><span data-stu-id="4efdd-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="4efdd-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4efdd-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4efdd-129">Spécifie une cellule dans un DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="4efdd-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4efdd-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="4efdd-130">Attributes</span></span>

|<span data-ttu-id="4efdd-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4efdd-131">**Attribute**</span></span>|<span data-ttu-id="4efdd-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="4efdd-132">**Type**</span></span>|<span data-ttu-id="4efdd-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4efdd-133">**Required**</span></span>|<span data-ttu-id="4efdd-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="4efdd-134">**Description**</span></span>|<span data-ttu-id="4efdd-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4efdd-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4efdd-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="4efdd-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="4efdd-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="4efdd-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4efdd-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="4efdd-138">optional</span></span>  <br/> |<span data-ttu-id="4efdd-139">Indique si le nom a été personnalisé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4efdd-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="4efdd-140">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="4efdd-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="4efdd-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="4efdd-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="4efdd-142">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="4efdd-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4efdd-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="4efdd-143">optional</span></span>  <br/> |<span data-ttu-id="4efdd-144">Indique si le nom universel a été personnalisé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4efdd-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="4efdd-145">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="4efdd-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="4efdd-146">Nom</span><span class="sxs-lookup"><span data-stu-id="4efdd-146">Name</span></span>  <br/> |<span data-ttu-id="4efdd-147">XSD : String</span><span class="sxs-lookup"><span data-stu-id="4efdd-147">xsd:string</span></span>  <br/> |<span data-ttu-id="4efdd-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="4efdd-148">optional</span></span>  <br/> |<span data-ttu-id="4efdd-149">Spécifie le nom dépendant de la langue de la propriété DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="4efdd-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="4efdd-150">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="4efdd-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4efdd-151">NameU</span><span class="sxs-lookup"><span data-stu-id="4efdd-151">NameU</span></span>  <br/> |<span data-ttu-id="4efdd-152">XSD : String</span><span class="sxs-lookup"><span data-stu-id="4efdd-152">xsd:string</span></span>  <br/> |<span data-ttu-id="4efdd-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="4efdd-153">optional</span></span>  <br/> |<span data-ttu-id="4efdd-154">Spécifie le nom indépendant du langage de la propriété DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="4efdd-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="4efdd-155">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="4efdd-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4efdd-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="4efdd-156">UniqueID</span></span>  <br/> |<span data-ttu-id="4efdd-157">XSD : String</span><span class="sxs-lookup"><span data-stu-id="4efdd-157">xsd:string</span></span>  <br/> |<span data-ttu-id="4efdd-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="4efdd-158">optional</span></span>  <br/> |<span data-ttu-id="4efdd-159">Valeur string facultative.</span><span class="sxs-lookup"><span data-stu-id="4efdd-159">Optional string.</span></span> <span data-ttu-id="4efdd-160">Un GUID (identificateur global unique) qui identifie la forme.</span><span class="sxs-lookup"><span data-stu-id="4efdd-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="4efdd-161">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="4efdd-161">Values of the xsd:string type.</span></span>  <br/> |
   

