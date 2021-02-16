---
title: Élément VisioDocument (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Élément racine d’un document Microsoft Visio.
ms.openlocfilehash: acb0a4e8ef1efb6d6d5872118241e36bb4e9630c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538486"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="c16c9-103">Élément VisioDocument (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c16c9-103">VisioDocument element (Visio XML)</span></span>

<span data-ttu-id="c16c9-104">Élément racine d’un document Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="c16c9-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c16c9-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="c16c9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c16c9-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="c16c9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c16c9-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="c16c9-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c16c9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c16c9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c16c9-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c16c9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c16c9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c16c9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c16c9-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="c16c9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c16c9-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="c16c9-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c16c9-113">Définition</span><span class="sxs-lookup"><span data-stu-id="c16c9-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c16c9-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c16c9-114">Elements and attributes</span></span>

<span data-ttu-id="c16c9-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="c16c9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c16c9-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c16c9-116">Parent elements</span></span>

<span data-ttu-id="c16c9-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="c16c9-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c16c9-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c16c9-118">Child elements</span></span>

|<span data-ttu-id="c16c9-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c16c9-119">**Element**</span></span>|<span data-ttu-id="c16c9-120">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c16c9-120">**Type**</span></span>|<span data-ttu-id="c16c9-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="c16c9-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c16c9-122">Colors</span><span class="sxs-lookup"><span data-stu-id="c16c9-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c16c9-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="c16c9-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c16c9-124">Contient le tableau de couleurs du document.</span><span class="sxs-lookup"><span data-stu-id="c16c9-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="c16c9-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="c16c9-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c16c9-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="c16c9-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c16c9-127">Contient des éléments qui spécifient les paramètres de document.</span><span class="sxs-lookup"><span data-stu-id="c16c9-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="c16c9-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="c16c9-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c16c9-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="c16c9-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c16c9-130">Spécifie la structure **shapeSheet d’un** document.</span><span class="sxs-lookup"><span data-stu-id="c16c9-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="c16c9-131">EventList</span><span class="sxs-lookup"><span data-stu-id="c16c9-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c16c9-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="c16c9-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c16c9-133">Contient un **élément EventItem** pour chaque événement auquel un objet doit répondre.</span><span class="sxs-lookup"><span data-stu-id="c16c9-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="c16c9-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="c16c9-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c16c9-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="c16c9-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c16c9-136">Contient une collection **d’éléments FaceName.**</span><span class="sxs-lookup"><span data-stu-id="c16c9-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="c16c9-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="c16c9-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c16c9-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="c16c9-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c16c9-139">Contient des éléments pour l’en-tête et le pied de groupe d’un document.</span><span class="sxs-lookup"><span data-stu-id="c16c9-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="c16c9-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="c16c9-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c16c9-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="c16c9-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c16c9-142">Spécifie l’ensemble des pages de dessin qui sont consultables et des jeux d’enregistrements actualisables dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="c16c9-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="c16c9-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="c16c9-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c16c9-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="c16c9-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c16c9-145">Contient une collection d’éléments StyleSheet pour le document.</span><span class="sxs-lookup"><span data-stu-id="c16c9-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c16c9-146">Attributs</span><span class="sxs-lookup"><span data-stu-id="c16c9-146">Attributes</span></span>

<span data-ttu-id="c16c9-147">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c16c9-147">None.</span></span>
  

