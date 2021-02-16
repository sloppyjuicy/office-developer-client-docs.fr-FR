---
title: Character_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 94a2aab3-6220-0cc5-ddc8-77a785821985
ms.openlocfilehash: c84a8d71fc2f080600a20625087d7c252bdcb3eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540202"
---
# <a name="character_type-complextype-visio-xml"></a><span data-ttu-id="be364-102">Character_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="be364-102">Character_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="be364-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="be364-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be364-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="be364-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="be364-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="be364-105">**Schema file**</span></span> <br/> |<span data-ttu-id="be364-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="be364-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="be364-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="be364-107">**Extension base**</span></span> <br/> |<span data-ttu-id="be364-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="be364-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="be364-109">Définition</span><span class="sxs-lookup"><span data-stu-id="be364-109">Definition</span></span>

```XML
          <xs:complexType name="Character_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="CharacterRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="be364-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="be364-110">Elements and attributes</span></span>

<span data-ttu-id="be364-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="be364-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="be364-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="be364-112">Child elements</span></span>

|<span data-ttu-id="be364-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="be364-113">**Element**</span></span>|<span data-ttu-id="be364-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="be364-114">**Type**</span></span>|<span data-ttu-id="be364-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="be364-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be364-116">Row</span><span class="sxs-lookup"><span data-stu-id="be364-116">Row</span></span>](row-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="be364-117">CharacterRow_Type</span><span class="sxs-lookup"><span data-stu-id="be364-117">CharacterRow_Type</span></span>](characterrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="be364-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="be364-118">Attributes</span></span>

<span data-ttu-id="be364-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="be364-119">None.</span></span>
  

