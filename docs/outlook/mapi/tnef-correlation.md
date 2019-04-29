---
title: Corrélation TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: Dernière modification le 12 mars 2013
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410370"
---
# <a name="tnef-correlation"></a>Corrélation TNEF

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains systèmes de messagerie effectuent une vérification de corrélation sur tout flux TNEF (Transport-Neutral Encapsulation Format) attaché à un message entrant afin de vérifier que le flux TNEF appartient effectivement à ce message. Cela implique la correspondance de la valeur d'un champ dans l'en-tête du message entrant avec une copie de cette valeur stockée dans une propriété dans le flux TNEF. Les valeurs qui sont vraisemblablement uniques pour chaque message, telles que les numéros d'identification de message, sont généralement utilisées pour cela. Le transport ou la passerelle qui a créé le flux TNEF est responsable du choix d'une valeur appropriée dans l'en-tête du message et de l'insertion d'une copie dans une propriété appropriée avant d'encoder les propriétés du message sortant dans le flux TNEF. Les passerelles ou transports qui reçoivent le message peuvent ensuite extraire cette propriété du flux TNEF et vérifier que sa valeur correspond à la valeur du champ d'en-tête correspondant sur le message entrant.
  
Si les valeurs ne correspondent pas, la passerelle ou le transport doit rejeter le flux TNEF et traiter uniquement l'enveloppe de message native. Ces contrôles sont prudents, car les clients de messagerie non-MAPI peuvent joindre un fichier contenant un flux TNEF d'un ancien message à un message de transfert ou à un message non lié; Si cette option n'est pas cochée, une telle erreur peut entraîner la perte du texte du message.
  
La valeur du champ d'en-tête choisi doit être unique pour le message. Il n'existe pas de champ d'en-tête fixe pour tous les systèmes de messagerie, car les différents systèmes de messagerie utilisent des champs d'en-tête différents, mais le système de messagerie affecte généralement un identificateur unique au message, ce qui convient à cette fin. Par exemple, les systèmes SMTP utilisent généralement l'en-tête MessageID, tandis que les systèmes X. 400 utilisent généralement l'attribut IM_THIS_IPM.
  

