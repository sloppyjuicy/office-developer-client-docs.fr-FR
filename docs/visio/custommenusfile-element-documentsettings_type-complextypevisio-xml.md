---
title: Élément CustomMenusFile (complexType DocumentSettings_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4c88bde5-45e1-8030-e72c-a735c374a5c4
description: Contient le nom du fichier d'interface utilisateur Microsoft Visio (. VSU) qui définit les menus et les raccourcis personnalisés d'un document.
ms.openlocfilehash: 347660abab266493254b4dc2b47150f3b80fd371
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282900"
---
# <a name="custommenusfile-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="e4fcd-103">Élément CustomMenusFile (complexType DocumentSettings_Type) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e4fcd-103">CustomMenusFile element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e4fcd-104">Contient le nom du fichier d'interface utilisateur Microsoft Visio (. VSU) qui définit les menus et les raccourcis personnalisés d'un document.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-104">Contains the name of the Microsoft Visio user interface (.vsu) file that defines custom menus and accelerators for a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e4fcd-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="e4fcd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e4fcd-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="e4fcd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e4fcd-107">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="e4fcd-107">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e4fcd-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e4fcd-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e4fcd-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e4fcd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e4fcd-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="e4fcd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e4fcd-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="e4fcd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e4fcd-112">document. Xml</span><span class="sxs-lookup"><span data-stu-id="e4fcd-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e4fcd-113">Définition</span><span class="sxs-lookup"><span data-stu-id="e4fcd-113">Definition</span></span>

```XML
< xs:element name="CustomMenusFile" type="CustomMenusFile_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e4fcd-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e4fcd-114">Elements and attributes</span></span>

<span data-ttu-id="e4fcd-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e4fcd-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e4fcd-116">Parent elements</span></span>

|<span data-ttu-id="e4fcd-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e4fcd-117">**Element**</span></span>|<span data-ttu-id="e4fcd-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="e4fcd-118">**Type**</span></span>|<span data-ttu-id="e4fcd-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="e4fcd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e4fcd-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="e4fcd-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e4fcd-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="e4fcd-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e4fcd-122">Contient les éléments qui spécifient les paramètres de document.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e4fcd-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e4fcd-123">Child elements</span></span>

<span data-ttu-id="e4fcd-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e4fcd-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="e4fcd-125">Attributes</span></span>

<span data-ttu-id="e4fcd-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-126">None.</span></span>
  

