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
  
L'attribut **attMAPIProps** est spécial dans la mesure où il peut être utilisé pour coder n'importe quelle propriété MAPI qui n'a pas de contrepartie dans le jeu d'attributs définis par le format TNEF existant. Les données d'attribut sont un ensemble compté de propriétés MAPI, de bout en bout. Le format de ce codage, qui permet d'utiliser n'importe quel ensemble de propriétés MAPI, est le suivant:  
  
 _Property_Seq:_
  
> propriété-Count _Property_Value,..._
    
Il doit y avoir autant d'éléments _Property_Value_ que la valeur du nombre de propriétés. 
  
 _Property_Value:_
  
> propriété-Tag _Property_property _propriété Proptag_Name_
    
La balise property est simplement la valeur associée à l'identificateur de la propriété, telle que 0x0037001F pour **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Inspecteur_
  
>  __ Valeur de la valeur-nombre _,..._
    
 _Valeur :_
  
> value-Data value-Size value-Data Padding value-Size value-IID value-Data Padding
    
 _Proptag_Name:_
  
> name-GUID nom-type nom-ID nom-GUID nom-type nom-chaîne-longueur nom-chaîne remplissage de la chaîne
    
L'encapsulation de chaque propriété varie en fonction de l'identificateur de propriété et du type de propriété. Les balises, identificateurs et types de propriété sont définis dans les fichiers d'en-tête Mapitags. h et Mapidefs. h.
  
Si la propriété est une propriété nommée, la balise de la propriété est immédiatement suivie du nom de la propriété MAPI, composé d'un identificateur global unique (GUID), d'un type et soit d'un identificateur, soit d'une chaîne Unicode.
  
Les propriétés à valeurs multiples et les propriétés à valeurs de longueur variable, telles que les types de propriété PT_BINARY, PT_STRING8, PT_UNICODE ou PT_OBJECT, sont traitées de la manière suivante. Tout d'abord, le nombre de valeurs codées en tant que type de données non signées 32 bits est placé dans le flux TNEF, suivi des valeurs individuelles. La valeur des données de chaque propriété est codée en octets, suivi de la valeur-Data elle-même. La valeur des données est complétée par une limite de 4 octets, bien que la quantité de remplissage ne soit pas incluse dans la taille de la valeur.
  
Si la propriété est de type PT_OBJECT, la valeur de la propriété Value est suivie de l'identificateur d'interface de l'objet. L'implémentation actuelle de TNEF prend en charge uniquement les identificateurs d'interface IID_IMessage, IID_IStorage et IID_Istream. La taille de l'identificateur d'interface est incluse dans la valeur value-Size.
  
Si l'objet est un message incorporé (c'est-à-dire qu'il a un type de propriété PT_OBJECT et un identificateur d'interface de IID_Imessage), les données de la valeur sont codées en tant que flux TNEF incorporé. Le codage réel d'un message incorporé dans l'implémentation TNEF est effectué en ouvrant un deuxième objet TNEF pour le flux d'origine et en traitant le flux inséré.
  

