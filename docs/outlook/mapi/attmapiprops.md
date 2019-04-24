---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 185bfbb151c4f8d4e36b40b94393d14d50c33edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318122"
---
# <a name="attmapiprops"></a><span data-ttu-id="430c1-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="430c1-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="430c1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="430c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="430c1-105">L'attribut **attMAPIProps** est spécial dans la mesure où il peut être utilisé pour coder n'importe quelle propriété MAPI qui n'a pas de contrepartie dans le jeu d'attributs définis par le format TNEF existant.</span><span class="sxs-lookup"><span data-stu-id="430c1-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="430c1-106">Les données d'attribut sont un ensemble compté de propriétés MAPI, de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="430c1-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="430c1-107">Le format de ce codage, qui permet d'utiliser n'importe quel ensemble de propriétés MAPI, est le suivant:</span><span class="sxs-lookup"><span data-stu-id="430c1-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="430c1-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="430c1-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="430c1-109">propriété-Count _Property_Value,..._</span><span class="sxs-lookup"><span data-stu-id="430c1-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="430c1-110">Il doit y avoir autant d'éléments _Property_Value_ que la valeur du nombre de propriétés.</span><span class="sxs-lookup"><span data-stu-id="430c1-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="430c1-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="430c1-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="430c1-112">propriété-Tag _Property_property _propriété Proptag_Name_</span><span class="sxs-lookup"><span data-stu-id="430c1-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="430c1-113">La balise property est simplement la valeur associée à l'identificateur de la propriété, telle que 0x0037001F pour **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="430c1-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="430c1-114">_Inspecteur_</span><span class="sxs-lookup"><span data-stu-id="430c1-114">_Property:_</span></span>
  
>  <span data-ttu-id="430c1-115">__ Valeur de la valeur-nombre _,..._</span><span class="sxs-lookup"><span data-stu-id="430c1-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="430c1-116">_Valeur :_</span><span class="sxs-lookup"><span data-stu-id="430c1-116">_Value:_</span></span>
  
> <span data-ttu-id="430c1-117">value-Data value-Size value-Data Padding value-Size value-IID value-Data Padding</span><span class="sxs-lookup"><span data-stu-id="430c1-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="430c1-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="430c1-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="430c1-119">name-GUID nom-type nom-ID nom-GUID nom-type nom-chaîne-longueur nom-chaîne remplissage de la chaîne</span><span class="sxs-lookup"><span data-stu-id="430c1-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="430c1-120">L'encapsulation de chaque propriété varie en fonction de l'identificateur de propriété et du type de propriété.</span><span class="sxs-lookup"><span data-stu-id="430c1-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="430c1-121">Les balises, identificateurs et types de propriété sont définis dans les fichiers d'en-tête Mapitags. h et Mapidefs. h.</span><span class="sxs-lookup"><span data-stu-id="430c1-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="430c1-122">Si la propriété est une propriété nommée, la balise de la propriété est immédiatement suivie du nom de la propriété MAPI, composé d'un identificateur global unique (GUID), d'un type et soit d'un identificateur, soit d'une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="430c1-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="430c1-123">Les propriétés à valeurs multiples et les propriétés à valeurs de longueur variable, telles que les types de propriété PT_BINARY, PT_STRING8, PT_UNICODE ou PT_OBJECT, sont traitées de la manière suivante.</span><span class="sxs-lookup"><span data-stu-id="430c1-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="430c1-124">Tout d'abord, le nombre de valeurs codées en tant que type de données non signées 32 bits est placé dans le flux TNEF, suivi des valeurs individuelles.</span><span class="sxs-lookup"><span data-stu-id="430c1-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="430c1-125">La valeur des données de chaque propriété est codée en octets, suivi de la valeur-Data elle-même.</span><span class="sxs-lookup"><span data-stu-id="430c1-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="430c1-126">La valeur des données est complétée par une limite de 4 octets, bien que la quantité de remplissage ne soit pas incluse dans la taille de la valeur.</span><span class="sxs-lookup"><span data-stu-id="430c1-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="430c1-127">Si la propriété est de type PT_OBJECT, la valeur de la propriété Value est suivie de l'identificateur d'interface de l'objet.</span><span class="sxs-lookup"><span data-stu-id="430c1-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="430c1-128">L'implémentation actuelle de TNEF prend en charge uniquement les identificateurs d'interface IID_IMessage, IID_IStorage et IID_Istream.</span><span class="sxs-lookup"><span data-stu-id="430c1-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="430c1-129">La taille de l'identificateur d'interface est incluse dans la valeur value-Size.</span><span class="sxs-lookup"><span data-stu-id="430c1-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="430c1-130">Si l'objet est un message incorporé (c'est-à-dire qu'il a un type de propriété PT_OBJECT et un identificateur d'interface de IID_Imessage), les données de la valeur sont codées en tant que flux TNEF incorporé.</span><span class="sxs-lookup"><span data-stu-id="430c1-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="430c1-131">Le codage réel d'un message incorporé dans l'implémentation TNEF est effectué en ouvrant un deuxième objet TNEF pour le flux d'origine et en traitant le flux inséré.</span><span class="sxs-lookup"><span data-stu-id="430c1-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

