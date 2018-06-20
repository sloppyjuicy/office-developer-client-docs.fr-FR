---
title: CustomToolbarsFile, élément (DocumentSettings_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9789239-a919-97f6-8109-126bb1038be6
description: Contient le nom du fichier (.vsu) d’interface utilisateur Microsoft Visio qui définit les barres d’outils personnalisées et des barres d’état pour un document.
ms.openlocfilehash: 46abc567d2135815a82b4efec47a7bd77d0763cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788401"
---
# <a name="customtoolbarsfile-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="2b09f-103">CustomToolbarsFile, élément (DocumentSettings_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="2b09f-103">CustomToolbarsFile element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2b09f-104">Contient le nom du fichier (.vsu) d’interface utilisateur Microsoft Visio qui définit les barres d’outils personnalisées et des barres d’état pour un document.</span><span class="sxs-lookup"><span data-stu-id="2b09f-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom toolbars and status bars for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b09f-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="2b09f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b09f-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="2b09f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2b09f-107">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="2b09f-107">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2b09f-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="2b09f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2b09f-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="2b09f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2b09f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2b09f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2b09f-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="2b09f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2b09f-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="2b09f-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2b09f-113">Définition</span><span class="sxs-lookup"><span data-stu-id="2b09f-113">Definition</span></span>

```XML
< xs:element name="CustomToolbarsFile" type="CustomToolbarsFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2b09f-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="2b09f-114">Elements and attributes</span></span>

<span data-ttu-id="2b09f-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="2b09f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2b09f-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2b09f-116">Parent elements</span></span>

|<span data-ttu-id="2b09f-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2b09f-117">**Element**</span></span>|<span data-ttu-id="2b09f-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="2b09f-118">**Type**</span></span>|<span data-ttu-id="2b09f-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="2b09f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2b09f-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="2b09f-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2b09f-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="2b09f-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2b09f-122">Contient des éléments qui spécifient les paramètres de document.</span><span class="sxs-lookup"><span data-stu-id="2b09f-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2b09f-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2b09f-123">Child elements</span></span>

<span data-ttu-id="2b09f-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2b09f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b09f-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="2b09f-125">Attributes</span></span>

<span data-ttu-id="2b09f-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2b09f-126">None.</span></span>
  

