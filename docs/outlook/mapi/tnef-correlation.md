---
title: Corrélation TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Dernière modification : 12 mars 2013'
ms.openlocfilehash: 5b5af5cee7c58eb300e4020c763431fd96bdd295
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563760"
---
# <a name="tnef-correlation"></a>Corrélation TNEF

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Certains systèmes de messagerie effectuent une vérification de corrélation sur n’importe quel flux de Transport-Neutral Encapsulation Format (TNEF) joint à un message entrant pour vérifier que le flux TNEF appartient à ce message. Cela implique correspondant à la valeur d’un champ dans l’en-tête du message entrant avec une copie de cette valeur stockée dans une propriété dans le flux TNEF. Les valeurs qui sont probablement uniques pour chaque message, tels que les numéros d’identification de message, sont généralement utilisés pour ce. Le transport ou la passerelle qui a créé le flux TNEF est chargé de choisir une valeur appropriée à partir de l’en-tête du message et placer une copie dans une propriété appropriée avant le codage des propriétés du message sortant dans le flux TNEF. Passerelles ou des transports qui reçoivent le message peuvent ensuite extraire cette propriété à partir du flux TNEF et vérifiez que sa valeur correspond à la valeur du champ d’en-tête du message entrant correspondant.
  
Si les valeurs ne correspondent pas, la passerelle ou le transport doit ignorer le processus uniquement l’enveloppe du message native et les flux TNEF. Ces contrôles sont prudents, car les clients de messagerie non basé sur MAPI peuvent joindre un fichier qui contient un flux TNEF à partir d’un message ancien pour un transfert ou même un message indépendant ; s’il est ne pas activé, cette erreur risque d’entraîner la perte de texte du message.
  
La valeur du champ en-tête choisie doit être unique au message. Il n’existe aucun champ d’en-tête fixe pour tous les systèmes de messagerie, car les différents systèmes de messagerie utilisent des champs d’en-tête différents, mais généralement le système de messagerie assigne un identificateur unique pour le message qui convient à cette fin. Par exemple, systèmes SMTP utilisent généralement l’en-tête MessageID, tandis que les systèmes X.400 utilisent généralement l’attribut IM_THIS_IPM.
  

