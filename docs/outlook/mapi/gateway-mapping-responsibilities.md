---
title: Responsabilités de la passerelle en cas de mappage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
ms.openlocfilehash: dca4a65e415a8cb502d7fed8d75d4fbc4bc0704a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380269"
---
# <a name="gateway-mapping-responsibilities"></a>Responsabilités de la passerelle en cas de mappage

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’une passerelle MAPI reçoit un message contenant des propriétés nommées dans l’un des jeux de propriétés spéciaux désignés pour contenir les propriétés mappables de la passerelle, la passerelle doit maguer toutes les propriétés au protocole du système de messagerie de destination. Bien que MAPI recommande que les passerelles gèrent toutes les propriétés nommées dans les jeux de propriétés spéciaux, les passerelles ne doivent gérer que deux : l’adresse de messagerie et le type d’adresse. Étant donné que les propriétés d’adresse de messagerie et de type d’adresse affectent directement la transmission des messages, il est essentiel que les passerelles prendre en charge le mappage de ces deux propriétés. Étant donné que les clés de recherche sont constituées du type d’adresse et de l’adresse d’un utilisateur, elles doivent également être traduites si possible.
  
Les identificateurs d’entrée ne sont pas censés être gérés fréquemment. Pour activer le mappage d’un identificateur d’entrée provenant d’un système de messagerie vers un identificateur d’entrée utilisable par un autre système de messagerie, la passerelle doit être en mesure d’utiliser le format des deux systèmes. Étant donné que la plupart des passerelles ne connaissent pas les formats d’identificateur d’entrée, la traduction des identificateurs d’entrée est rare.
  
Une autre propriété mappable qui n’est pas prévue pour être traduite fréquemment est le nom complet. Les passerelles doivent stocker les noms d’affichage et les transmettre, mais pas nécessairement les traduire. 
  

