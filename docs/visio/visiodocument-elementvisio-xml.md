---
title: Élément VisioDocument (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Élément racine d’un document Microsoft Visio document.
ms.openlocfilehash: acb0a4e8ef1efb6d6d5872118241e36bb4e9630c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538486"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="738a2-103">Élément VisioDocument (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="738a2-103">VisioDocument element (Visio XML)</span></span>

<span data-ttu-id="738a2-104">Élément racine d’un document Microsoft Visio document.</span><span class="sxs-lookup"><span data-stu-id="738a2-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="738a2-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="738a2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="738a2-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="738a2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="738a2-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="738a2-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="738a2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="738a2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="738a2-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="738a2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="738a2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="738a2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="738a2-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="738a2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="738a2-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="738a2-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="738a2-113">Définition</span><span class="sxs-lookup"><span data-stu-id="738a2-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="738a2-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="738a2-114">Elements and attributes</span></span>

<span data-ttu-id="738a2-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="738a2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="738a2-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="738a2-116">Parent elements</span></span>

<span data-ttu-id="738a2-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="738a2-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="738a2-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="738a2-118">Child elements</span></span>

|<span data-ttu-id="738a2-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="738a2-119">**Element**</span></span>|<span data-ttu-id="738a2-120">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="738a2-120">**Type**</span></span>|<span data-ttu-id="738a2-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="738a2-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="738a2-122">Colors</span><span class="sxs-lookup"><span data-stu-id="738a2-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="738a2-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="738a2-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="738a2-124">Contient le tableau de couleurs du document.</span><span class="sxs-lookup"><span data-stu-id="738a2-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="738a2-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="738a2-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="738a2-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="738a2-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="738a2-127">Contient des éléments qui spécifient les paramètres de document.</span><span class="sxs-lookup"><span data-stu-id="738a2-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="738a2-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="738a2-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="738a2-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="738a2-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="738a2-130">Spécifie la structure **shapeSheet d’un** document.</span><span class="sxs-lookup"><span data-stu-id="738a2-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="738a2-131">EventList</span><span class="sxs-lookup"><span data-stu-id="738a2-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="738a2-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="738a2-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="738a2-133">Contient un **élément EventItem** pour chaque événement auquel un objet doit répondre.</span><span class="sxs-lookup"><span data-stu-id="738a2-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="738a2-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="738a2-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="738a2-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="738a2-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="738a2-136">Contient une collection **d’éléments FaceName.**</span><span class="sxs-lookup"><span data-stu-id="738a2-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="738a2-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="738a2-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="738a2-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="738a2-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="738a2-139">Contient des éléments pour l’en-tête et le pied de groupe d’un document.</span><span class="sxs-lookup"><span data-stu-id="738a2-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="738a2-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="738a2-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="738a2-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="738a2-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="738a2-142">Spécifie l’ensemble des pages de dessin qui sont consultables et un ensemble de jeux d’enregistrements actualisables dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="738a2-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="738a2-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="738a2-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="738a2-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="738a2-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="738a2-145">Contient une collection d’éléments StyleSheet pour le document.</span><span class="sxs-lookup"><span data-stu-id="738a2-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="738a2-146">Attributs</span><span class="sxs-lookup"><span data-stu-id="738a2-146">Attributes</span></span>

<span data-ttu-id="738a2-147">Aucun.</span><span class="sxs-lookup"><span data-stu-id="738a2-147">None.</span></span>
  

