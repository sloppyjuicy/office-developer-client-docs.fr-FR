---
title: Type complexe Connects_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 68a85d32-9bf2-2f7c-2797-85ddd593fc37
ms.openlocfilehash: 4d2740bc0ee0934b28bbebbc10ca9c861c563be0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788346"
---
# <a name="connectstype-complextype-visio-xml"></a><span data-ttu-id="34920-102">Type complexe Connects_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="34920-102">Connects_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="34920-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="34920-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34920-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="34920-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="34920-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="34920-105">**Schema file**</span></span> <br/> |<span data-ttu-id="34920-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="34920-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="34920-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="34920-107">**Extension base**</span></span> <br/> |<span data-ttu-id="34920-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="34920-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="34920-109">Définition</span><span class="sxs-lookup"><span data-stu-id="34920-109">Definition</span></span>

```XML
          <xs:complexType name="Connects_Type">
          
          <xs:sequence>
    <xs:element name="Connect"  type="Connect_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="34920-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="34920-110">Elements and attributes</span></span>

<span data-ttu-id="34920-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="34920-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="34920-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="34920-112">Child elements</span></span>

|<span data-ttu-id="34920-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="34920-113">**Element**</span></span>|<span data-ttu-id="34920-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="34920-114">**Type**</span></span>|<span data-ttu-id="34920-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="34920-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="34920-116">Connect</span><span class="sxs-lookup"><span data-stu-id="34920-116">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="34920-117">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="34920-117">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="34920-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="34920-118">Attributes</span></span>

<span data-ttu-id="34920-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="34920-119">None.</span></span>
  

