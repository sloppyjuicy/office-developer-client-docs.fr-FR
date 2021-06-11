---
title: Format TNEF (Transport Neutral Encapsulation Format)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: Dernière modification le 12 mars 2013
ms.openlocfilehash: d902039fa1081e30947ddd8f70ead9ae7acec06a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428689"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Format TNEF (Transport Neutral Encapsulation Format)

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le format TNEF est un format de conversion d’un ensemble de propriétés MAPI (message MAPI) en un flux de données série. Les fonctions TNEF sont principalement utilisées par les fournisseurs de transport qui doivent encoder les propriétés de message MAPI pour la transmission via un système de messagerie qui ne prend pas en charge ces propriétés directement. Par exemple, un transport SMTP utilise le TNEF pour coder des propriétés telles que **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), qui n’ont pas de représentations directes dans la structure d’un message SMTP.
  
L’implémentation TNEF définit plusieurs attributs spécifiques au TNEF, chacun correspondant à une propriété MAPI particulière. Ces attributs sont utilisés pour coder leurs propriétés MAPI respectives dans le flux TNEF. En outre, un attribut spécial est défini et peut être utilisé pour encapsuler toute propriété MAPI qui n’a pas d’attribut spécifique correspondant à celle-ci. La raison pour laquelle ces attributs sont définis, au lieu d’utiliser simplement une méthode d’encodage uniforme pour toutes les propriétés MAPI, est de permettre la compatibilité ascendante avec les logiciels non conformes MAPI qui utilisent le TNEF.
  
Le reste de cette section décrit la structure et la syntaxe d’un flux TNEF, le mappage entre les propriétés MAPI et les attributs TNEF, ainsi que les considérations importantes pour certains attributs TNEF.
  

