---
title: ControlRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f9ee251-e685-e56c-3c8a-cb727ad62064
ms.openlocfilehash: a6bd54f425e211716ce7dc9a7206a3d079383d5d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538668"
---
# <a name="controlrow_type-complextype-visio-xml"></a><span data-ttu-id="fda70-102">ControlRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fda70-102">ControlRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="fda70-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="fda70-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fda70-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fda70-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fda70-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fda70-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fda70-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fda70-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fda70-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="fda70-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fda70-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="fda70-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fda70-109">Définition</span><span class="sxs-lookup"><span data-stu-id="fda70-109">Definition</span></span>

```XML
          <xs:complexType name="ControlRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedIndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="fda70-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fda70-110">Elements and attributes</span></span>

<span data-ttu-id="fda70-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="fda70-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fda70-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fda70-112">Child elements</span></span>

|<span data-ttu-id="fda70-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fda70-113">**Element**</span></span>|<span data-ttu-id="fda70-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="fda70-114">**Type**</span></span>|<span data-ttu-id="fda70-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="fda70-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fda70-116">Cell</span><span class="sxs-lookup"><span data-stu-id="fda70-116">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="fda70-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="fda70-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fda70-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="fda70-118">Attributes</span></span>

<span data-ttu-id="fda70-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fda70-119">None.</span></span>
  

