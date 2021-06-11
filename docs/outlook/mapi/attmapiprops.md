---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 185bfbb151c4f8d4e36b40b94393d14d50c33edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410454"
---
# <a name="attmapiprops"></a>attMAPIProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
**L’attribut attMAPIProps** est spécial en ce sens qu’il peut être utilisé pour encoder n’importe quelle propriété MAPI qui n’a pas d’équivalent dans l’ensemble des attributs définis par TNEF existants. Les données d’attribut sont un ensemble compté de propriétés MAPI disposés de bout en bout. Le format de ce codage, qui autorise tout ensemble de propriétés MAPI, est le suivant :  
  
 _Property_Seq :_
  
> propriété-count  _Property_Value,..._
    
Il doit y avoir autant  _d Property_Value_ que la valeur du nombre de propriétés l’indique. 
  
 _Property_Value :_
  
> property-tag _Property_property-tag  _Proptag_Name Property_
    
La balise de propriété est simplement la valeur associée à l’identificateur de propriété, telle que 0x0037001F pour **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Propriété :_
  
>  _Value-count_  _Value,..._
    
 _Valeur :_
  
> value-data value-size value-data padding value-size value-IID value-data padding
    
 _Proptag_Name :_
  
> name-guid name-kind name-id name-guid name-kind name-string-length name-string padding
    
L’encapsulation de chaque propriété varie en fonction de l’identificateur de propriété et du type de propriété. Les balises de propriété, les identificateurs et les types sont définis dans les fichiers d’en-tête Mapitags.h et Mapidefs.h.
  
Si la propriété est une propriété nommée, la balise de propriété est immédiatement suivie du nom de la propriété MAPI, constitué d’un identificateur global unique (GUID), d’un type et d’un identificateur ou d’une chaîne Unicode.
  
Les propriétés à valeurs multiples et les propriétés avec des valeurs de longueur variable, telles que les types de propriétés PT_BINARY, PT_STRING8, PT_UNICODE ou PT_OBJECT, sont traitées de la manière suivante. Tout d’abord, le nombre de valeurs, codées comme un long non signé 32 bits, est placé dans le flux TNEF, suivi des valeurs individuelles. Les données de valeur de chaque propriété sont codées en tant que taille en octets, suivies des données de valeur proprement dite. Les données de valeur sont ajoutées à une limite de 4 byte, bien que la quantité de remplissage ne soit pas incluse dans la taille de la valeur.
  
Si la propriété est de type PT_OBJECT, la taille de la valeur est suivie de l’identificateur d’interface de l’objet. L’implémentation actuelle de TNEF prend uniquement en charge les identificateurs IID_IMessage, IID_IStorage et IID_Istream’interface. La taille de l’identificateur d’interface est incluse dans la taille de la valeur.
  
Si l’objet est un message incorporé (c’est-à-dire qu’il possède un type de propriété de PT_OBJECT et un identificateur d’interface de IID_Imessage), les données de valeur sont codées en tant que flux TNEF incorporé. Le codage réel d’un message incorporé dans l’implémentation TNEF s’fait en ouvrant un deuxième objet TNEF pour le flux d’origine et en traitant le flux incorporé.
  

