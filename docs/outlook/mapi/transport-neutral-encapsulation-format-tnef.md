---
title: Format TNEF (Transport Neutral Encapsulation Format)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Dernière modification : 12 mars 2013'
ms.openlocfilehash: 440c27b019b91ec8c2c02e37850d2768a273559b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591932"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Format TNEF (Transport Neutral Encapsulation Format)

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le format TNEF est un format de conversion d’un jeu de propriétés MAPI — un message MAPI — dans un flux de données en série. Les fonctions TNEF sont principalement utilisées par les fournisseurs de transport qui peut-être coder les propriétés de message MAPI pour la transmission via un système de messagerie qui ne prend pas en charge ces propriétés directement. Par exemple, un type de transport basé sur SMTP utilise TNEF pour coder les propriétés comme **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), qui n’ont pas de représentations directes dans la structure d’un message SMTP.
  
L’implémentation TNEF définit plusieurs attributs spécifiques TNEF, chacun d'entre eux correspond à une propriété MAPI particulière. Ces attributs sont utilisés pour coder leurs propriétés MAPI respectifs dans le flux TNEF. En outre, un attribut spécial est défini pouvant être utilisés pour encapsuler des propriétés MAPI qui ne dispose pas d’un attribut spécifique correspondante. La raison pour laquelle ces attributs sont définis, au lieu d’utiliser simplement une méthode pour toutes les propriétés MAPI de codage d’uniforme — consiste à autoriser la compatibilité descendante avec les logiciels non compatibles MAPI à l’aide de TNEF.
  
Le reste de cette section décrit la structure et la syntaxe d’un flux TNEF, le mappage entre les propriétés MAPI et attributs TNEF et considérations importantes pour certains attributs TNEF.
  

