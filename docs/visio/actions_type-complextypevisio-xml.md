---
title: Actions_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: 384b948c61f3b618d108db090721ea6768d69372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538409"
---
# <a name="actions_type-complextype-visio-xml"></a><span data-ttu-id="9b1d6-102">Actions_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9b1d6-102">Actions_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9b1d6-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9b1d6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b1d6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9b1d6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9b1d6-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9b1d6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9b1d6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9b1d6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9b1d6-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9b1d6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9b1d6-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="9b1d6-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9b1d6-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9b1d6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9b1d6-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9b1d6-110">Elements and attributes</span></span>

<span data-ttu-id="9b1d6-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="9b1d6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9b1d6-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9b1d6-112">Child elements</span></span>

|<span data-ttu-id="9b1d6-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9b1d6-113">**Element**</span></span>|<span data-ttu-id="9b1d6-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="9b1d6-114">**Type**</span></span>|<span data-ttu-id="9b1d6-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9b1d6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9b1d6-116">Row</span><span class="sxs-lookup"><span data-stu-id="9b1d6-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9b1d6-117">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="9b1d6-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9b1d6-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="9b1d6-118">Attributes</span></span>

<span data-ttu-id="9b1d6-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9b1d6-119">None.</span></span>
  

