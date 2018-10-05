---
title: Masters, élément (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Contient la forme de base des éléments pour le document.
ms.openlocfilehash: ea2cee2f9845f8a72220081617a11cf4f72dafd1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400991"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="78c7b-103">Masters, élément (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="78c7b-103">Masters element ('Visio XML')</span></span>

<span data-ttu-id="78c7b-104">Contient la forme de base des éléments pour le document.</span><span class="sxs-lookup"><span data-stu-id="78c7b-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78c7b-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="78c7b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78c7b-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="78c7b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="78c7b-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="78c7b-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="78c7b-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="78c7b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="78c7b-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="78c7b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="78c7b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="78c7b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="78c7b-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="78c7b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="78c7b-112">Masters.Xml</span><span class="sxs-lookup"><span data-stu-id="78c7b-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="78c7b-113">Définition</span><span class="sxs-lookup"><span data-stu-id="78c7b-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="78c7b-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="78c7b-114">Elements and attributes</span></span>

<span data-ttu-id="78c7b-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="78c7b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="78c7b-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="78c7b-116">Parent elements</span></span>

<span data-ttu-id="78c7b-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="78c7b-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78c7b-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="78c7b-118">Child elements</span></span>

|<span data-ttu-id="78c7b-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="78c7b-119">**Element**</span></span>|<span data-ttu-id="78c7b-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="78c7b-120">**Type**</span></span>|<span data-ttu-id="78c7b-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="78c7b-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="78c7b-122">Forme de base</span><span class="sxs-lookup"><span data-stu-id="78c7b-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78c7b-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="78c7b-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78c7b-124">Contient des éléments qui définissent un masque du document.</span><span class="sxs-lookup"><span data-stu-id="78c7b-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="78c7b-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="78c7b-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78c7b-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="78c7b-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78c7b-127">Spécifie un raccourci de base défini dans le document.</span><span class="sxs-lookup"><span data-stu-id="78c7b-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="78c7b-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="78c7b-128">Attributes</span></span>

<span data-ttu-id="78c7b-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="78c7b-129">None.</span></span>
  

