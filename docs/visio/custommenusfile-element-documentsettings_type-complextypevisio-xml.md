---
title: Élément CustomMenusFile (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4c88bde5-45e1-8030-e72c-a735c374a5c4
description: Contient le nom du fichier d’interface Visio Microsoft (.vsu) qui définit des menus et des accélérateurs personnalisés pour un document.
ms.openlocfilehash: 69eca703acf30a10296c13452c2f3e2a11521cd4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540524"
---
# <a name="custommenusfile-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="2a52a-103">Élément CustomMenusFile (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2a52a-103">CustomMenusFile element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="2a52a-104">Contient le nom du fichier d’interface Visio Microsoft (.vsu) qui définit des menus et des accélérateurs personnalisés pour un document.</span><span class="sxs-lookup"><span data-stu-id="2a52a-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom menus and accelerators for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a52a-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="2a52a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a52a-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="2a52a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2a52a-107">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="2a52a-107">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2a52a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2a52a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2a52a-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="2a52a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2a52a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2a52a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2a52a-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="2a52a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2a52a-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="2a52a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2a52a-113">Définition</span><span class="sxs-lookup"><span data-stu-id="2a52a-113">Definition</span></span>

```XML
< xs:element name="CustomMenusFile" type="CustomMenusFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2a52a-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="2a52a-114">Elements and attributes</span></span>

<span data-ttu-id="2a52a-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="2a52a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2a52a-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2a52a-116">Parent elements</span></span>

|<span data-ttu-id="2a52a-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2a52a-117">**Element**</span></span>|<span data-ttu-id="2a52a-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="2a52a-118">**Type**</span></span>|<span data-ttu-id="2a52a-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="2a52a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2a52a-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="2a52a-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2a52a-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="2a52a-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2a52a-122">Contient des éléments qui spécifient les paramètres de document.</span><span class="sxs-lookup"><span data-stu-id="2a52a-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2a52a-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2a52a-123">Child elements</span></span>

<span data-ttu-id="2a52a-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2a52a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a52a-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="2a52a-125">Attributes</span></span>

<span data-ttu-id="2a52a-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2a52a-126">None.</span></span>
  

