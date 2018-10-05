---
title: Type complexe Scratch_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e3dd8c8-e84c-61ff-bfff-57d97545e441
ms.openlocfilehash: 4002466eb98beac889fb27b2aec07aa6a5e31ceb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398961"
---
# <a name="scratchtype-complextype-visio-xml"></a><span data-ttu-id="e5212-102">Type complexe Scratch_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="e5212-102">Scratch_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e5212-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="e5212-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5212-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e5212-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e5212-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e5212-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e5212-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e5212-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e5212-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="e5212-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e5212-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="e5212-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e5212-109">Définition</span><span class="sxs-lookup"><span data-stu-id="e5212-109">Definition</span></span>

```XML
          <xs:complexType name="Scratch_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ScratchRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e5212-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e5212-110">Elements and attributes</span></span>

<span data-ttu-id="e5212-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="e5212-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e5212-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e5212-112">Child elements</span></span>

|<span data-ttu-id="e5212-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e5212-113">**Element**</span></span>|<span data-ttu-id="e5212-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="e5212-114">**Type**</span></span>|<span data-ttu-id="e5212-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="e5212-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e5212-116">Row</span><span class="sxs-lookup"><span data-stu-id="e5212-116">Row</span></span>](row-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e5212-117">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="e5212-117">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e5212-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="e5212-118">Attributes</span></span>

<span data-ttu-id="e5212-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e5212-119">None.</span></span>
  

