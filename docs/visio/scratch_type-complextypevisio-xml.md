---
title: Type complexe Scratch_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e3dd8c8-e84c-61ff-bfff-57d97545e441
ms.openlocfilehash: 973a0db86eec553c7a728095e28735d4cdb91041
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789592"
---
# <a name="scratchtype-complextype-visio-xml"></a><span data-ttu-id="6bcae-102">Type complexe Scratch_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="6bcae-102">Scratch_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6bcae-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="6bcae-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6bcae-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="6bcae-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6bcae-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6bcae-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6bcae-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6bcae-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6bcae-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="6bcae-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6bcae-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="6bcae-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6bcae-109">Définition</span><span class="sxs-lookup"><span data-stu-id="6bcae-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6bcae-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6bcae-110">Elements and attributes</span></span>

<span data-ttu-id="6bcae-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="6bcae-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6bcae-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6bcae-112">Child elements</span></span>

|<span data-ttu-id="6bcae-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6bcae-113">**Element**</span></span>|<span data-ttu-id="6bcae-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="6bcae-114">**Type**</span></span>|<span data-ttu-id="6bcae-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="6bcae-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6bcae-116">Row</span><span class="sxs-lookup"><span data-stu-id="6bcae-116">Row</span></span>](row-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="6bcae-117">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="6bcae-117">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6bcae-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="6bcae-118">Attributes</span></span>

<span data-ttu-id="6bcae-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6bcae-119">None.</span></span>
  

