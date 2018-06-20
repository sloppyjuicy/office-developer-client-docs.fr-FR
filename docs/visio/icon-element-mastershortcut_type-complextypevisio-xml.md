---
title: Icon, élément (MasterShortcut_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 07d8ba86-8e35-d151-e6c1-150c37cc2acd
description: Spécifie qu'un MIME (Multipurpose Internet Mail Extensions) codés icône binaire (au format .ico) d’un élément MasterShortcut dans un document.
ms.openlocfilehash: 46ca7c3f6ba733d31823f6b47f083c46dd941c14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788803"
---
# <a name="icon-element-mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="2a516-103">Icon, élément (MasterShortcut_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="2a516-103">Icon element (MasterShortcut_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2a516-104">Spécifie qu'un MIME (Multipurpose Internet Mail Extensions) codés icône binaire (au format .ico) d’un élément MasterShortcut dans un document.</span><span class="sxs-lookup"><span data-stu-id="2a516-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a MasterShortcut element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a516-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="2a516-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a516-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="2a516-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2a516-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="2a516-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2a516-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="2a516-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2a516-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="2a516-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2a516-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2a516-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2a516-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="2a516-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2a516-112">Masters.Xml</span><span class="sxs-lookup"><span data-stu-id="2a516-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2a516-113">Définition</span><span class="sxs-lookup"><span data-stu-id="2a516-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2a516-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="2a516-114">Elements and attributes</span></span>

<span data-ttu-id="2a516-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="2a516-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2a516-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2a516-116">Parent elements</span></span>

|<span data-ttu-id="2a516-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2a516-117">**Element**</span></span>|<span data-ttu-id="2a516-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="2a516-118">**Type**</span></span>|<span data-ttu-id="2a516-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="2a516-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2a516-120">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="2a516-120">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2a516-121">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="2a516-121">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2a516-122">Spécifie un format maître inutilisé.</span><span class="sxs-lookup"><span data-stu-id="2a516-122">Specifies an unused master format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2a516-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2a516-123">Child elements</span></span>

<span data-ttu-id="2a516-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2a516-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a516-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="2a516-125">Attributes</span></span>

<span data-ttu-id="2a516-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2a516-126">None.</span></span>
  

