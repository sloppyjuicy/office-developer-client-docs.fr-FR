---
title: Type complexe Tabs_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b97155ce-f0d2-e35c-bc58-e288f653ce2c
ms.openlocfilehash: a46e9d0cfa1ad0e9bd398afec7a2f03de46c367f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789846"
---
# <a name="tabstype-complextype-visio-xml"></a><span data-ttu-id="9a614-102">Type complexe Tabs_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="9a614-102">Tabs_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9a614-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9a614-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a614-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="9a614-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9a614-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9a614-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9a614-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9a614-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9a614-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9a614-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9a614-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="9a614-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a614-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9a614-109">Definition</span></span>

```XML
          <xs:complexType name="Tabs_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="TabsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9a614-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9a614-110">Elements and attributes</span></span>

<span data-ttu-id="9a614-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="9a614-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9a614-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9a614-112">Child elements</span></span>

|<span data-ttu-id="9a614-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9a614-113">**Element**</span></span>|<span data-ttu-id="9a614-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="9a614-114">**Type**</span></span>|<span data-ttu-id="9a614-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9a614-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9a614-116">Row</span><span class="sxs-lookup"><span data-stu-id="9a614-116">Row</span></span>](row-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9a614-117">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="9a614-117">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9a614-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="9a614-118">Attributes</span></span>

<span data-ttu-id="9a614-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9a614-119">None.</span></span>
  

