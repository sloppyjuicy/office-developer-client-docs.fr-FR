---
title: HeaderFooter, élément (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Contient les éléments d’en-tête et de pied de page d’un document.
ms.openlocfilehash: eabb19100c4b37a546c0a271cfba5a0c865a7e83
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384443"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="ce370-103">HeaderFooter, élément (VisioDocument_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="ce370-103">HeaderFooter element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ce370-104">Contient les éléments d’en-tête et de pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="ce370-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce370-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="ce370-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce370-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ce370-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ce370-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="ce370-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ce370-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="ce370-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ce370-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ce370-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ce370-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ce370-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ce370-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="ce370-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ce370-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="ce370-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ce370-113">Définition</span><span class="sxs-lookup"><span data-stu-id="ce370-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ce370-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ce370-114">Elements and attributes</span></span>

<span data-ttu-id="ce370-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="ce370-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ce370-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ce370-116">Parent elements</span></span>

|<span data-ttu-id="ce370-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ce370-117">**Element**</span></span>|<span data-ttu-id="ce370-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="ce370-118">**Type**</span></span>|<span data-ttu-id="ce370-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ce370-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ce370-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="ce370-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="ce370-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="ce370-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce370-122">L’élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="ce370-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ce370-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ce370-123">Child elements</span></span>

|<span data-ttu-id="ce370-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ce370-124">**Element**</span></span>|<span data-ttu-id="ce370-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="ce370-125">**Type**</span></span>|<span data-ttu-id="ce370-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="ce370-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ce370-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="ce370-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce370-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="ce370-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce370-129">Contient la chaîne de texte qui apparaît dans la partie centrale du pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="ce370-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="ce370-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="ce370-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce370-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="ce370-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce370-132">Contient la chaîne de texte qui apparaît dans la partie gauche du pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="ce370-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="ce370-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="ce370-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce370-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="ce370-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce370-135">Indique la marge du pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="ce370-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="ce370-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="ce370-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce370-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="ce370-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce370-138">Contient la chaîne de texte qui apparaît dans la partie droite du pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="ce370-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="ce370-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="ce370-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce370-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="ce370-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce370-141">Contient la chaîne de texte qui apparaît dans la partie centrale de l’en-tête d’un document.</span><span class="sxs-lookup"><span data-stu-id="ce370-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="ce370-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="ce370-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce370-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="ce370-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce370-144">Spécifie la police utilisée pour le texte d’en-tête et pied de page.</span><span class="sxs-lookup"><span data-stu-id="ce370-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="ce370-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="ce370-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce370-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="ce370-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce370-147">Contient la chaîne de texte qui apparaît dans la partie gauche de l’en-tête d’un document.</span><span class="sxs-lookup"><span data-stu-id="ce370-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="ce370-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="ce370-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce370-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="ce370-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce370-150">Indique la marge de l’en-tête d’un document.</span><span class="sxs-lookup"><span data-stu-id="ce370-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="ce370-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="ce370-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce370-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="ce370-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce370-153">Contient la chaîne de texte qui apparaît dans la partie droite de l’en-tête d’un document.</span><span class="sxs-lookup"><span data-stu-id="ce370-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ce370-154">Attributs</span><span class="sxs-lookup"><span data-stu-id="ce370-154">Attributes</span></span>

|<span data-ttu-id="ce370-155">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ce370-155">**Attribute**</span></span>|<span data-ttu-id="ce370-156">**Type**</span><span class="sxs-lookup"><span data-stu-id="ce370-156">**Type**</span></span>|<span data-ttu-id="ce370-157">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ce370-157">**Required**</span></span>|<span data-ttu-id="ce370-158">**Description**</span><span class="sxs-lookup"><span data-stu-id="ce370-158">**Description**</span></span>|<span data-ttu-id="ce370-159">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ce370-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ce370-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="ce370-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="ce370-161">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ce370-161">xsd:string</span></span>  <br/> |<span data-ttu-id="ce370-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="ce370-162">optional</span></span>  <br/> |<span data-ttu-id="ce370-163">La valeur RVB de la couleur du texte de l’en-tête et le pied de page au format hexadécimal ; par exemple, #rrggbb.</span><span class="sxs-lookup"><span data-stu-id="ce370-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="ce370-164">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ce370-164">Values of the xsd:string type.</span></span>  <br/> |
   

