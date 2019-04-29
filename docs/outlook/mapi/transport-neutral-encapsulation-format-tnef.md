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
  
Le format TNEF est un format permettant de convertir un ensemble de propriétés MAPI (un message MAPI) en un flux de données série. Les fonctions TNEF sont principalement utilisées par les fournisseurs de transport qui doivent coder les propriétés de message MAPI pour la transmission via un système de messagerie qui ne prend pas directement en charge ces propriétés. Par exemple, un transport SMTP utilise le format TNEF pour coder les propriétés comme **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), qui n'ont pas de représentation directe dans la structure d'un message SMTP.
  
L'implémentation TNEF définit plusieurs attributs spécifiques au format TNEF, chacun correspondant à une propriété MAPI particulière. Ces attributs sont utilisés pour encoder leurs propriétés MAPI respectives dans le flux TNEF. De plus, un attribut spécial est défini qui peut être utilisé pour encapsuler une propriété MAPI qui n'a pas d'attribut spécifique correspondant. La raison pour laquelle ces attributs sont définis, au lieu d'utiliser simplement une méthode de codage uniforme pour toutes les propriétés MAPI, est d'activer la compatibilité descendante avec un logiciel non conforme à la norme MAPI qui utilise le format TNEF.
  
Le reste de cette section décrit la structure et la syntaxe d'un flux TNEF, le mappage entre les propriétés MAPI et les attributs TNEF, ainsi que des considérations importantes pour certains attributs TNEF.
  

