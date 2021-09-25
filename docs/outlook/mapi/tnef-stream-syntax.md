---
title: Syntaxe de flux TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 841404f5f7cb13fadd964f13174dc25c493e0015
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609326"
---
# <a name="tnef-stream-syntax"></a>Syntaxe de flux TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique présente une description Bakus-Nauer de la syntaxe de flux TNEF. Dans cette description, les éléments nonterminaux qui ont une définition supplémentaire sont en italique. Les constantes et les éléments littéraux sont en gras. Les séquences d’éléments sont répertoriées dans l’ordre sur une seule ligne. Par exemple, _l’élément Stream_ se compose de la **constante TNEF_SIGNATURE**, suivie d’une clé , suivie d’un  _objet_. Lorsqu’un élément possède plusieurs implémentations possibles, les alternatives sont répertoriées sur des lignes consécutives. Par exemple, un _objet_ peut se composer  _d’un Message_Seq,_ d’un Message_Seq suivi d’un _Attach_Seq_ ou simplement d’un _Attach_Seq_.
  
 _TNEF_Stream :_
  
> **TNEF_SIGNATURE** _Key,_ _objet_
    
 _Clé :_
  
> un integer non signé 16 bits non zéro
    
Les transports TNEF activés génèrent cette valeur avant d’utiliser l’implémentation TNEF pour générer un flux TNEF.
  
 _Objet :_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq :_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion :_
  
> **LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum 
    
 _attMessageClass :_
  
> **LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum 
    
 _Msg_Attribute_Seq :_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute :_
  
> **LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum 
    
Attribute-ID est l’un des identificateurs d’attributS TNEF, tels **que attSubject**. La longueur d’attribut est la longueur en octets des données d’attribut. Les données d’attribut sont les données associées à l’attribut.
  
 _Attach_Seq :_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata :_
  
> **LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum 
    
Renddata est les données associées à la structure **RENDDATA** qui contient les informations de rendu pour la pièce jointe correspondante. La structure **RENDDATA** est définie dans le format TNEF. Fichier d’en-tête H. 
  
 _Att_Attribute_Seq :_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute :_
  
>  LVL_ATTACHMENT’attribut-ID attribut-length attribute-data checksum 
    
L’ID d’attribut, la longueur d’attribut et les données d’attribut ont les mêmes significations que pour l’Msg_Attribute’élément.
  

