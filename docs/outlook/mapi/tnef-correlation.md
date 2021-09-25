---
title: Corrélation TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: Dernière modification le 12 mars 2013
ms.openlocfilehash: 6f7c9403990a7950bb2e2c88528477e5a9b90501
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590906"
---
# <a name="tnef-correlation"></a>Corrélation TNEF

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains systèmes de messagerie effectuent une vérification de corrélation sur n’importe quel flux TNEF (Transport-Neutral Encapsulation Format) joint à un message entrant pour vérifier que le flux TNEF appartient bien à ce message. Cela implique de faire correspondre la valeur d’un champ dans l’en-tête du message entrant avec une copie de cette valeur stockée dans une propriété dans le flux TNEF. Les valeurs qui sont probablement uniques pour chaque message, telles que les numéros d’ID de message, sont généralement utilisées pour cela. Le transport ou la passerelle qui a créé le flux TNEF est chargé de choisir une valeur appropriée dans l’en-tête du message et de placer une copie dans une propriété appropriée avant de coder les propriétés du message sortant dans le flux TNEF. Les passerelles ou les transports qui reçoivent le message peuvent ensuite extraire cette propriété du flux TNEF et vérifier que sa valeur correspond à la valeur du champ d’en-tête correspondant sur le message entrant.
  
Si les valeurs ne correspondent pas, la passerelle ou le transport doit ignorer le flux TNEF et traiter uniquement l’enveloppe de message native. Ces vérifications sont prudents, car les clients de messagerie non MAPI peuvent joindre un fichier qui contient un flux TNEF d’un ancien message à un envoi, voire à un message non lié ; Si elle n’est pas vérifiée, une telle erreur peut entraîner la perte de texte du message.
  
La valeur de champ d’en-tête choisie doit être propre au message. Il n’existe pas de champ d’en-tête fixe pour tous les systèmes de messagerie, car différents systèmes de messagerie utilisent des champs d’en-tête différents, mais généralement le système de messagerie affecte un identificateur unique au message, ce qui convient à cet effet. Par exemple, les systèmes SMTP utilisent généralement l’en-tête MessageID, tandis que les systèmes X.400 utilisent généralement l IM_THIS_IPM de message.
  

