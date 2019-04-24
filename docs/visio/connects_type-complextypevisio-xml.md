---
title: ComplexType Connects_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 68a85d32-9bf2-2f7c-2797-85ddd593fc37
ms.openlocfilehash: ed5046656554fdd64251601c12e6817d586cd689
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319571"
---
# <a name="connectstype-complextype-visio-xml"></a><span data-ttu-id="68d26-102">ComplexType Connects_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="68d26-102">Connects_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="68d26-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="68d26-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68d26-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="68d26-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="68d26-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="68d26-105">**Schema file**</span></span> <br/> |<span data-ttu-id="68d26-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="68d26-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="68d26-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="68d26-107">**Extension base**</span></span> <br/> |<span data-ttu-id="68d26-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="68d26-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68d26-109">Définition</span><span class="sxs-lookup"><span data-stu-id="68d26-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="68d26-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="68d26-110">Elements and attributes</span></span>

<span data-ttu-id="68d26-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="68d26-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="68d26-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="68d26-112">Child elements</span></span>

|<span data-ttu-id="68d26-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="68d26-113">**Element**</span></span>|<span data-ttu-id="68d26-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="68d26-114">**Type**</span></span>|<span data-ttu-id="68d26-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="68d26-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68d26-116">Connect</span><span class="sxs-lookup"><span data-stu-id="68d26-116">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68d26-117">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="68d26-117">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="68d26-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="68d26-118">Attributes</span></span>

<span data-ttu-id="68d26-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="68d26-119">None.</span></span>
  

