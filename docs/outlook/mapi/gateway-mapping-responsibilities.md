---
title: Responsabilités de la passerelle en cas de mappage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 214d24bb0b0af525d5e2588c556c37cf720364a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422753"
---
# <a name="gateway-mapping-responsibilities"></a>Responsabilités de la passerelle en cas de mappage

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’une passerelle sensible à MAPI reçoit un message contenant des propriétés nommées dans l’un des jeux de propriétés spéciaux désignés pour contenir des propriétés mappables de passerelle, la passerelle doit maguer toutes les propriétés au protocole du système de messagerie de destination. Bien que MAPI recommande que les passerelles gèrent toutes les propriétés nommées dans les jeux de propriétés spéciaux, les passerelles ne doivent en gérer que deux : l’adresse de messagerie et le type d’adresse. Étant donné que les propriétés d’adresse de messagerie et de type d’adresse affectent directement la transmission des messages, il est essentiel que les passerelles prendre en charge le mappage de ces deux propriétés. Étant donné que les clés de recherche sont constituées du type d’adresse et de l’adresse d’un utilisateur, elles doivent également être traduites si possible.
  
Les identificateurs d’entrée ne sont pas censés être gérés fréquemment. Pour activer le mappage d’un identificateur d’entrée provenant d’un système de messagerie vers un identificateur d’entrée utilisable par un autre système de messagerie, la passerelle doit être en mesure d’utiliser le format des deux systèmes. Étant donné que la plupart des passerelles ne connaissent pas les formats d’identificateur d’entrée, la traduction des identificateurs d’entrée est rare.
  
Une autre propriété mappable qui n’est pas prévue pour être traduite fréquemment est le nom complet. Les passerelles doivent stocker les noms d’affichage et les transmettre, mais pas nécessairement les traduire. 
  

