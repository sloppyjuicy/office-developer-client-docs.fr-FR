---
title: Syntaxe de flux TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: cbaf37415608dd1d79a06be65b34632f2b4afc89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787379"
---
# <a name="tnef-stream-syntax"></a>Syntaxe de flux TNEF

  
  
**S’applique à**: Outlook 
  
Cette rubrique présente un Bakus-Nauer comme description de la syntaxe de flux TNEF. Dans cette description, les éléments non terminaux possédant une définition plus précise sont en italique. Constantes et éléments littérales sont en gras. Séquences d’éléments sont répertoriés dans l’ordre sur une seule ligne. Par exemple, l’élément de _flux de données_ se compose de la constante **TNEF_SIGNATURE**, suivi d’une _clé_, suivi d’un _objet_. Lorsqu’un élément a plus d’une implémentation possible, les alternatives figurent sur des lignes consécutives. Par exemple, un _objet_ peut se composer d’un _Message_Seq_, un _Message_Seq_ suivi d’un _Attach_Seq_ou juste un _Attach_Seq_.
  
 _TNEF_Stream :_
  
> **TNEF_SIGNATURE** _Clé_ _Objet_
    
 _Clé :_
  
> un entier non signé de 16 bits différente de zéro
    
Transports TNEF activé génèrent cette valeur avant d’utiliser la mise en œuvre TNEF pour générer un flux TNEF.
  
 _Objet :_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq :_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion :_
  
> **LVL_MESSAGE attTnefVersion sizeof** **0 x 00010000** somme de contrôle 
    
 _attMessageClass :_
  
> **LVL_MESSAGE attMessageClass** somme de contrôle _msg_class_length msg_class_ 
    
 _Msg_Attribute_Seq :_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute :_
  
> Somme de contrôle **LVL_MESSAGE** -ID de l’attribut attribut longueur données d’attribut 
    
Attribut-ID est un des identificateurs d’attribut TNEF, tel que **attSubject**. Longueur de l’attribut est la longueur, en octets, des données d’attribut. Données d’attribut sont les données associées à l’attribut.
  
 _Attach_Seq :_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata :_
  
> **LVL_ATTACHMENT attRenddata** somme de contrôle **sizeof(RENDDATA)** renddata 
    
Renddata est les données associées à la structure **RENDDATA** qui contient les informations de rendu de la pièce jointe correspondante. La structure **RENDDATA** est définie dans le format TNEF. Fichier d’en-tête H. 
  
 _Att_Attribute_Seq :_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute :_
  
> Somme de contrôle **LVL_ATTACHMENT** -ID de l’attribut attribut longueur données d’attribut 
    
ID d’attribut, longueur de l’attribut et données d’attribut ont la même signification que pour l’élément Msg_Attribute.
  

