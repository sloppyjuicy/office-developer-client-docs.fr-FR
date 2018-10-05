---
title: DocumentSheet, élément (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Spécifie une structure DocumentSheet.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383463"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="47656-103">DocumentSheet, élément (VisioDocument_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="47656-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="47656-104">Spécifie une structure DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="47656-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="47656-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="47656-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47656-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="47656-106">**Element type**</span></span> <br/> |[<span data-ttu-id="47656-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="47656-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="47656-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="47656-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="47656-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="47656-109">**Schema file**</span></span> <br/> |<span data-ttu-id="47656-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="47656-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="47656-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="47656-111">**Document parts**</span></span> <br/> |<span data-ttu-id="47656-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="47656-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47656-113">Définition</span><span class="sxs-lookup"><span data-stu-id="47656-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="47656-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="47656-114">Elements and attributes</span></span>

<span data-ttu-id="47656-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="47656-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="47656-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="47656-116">Parent elements</span></span>

|<span data-ttu-id="47656-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="47656-117">**Element**</span></span>|<span data-ttu-id="47656-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="47656-118">**Type**</span></span>|<span data-ttu-id="47656-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="47656-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="47656-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="47656-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="47656-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="47656-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="47656-122">L’élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="47656-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="47656-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="47656-123">Child elements</span></span>

|<span data-ttu-id="47656-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="47656-124">**Element**</span></span>|<span data-ttu-id="47656-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="47656-125">**Type**</span></span>|<span data-ttu-id="47656-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="47656-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="47656-127">Cell</span><span class="sxs-lookup"><span data-stu-id="47656-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="47656-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="47656-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="47656-129">Spécifie une cellule dans un DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="47656-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="47656-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="47656-130">Attributes</span></span>

|<span data-ttu-id="47656-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="47656-131">**Attribute**</span></span>|<span data-ttu-id="47656-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="47656-132">**Type**</span></span>|<span data-ttu-id="47656-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="47656-133">**Required**</span></span>|<span data-ttu-id="47656-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="47656-134">**Description**</span></span>|<span data-ttu-id="47656-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="47656-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="47656-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="47656-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="47656-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="47656-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="47656-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="47656-138">optional</span></span>  <br/> |<span data-ttu-id="47656-139">Indique si le nom a été personnalisé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="47656-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="47656-140">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="47656-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="47656-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="47656-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="47656-142">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="47656-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="47656-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="47656-143">optional</span></span>  <br/> |<span data-ttu-id="47656-144">Indique si le nom universel a été personnalisé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="47656-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="47656-145">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="47656-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="47656-146">Nom</span><span class="sxs-lookup"><span data-stu-id="47656-146">Name</span></span>  <br/> |<span data-ttu-id="47656-147">XSD : String</span><span class="sxs-lookup"><span data-stu-id="47656-147">xsd:string</span></span>  <br/> |<span data-ttu-id="47656-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="47656-148">optional</span></span>  <br/> |<span data-ttu-id="47656-149">Spécifie le nom dépendant de la langue de la propriété DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="47656-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="47656-150">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="47656-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="47656-151">NameU</span><span class="sxs-lookup"><span data-stu-id="47656-151">NameU</span></span>  <br/> |<span data-ttu-id="47656-152">XSD : String</span><span class="sxs-lookup"><span data-stu-id="47656-152">xsd:string</span></span>  <br/> |<span data-ttu-id="47656-153">facultatif</span><span class="sxs-lookup"><span data-stu-id="47656-153">optional</span></span>  <br/> |<span data-ttu-id="47656-154">Spécifie le nom indépendant du langage de la propriété DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="47656-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="47656-155">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="47656-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="47656-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="47656-156">UniqueID</span></span>  <br/> |<span data-ttu-id="47656-157">XSD : String</span><span class="sxs-lookup"><span data-stu-id="47656-157">xsd:string</span></span>  <br/> |<span data-ttu-id="47656-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="47656-158">optional</span></span>  <br/> |<span data-ttu-id="47656-159">Valeur string facultative.</span><span class="sxs-lookup"><span data-stu-id="47656-159">Optional string.</span></span> <span data-ttu-id="47656-160">Un GUID (identificateur global unique) qui identifie la forme.</span><span class="sxs-lookup"><span data-stu-id="47656-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="47656-161">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="47656-161">Values of the xsd:string type.</span></span>  <br/> |
   

