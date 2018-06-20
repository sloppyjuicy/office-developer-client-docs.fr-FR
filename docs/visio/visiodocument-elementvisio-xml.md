---
title: Élément VisioDocument (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: L’élément racine d’un document Microsoft Visio.
ms.openlocfilehash: 5a325b78ec64708246f0c8a6f5396c2ce1569121
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790033"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="4200d-103">Élément VisioDocument (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="4200d-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="4200d-104">L’élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="4200d-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4200d-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="4200d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4200d-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="4200d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4200d-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="4200d-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4200d-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="4200d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4200d-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4200d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4200d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4200d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4200d-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="4200d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4200d-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="4200d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4200d-113">Définition</span><span class="sxs-lookup"><span data-stu-id="4200d-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4200d-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4200d-114">Elements and attributes</span></span>

<span data-ttu-id="4200d-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="4200d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4200d-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4200d-116">Parent elements</span></span>

<span data-ttu-id="4200d-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4200d-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4200d-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4200d-118">Child elements</span></span>

|<span data-ttu-id="4200d-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4200d-119">**Element**</span></span>|<span data-ttu-id="4200d-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="4200d-120">**Type**</span></span>|<span data-ttu-id="4200d-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="4200d-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4200d-122">Couleurs</span><span class="sxs-lookup"><span data-stu-id="4200d-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4200d-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="4200d-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4200d-124">Contient la table des couleurs du document.</span><span class="sxs-lookup"><span data-stu-id="4200d-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="4200d-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="4200d-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4200d-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="4200d-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4200d-127">Contient des éléments qui spécifient les paramètres de document.</span><span class="sxs-lookup"><span data-stu-id="4200d-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="4200d-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="4200d-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4200d-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="4200d-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4200d-130">Spécifie la structure de **la feuille ShapeSheet** d’un document.</span><span class="sxs-lookup"><span data-stu-id="4200d-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="4200d-131">EventList</span><span class="sxs-lookup"><span data-stu-id="4200d-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4200d-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="4200d-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4200d-133">Contient un élément **EventItem** pour chaque événement auquel un objet doit répondre.</span><span class="sxs-lookup"><span data-stu-id="4200d-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="4200d-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="4200d-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4200d-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="4200d-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4200d-136">Contient une collection d’éléments de **nom de la police** .</span><span class="sxs-lookup"><span data-stu-id="4200d-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="4200d-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="4200d-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4200d-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="4200d-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4200d-139">Contient les éléments d’en-tête et de pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="4200d-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="4200d-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="4200d-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4200d-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="4200d-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4200d-142">Spécifie le jeu de pages qui sont visibles et définir des jeux d’enregistrements qui sont actualisables dans un dessin de dessin.</span><span class="sxs-lookup"><span data-stu-id="4200d-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="4200d-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="4200d-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4200d-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="4200d-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4200d-145">Contient une collection d’éléments de feuille de style pour le document.</span><span class="sxs-lookup"><span data-stu-id="4200d-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4200d-146">Attributs</span><span class="sxs-lookup"><span data-stu-id="4200d-146">Attributes</span></span>

<span data-ttu-id="4200d-147">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4200d-147">None.</span></span>
  

