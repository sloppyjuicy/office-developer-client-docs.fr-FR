---
title: ComplexType ActionTagRow_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d42c212-b068-84fa-e271-bbe1fae52a48
ms.openlocfilehash: 7d2822cb0df0b18e7f19e380fc3e1ba9e4f10c69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541371"
---
# <a name="actiontagrowtype-complextype-visio-xml"></a><span data-ttu-id="0d0f6-102">ComplexType ActionTagRow_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0d0f6-102">ActionTagRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0d0f6-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="0d0f6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d0f6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0d0f6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0d0f6-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0d0f6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0d0f6-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="0d0f6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0d0f6-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="0d0f6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0d0f6-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="0d0f6-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0d0f6-109">Définition</span><span class="sxs-lookup"><span data-stu-id="0d0f6-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTagRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0d0f6-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0d0f6-110">Elements and attributes</span></span>

<span data-ttu-id="0d0f6-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="0d0f6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0d0f6-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0d0f6-112">Child elements</span></span>

|<span data-ttu-id="0d0f6-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0d0f6-113">**Element**</span></span>|<span data-ttu-id="0d0f6-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="0d0f6-114">**Type**</span></span>|<span data-ttu-id="0d0f6-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="0d0f6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0d0f6-116">Cell</span><span class="sxs-lookup"><span data-stu-id="0d0f6-116">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0d0f6-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0d0f6-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0d0f6-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="0d0f6-118">Attributes</span></span>

<span data-ttu-id="0d0f6-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0d0f6-119">None.</span></span>
  

