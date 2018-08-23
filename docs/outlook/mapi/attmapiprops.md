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
ms.openlocfilehash: 72f252791e374ed4b9b2a40c9b151ef2b91fefe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588054"
---
# <a name="attmapiprops"></a>attMAPIProps

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
L’attribut **attMAPIProps** est spécial en ce sens qu’il peut être utilisé pour encoder des propriétés MAPI qui n’ont pas un équivalent dans l’ensemble des attributs définis par le format TNEF existants. Les données d’attribut sont un ensemble de propriétés MAPI définies de bout en bout compté. Le format de codage, qui permet à n’importe quel jeu de propriétés MAPI, est comme suit :  
  
 _Property_Seq :_
  
> compte de la propriété _nom..._
    
Il doit exister autant d’éléments _nom_ comme l’indique la valeur de nombre de propriétés. 
  
 _Nom :_
  
> balise de propriété _Property_property-balise _Propriété Proptag_Name_
    
La balise de propriété est simplement la valeur associée à l’identificateur de la propriété, tel que 0x0037001F pour **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Propriété :_
  
>  _Valeur_ -nombre de valeurs _valeur..._
    
 _Valeur :_
  
> valeur-taille de la valeur valeur données-remplissage du remplissage de données de la valeur taille de la valeur valeur-IID
    
 _Proptag_Name :_
  
> remplissage de chaîne de nom guid-nom nom-id de type-nom nom-guid Nom-type longueur de chaîne de nom
    
L’encapsulation de chaque propriété varie en fonction de l’identificateur de propriété et le type de propriété. Types, les identificateurs et les balises de propriété sont définies dans les fichiers d’en-tête Mapitags.h et Mapidefs.h.
  
Si la propriété est une propriété nommée, la balise de propriété est immédiatement suivie par le nom de la propriété MAPI, constitué d’un identificateur global unique (GUID), un type et un identificateur ou une chaîne Unicode.
  
Propriétés à valeurs multiples et des propriétés avec les valeurs de longueur variable, telles que les types de propriété PT_BINARY, PT_STRING8, PT_UNICODE ou PT_OBJECT, sont traitées de la manière suivante. Tout d’abord le nombre de valeurs, codées en tant que 32 bits long, non signée est placé dans le flux TNEF, suivi par les valeurs individuelles. Données de valeur de chaque propriété sont codée en tant que sa taille en octets, suivi par les données de valeur proprement dite. Données de la valeur sont remplie avec une limite de 4 octets, bien que la taille de la marge n’est pas inclus dans la taille de la valeur.
  
Si la propriété est de type PT_OBJECT, la taille de la valeur est suivie de l’identificateur d’interface de l’objet. L’implémentation actuelle du format TNEF prend uniquement en charge les identificateurs d’interface IID_Istream, IID_IStorage et IID_IMessage. La taille de l’identificateur d’interface est incluse dans la taille de la valeur.
  
Si l’objet est un message incorporé (autrement dit, elle possède un type de propriété de PT_OBJECT et un identificateur d’interface de IID_Imessage), la valeur des données sont codées en tant qu’un flux TNEF intégré. Le codage d’un message incorporé dans implémentation TNEF est effectué en ouvrant un deuxième objet TNEF pour le flux d’origine et de traitement inline flux.
  

