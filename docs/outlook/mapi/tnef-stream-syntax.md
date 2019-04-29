---
title: Syntaxe de flux TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423026"
---
# <a name="tnef-stream-syntax"></a>Syntaxe de flux TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique présente une bakus-Nauer comme la description de la syntaxe de flux TNEF. Dans cette description, les éléments autres que les terminaux qui ont une définition supplémentaire sont en italique. Les constantes et les éléments littéraux sont en gras. Les séquences d'éléments sont répertoriées dans l'ordre sur une seule ligne. Par exemple, l'élément de _flux_ se compose de la constante **TNEF_SIGNATURE**, suivie d'une _clé_, suivie d'un _objet_. Lorsqu'un élément a plus d'une implémentation possible, les alternatives sont répertoriées sur des lignes consécutives. Par exemple, un _objet_ peut être constitué d'un _Message_Seq_, d'un _Message_Seq_ suivi d'un _Attach_Seq_ou simplement d'un _Attach_Seq_.
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Clé_ _Objet_
    
 _Flèche_
  
> un entier non signé 16 bits différent de zéro
    
Les transports activés par TNEF génèrent cette valeur avant d'utiliser l'implémentation TNEF pour générer un flux TNEF.
  
 _Dessin_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE attTnefVersion sizeof (ULONG)** total de contrôle **0x00010000** 
    
 _attMessageClass:_
  
> **LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> Attribut de longueur d'attribut **LVL_MESSAGE** attribute-length-Data checksum 
    
Attribute-ID est l'un des identificateurs d'attribut TNEF, tels que **attSubject**. Attribute-length est la longueur en octets des données d'attribut. Attribute-Data est les données associées à l'attribut.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata** **sizeof (RENDDATA)** RENDDATA checksum 
    
Renddata est les données associées à la structure **Renddata** qui contient les informations de rendu pour la pièce jointe correspondante. La structure **RENDDATA** est définie dans le format TNEF. Fichier d'en-tête H. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> Attribut de longueur d'attribut **LVL_ATTACHMENT** attribute-length-Data checksum 
    
Attribute-ID, attribute-Length et attribute-Data ont les mêmes significations que pour l'élément Msg_Attribute.
  

