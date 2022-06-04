---
title: Corrélation TNEF
description: Décrit comment certains systèmes de messagerie effectuent une vérification de corrélation sur un flux TNEF attaché à un message entrant à des fins de vérification.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
ms.openlocfilehash: b2907b7cd0f2b1439eead8d2ce6f3174c501bd51
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893633"
---
# <a name="tnef-correlation"></a>Corrélation TNEF

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains systèmes de messagerie effectuent une vérification de corrélation sur n’importe quel flux TNEF (Encapsulation Format) Transport-Neutral joint à un message entrant pour vérifier que le flux TNEF appartient en fait à ce message. Cela implique de faire correspondre la valeur d’un champ dans l’en-tête du message entrant avec une copie de cette valeur stockée dans une propriété dans le flux TNEF. Les valeurs probablement uniques pour chaque message, telles que les numéros d’ID de message, sont généralement utilisées pour cela. Le transport ou la passerelle qui a créé le flux TNEF est chargé de choisir une valeur appropriée dans l’en-tête de message et de placer une copie dans une propriété appropriée avant d’encoder les propriétés du message sortant dans le flux TNEF. Les passerelles ou les transports qui reçoivent le message peuvent ensuite extraire cette propriété du flux TNEF et vérifier que sa valeur correspond à la valeur du champ d’en-tête correspondant sur le message entrant.
  
Si les valeurs ne correspondent pas, la passerelle ou le transport doit ignorer le flux TNEF et traiter uniquement l’enveloppe de message native. Ces vérifications sont prudentes, car les clients de messagerie non mapi peuvent attacher un fichier qui contient un flux TNEF d’un ancien message à un transfert ou même à un message non lié; si elle n’est pas vérifiée, une telle erreur peut entraîner la perte du texte du message.
  
La valeur du champ d’en-tête choisie doit être unique au message. Il n’existe aucun champ d’en-tête fixe pour tous les systèmes de messagerie, car différents systèmes de messagerie utilisent des champs d’en-tête différents, mais généralement le système de messagerie affecte un identificateur unique au message qui convient à cet effet. Par exemple, les systèmes SMTP utilisent généralement l’en-tête MessageID, tandis que les systèmes X.400 utilisent généralement l’attribut IM_THIS_IPM.
  

