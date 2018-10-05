---
title: Type complexe FaceNames_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 234bbe07-004e-0604-144c-376d7b06994b
ms.openlocfilehash: 6f9cd84dffc22f4211a8445a2d493ef7d4f4a4f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387145"
---
# <a name="facenamestype-complextype-visio-xml"></a><span data-ttu-id="467b8-102">Type complexe FaceNames_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="467b8-102">FaceNames_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="467b8-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="467b8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="467b8-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="467b8-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="467b8-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="467b8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="467b8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="467b8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="467b8-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="467b8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="467b8-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="467b8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="467b8-109">Définition</span><span class="sxs-lookup"><span data-stu-id="467b8-109">Definition</span></span>

```XML
          <xs:complexType name="FaceNames_Type">
          
          <xs:sequence>
    <xs:element name="FaceName"  type="FaceName_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="467b8-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="467b8-110">Elements and attributes</span></span>

<span data-ttu-id="467b8-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="467b8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="467b8-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="467b8-112">Child elements</span></span>

|<span data-ttu-id="467b8-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="467b8-113">**Element**</span></span>|<span data-ttu-id="467b8-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="467b8-114">**Type**</span></span>|<span data-ttu-id="467b8-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="467b8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="467b8-116">Nom de la police</span><span class="sxs-lookup"><span data-stu-id="467b8-116">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="467b8-117">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="467b8-117">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="467b8-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="467b8-118">Attributes</span></span>

<span data-ttu-id="467b8-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="467b8-119">None.</span></span>
  

