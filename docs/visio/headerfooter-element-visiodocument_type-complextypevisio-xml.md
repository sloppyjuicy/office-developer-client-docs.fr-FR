---
title: HeaderFooter, élément (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Contient des éléments pour l’en-tête et le pied de page d’un document.
ms.openlocfilehash: c3c2f0adab4448ca88e5f2cca5605f397c48bd98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541105"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="44509-103">HeaderFooter, élément (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="44509-103">HeaderFooter element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="44509-104">Contient des éléments pour l’en-tête et le pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="44509-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44509-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="44509-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44509-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="44509-106">**Element type**</span></span> <br/> |[<span data-ttu-id="44509-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="44509-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="44509-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="44509-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="44509-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="44509-109">**Schema file**</span></span> <br/> |<span data-ttu-id="44509-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="44509-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="44509-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="44509-111">**Document parts**</span></span> <br/> |<span data-ttu-id="44509-112">document. Xml</span><span class="sxs-lookup"><span data-stu-id="44509-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="44509-113">Définition</span><span class="sxs-lookup"><span data-stu-id="44509-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="44509-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="44509-114">Elements and attributes</span></span>

<span data-ttu-id="44509-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="44509-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="44509-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="44509-116">Parent elements</span></span>

|<span data-ttu-id="44509-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="44509-117">**Element**</span></span>|<span data-ttu-id="44509-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="44509-118">**Type**</span></span>|<span data-ttu-id="44509-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="44509-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="44509-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="44509-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="44509-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="44509-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44509-122">Élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="44509-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="44509-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="44509-123">Child elements</span></span>

|<span data-ttu-id="44509-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="44509-124">**Element**</span></span>|<span data-ttu-id="44509-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="44509-125">**Type**</span></span>|<span data-ttu-id="44509-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="44509-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="44509-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="44509-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44509-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="44509-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44509-129">Contient la chaîne de texte qui apparaît dans la partie centrale du pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="44509-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="44509-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="44509-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44509-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="44509-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44509-132">Contient la chaîne de texte qui apparaît dans la partie gauche du pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="44509-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="44509-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="44509-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44509-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="44509-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44509-135">Spécifie la marge du pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="44509-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="44509-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="44509-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44509-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="44509-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44509-138">Contient la chaîne de texte qui apparaît dans la partie droite du pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="44509-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="44509-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="44509-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44509-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="44509-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44509-141">Contient la chaîne de texte qui apparaît au centre de l’en-tête d’un document.</span><span class="sxs-lookup"><span data-stu-id="44509-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="44509-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="44509-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44509-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="44509-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44509-144">Spécifie la police utilisée pour le texte de l’en-tête et du pied de page.</span><span class="sxs-lookup"><span data-stu-id="44509-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="44509-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="44509-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44509-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="44509-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44509-147">Contient la chaîne de texte qui apparaît dans la partie gauche de l’en-tête d’un document.</span><span class="sxs-lookup"><span data-stu-id="44509-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="44509-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="44509-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44509-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="44509-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44509-150">Cette énumération spécifie la marge de l’en-tête d’un document.</span><span class="sxs-lookup"><span data-stu-id="44509-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="44509-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="44509-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44509-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="44509-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44509-153">Contient la chaîne de texte qui apparaît dans la partie droite de l’en-tête d’un document.</span><span class="sxs-lookup"><span data-stu-id="44509-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="44509-154">Attributs</span><span class="sxs-lookup"><span data-stu-id="44509-154">Attributes</span></span>

|<span data-ttu-id="44509-155">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="44509-155">**Attribute**</span></span>|<span data-ttu-id="44509-156">**Type**</span><span class="sxs-lookup"><span data-stu-id="44509-156">**Type**</span></span>|<span data-ttu-id="44509-157">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="44509-157">**Required**</span></span>|<span data-ttu-id="44509-158">**Description**</span><span class="sxs-lookup"><span data-stu-id="44509-158">**Description**</span></span>|<span data-ttu-id="44509-159">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="44509-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="44509-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="44509-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="44509-161">xsd: String</span><span class="sxs-lookup"><span data-stu-id="44509-161">xsd:string</span></span>  <br/> |<span data-ttu-id="44509-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="44509-162">optional</span></span>  <br/> |<span data-ttu-id="44509-163">Valeur RVB de la couleur du texte de l’en-tête et du pied de page en notation hexadécimale; par exemple, #rrggbb.</span><span class="sxs-lookup"><span data-stu-id="44509-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="44509-164">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="44509-164">Values of the xsd:string type.</span></span>  <br/> |
   

