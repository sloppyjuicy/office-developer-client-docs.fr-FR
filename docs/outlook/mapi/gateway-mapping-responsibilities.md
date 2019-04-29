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
  
Lorsqu'une passerelle compatible MAPI reçoit un message contenant des propriétés nommées dans l'un des jeux de propriétés spécifiques désignés pour contenir des propriétés mappées sur la passerelle, la passerelle doit mapper toutes les propriétés au protocole du système de messagerie de destination. Bien que MAPI recommande que les passerelles gèrent toutes les propriétés nommées dans les jeux de propriétés spéciales, les passerelles sont censées gérer uniquement deux: adresse de messagerie et type d'adresse. Étant donné que les propriétés d'adresse de messagerie et de type d'adresse affectent directement la transmission des messages, il est essentiel que les passerelles prennent en charge le mappage de ces deux propriétés. Étant donné que les clés de recherche se composent du type d'adresse et de l'adresse d'un utilisateur, elles doivent également être traduites dans la mesure du possible.
  
Les identificateurs d'entrée ne sont pas censés être gérés fréquemment. Pour activer le mappage d'un identificateur d'entrée provenant d'un système de messagerie à un identificateur d'entrée utilisable par un autre système de messagerie, la passerelle doit être en mesure d'utiliser le format des deux systèmes. Étant donné que la plupart des passerelles ne prennent pas en charge les formats d'identificateur d'entrée, la traduction des identificateurs d'entrée est rare.
  
Le nom complet est une autre propriété mappable qui n'est pas censée être traduite fréquemment. Les passerelles doivent stocker les noms d'affichage et les transmettre, mais pas nécessairement les traduire. 
  

