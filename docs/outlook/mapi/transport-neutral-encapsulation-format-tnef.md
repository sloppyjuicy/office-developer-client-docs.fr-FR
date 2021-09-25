---
title: Format TNEF (Transport Neutral Encapsulation Format)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: Dernière modification le 12 mars 2013
ms.openlocfilehash: 22ba19f374421656317196080e6a22153700f851
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590907"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Format TNEF (Transport Neutral Encapsulation Format)

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le format TNEF est un format de conversion d’un ensemble de propriétés MAPI (message MAPI) en un flux de données série. Les fonctions TNEF sont principalement utilisées par les fournisseurs de transport qui doivent encoder les propriétés de message MAPI pour la transmission via un système de messagerie qui ne prend pas en charge ces propriétés directement. Par exemple, un transport SMTP utilise le TNEF pour coder des propriétés telles que **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), qui n’ont pas de représentations directes dans la structure d’un message SMTP.
  
L’implémentation TNEF définit plusieurs attributs spécifiques au TNEF, chacun correspondant à une propriété MAPI particulière. Ces attributs sont utilisés pour coder leurs propriétés MAPI respectives dans le flux TNEF. En outre, un attribut spécial est défini et peut être utilisé pour encapsuler toute propriété MAPI qui n’a pas d’attribut spécifique correspondant à celle-ci. La raison pour laquelle ces attributs sont définis, au lieu d’utiliser simplement une méthode d’encodage uniforme pour toutes les propriétés MAPI, est de permettre la compatibilité ascendante avec les logiciels non conformes MAPI qui utilisent le TNEF.
  
Le reste de cette section décrit la structure et la syntaxe d’un flux TNEF, le mappage entre les propriétés MAPI et les attributs TNEF, ainsi que les considérations importantes pour certains attributs TNEF.
  

