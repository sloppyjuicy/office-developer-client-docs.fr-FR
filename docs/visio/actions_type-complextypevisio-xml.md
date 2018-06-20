---
title: Type complexe Actions_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: e28b80e64865196fd6ba13035385b9523f6b1bc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788005"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="7f92f-102">Type complexe Actions_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="7f92f-102">Actions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7f92f-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7f92f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f92f-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="7f92f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7f92f-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7f92f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7f92f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7f92f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7f92f-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7f92f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7f92f-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="7f92f-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7f92f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="7f92f-109">Definition</span></span>

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7f92f-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7f92f-110">Elements and attributes</span></span>

<span data-ttu-id="7f92f-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="7f92f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7f92f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7f92f-112">Child elements</span></span>

|<span data-ttu-id="7f92f-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7f92f-113">**Element**</span></span>|<span data-ttu-id="7f92f-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="7f92f-114">**Type**</span></span>|<span data-ttu-id="7f92f-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="7f92f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7f92f-116">Row</span><span class="sxs-lookup"><span data-stu-id="7f92f-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="7f92f-117">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="7f92f-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7f92f-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="7f92f-118">Attributes</span></span>

<span data-ttu-id="7f92f-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7f92f-119">None.</span></span>
  

