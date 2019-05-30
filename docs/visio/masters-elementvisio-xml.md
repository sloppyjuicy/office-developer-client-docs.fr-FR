---
title: Masters, élément (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Contient les éléments de forme de base pour le document.
ms.openlocfilehash: b2506466a5208223e3e7b9668ad6442030ec95c9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538052"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="5b201-103">Masters, élément (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5b201-103">Masters element (Visio XML)</span></span>

<span data-ttu-id="5b201-104">Contient les éléments de forme de base pour le document.</span><span class="sxs-lookup"><span data-stu-id="5b201-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b201-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="5b201-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b201-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="5b201-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5b201-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="5b201-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5b201-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5b201-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5b201-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="5b201-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5b201-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="5b201-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5b201-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="5b201-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5b201-112">Masters. Xml</span><span class="sxs-lookup"><span data-stu-id="5b201-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5b201-113">Définition</span><span class="sxs-lookup"><span data-stu-id="5b201-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5b201-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="5b201-114">Elements and attributes</span></span>

<span data-ttu-id="5b201-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="5b201-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5b201-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5b201-116">Parent elements</span></span>

<span data-ttu-id="5b201-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="5b201-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b201-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5b201-118">Child elements</span></span>

|<span data-ttu-id="5b201-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5b201-119">**Element**</span></span>|<span data-ttu-id="5b201-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="5b201-120">**Type**</span></span>|<span data-ttu-id="5b201-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="5b201-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b201-122">Master</span><span class="sxs-lookup"><span data-stu-id="5b201-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b201-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="5b201-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b201-124">Contient des éléments qui définissent une forme de base pour le document.</span><span class="sxs-lookup"><span data-stu-id="5b201-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="5b201-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="5b201-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b201-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="5b201-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b201-127">Spécifie un raccourci de forme de base défini dans le document.</span><span class="sxs-lookup"><span data-stu-id="5b201-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5b201-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="5b201-128">Attributes</span></span>

<span data-ttu-id="5b201-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5b201-129">None.</span></span>
  

