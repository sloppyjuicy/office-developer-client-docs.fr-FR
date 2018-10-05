---
title: Type complexe TabsRow_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8b9258a0-05fa-b0b0-90ed-dc1c4faa288a
ms.openlocfilehash: fed6c70119007164113ba76296bed5662e331c17
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395321"
---
# <a name="tabsrowtype-complextype-visio-xml"></a><span data-ttu-id="6288d-102">Type complexe TabsRow_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="6288d-102">TabsRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6288d-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="6288d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6288d-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="6288d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6288d-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6288d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6288d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6288d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6288d-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="6288d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6288d-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="6288d-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6288d-109">Définition</span><span class="sxs-lookup"><span data-stu-id="6288d-109">Definition</span></span>

```XML
          <xs:complexType name="TabsRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6288d-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6288d-110">Elements and attributes</span></span>

<span data-ttu-id="6288d-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="6288d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6288d-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6288d-112">Child elements</span></span>

|<span data-ttu-id="6288d-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6288d-113">**Element**</span></span>|<span data-ttu-id="6288d-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="6288d-114">**Type**</span></span>|<span data-ttu-id="6288d-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="6288d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6288d-116">Cell</span><span class="sxs-lookup"><span data-stu-id="6288d-116">Cell</span></span>](cell-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="6288d-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="6288d-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6288d-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="6288d-118">Attributes</span></span>

<span data-ttu-id="6288d-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6288d-119">None.</span></span>
  

