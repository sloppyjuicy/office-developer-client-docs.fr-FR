---
title: Type complexe StyleSheets_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: a48dc8d4c8327cffc53469a8c6d8a81d021a4500
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789832"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="a0c83-102">Type complexe StyleSheets_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="a0c83-102">StyleSheets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a0c83-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a0c83-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0c83-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="a0c83-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a0c83-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a0c83-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a0c83-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a0c83-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a0c83-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a0c83-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a0c83-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="a0c83-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a0c83-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a0c83-109">Definition</span></span>

```XML
          <xs:complexType name="StyleSheets_Type">
          
          <xs:sequence>
    <xs:element name="StyleSheet"  type="StyleSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a0c83-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a0c83-110">Elements and attributes</span></span>

<span data-ttu-id="a0c83-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="a0c83-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a0c83-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a0c83-112">Child elements</span></span>

|<span data-ttu-id="a0c83-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a0c83-113">**Element**</span></span>|<span data-ttu-id="a0c83-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="a0c83-114">**Type**</span></span>|<span data-ttu-id="a0c83-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a0c83-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a0c83-116">Feuille de style</span><span class="sxs-lookup"><span data-stu-id="a0c83-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a0c83-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a0c83-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a0c83-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="a0c83-118">Attributes</span></span>

<span data-ttu-id="a0c83-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a0c83-119">None.</span></span>
  

