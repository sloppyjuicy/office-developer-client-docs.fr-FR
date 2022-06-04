---
title: Format TNEF (Transport Neutral Encapsulation Format)
description: Décrit TNEF, un format permettant de convertir un ensemble de propriétés MAPI (un message MAPI) en flux de données série.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
ms.openlocfilehash: 21692ac3ba96f547f1eda92a649e689680900cdb
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894641"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a>Format TNEF (Transport Neutral Encapsulation Format)

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
TNEF est un format permettant de convertir un ensemble de propriétés MAPI (un message MAPI) en flux de données série. Les fonctions TNEF sont principalement utilisées par les fournisseurs de transport qui doivent encoder les propriétés de message MAPI pour la transmission via un système de messagerie qui ne prend pas en charge ces propriétés directement. Par exemple, un transport SMTP utilise TNEF pour encoder des propriétés telles **que PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), qui n’ont pas de représentations directes dans la structure d’un message SMTP.
  
L’implémentation TNEF définit plusieurs attributs spécifiques à TNEF, chacun correspondant à une propriété MAPI particulière. Ces attributs sont utilisés pour encoder leurs propriétés MAPI respectives dans le flux TNEF. En outre, un attribut spécial est défini qui peut être utilisé pour encapsuler toute propriété MAPI qui n’a pas d’attribut spécifique qui lui correspond. La raison pour laquelle ces attributs sont définis , au lieu d’utiliser simplement une méthode d’encodage uniforme pour toutes les propriétés MAPI, est d’activer la compatibilité descendante avec les logiciels non conformes MAPI qui utilisent TNEF.
  
Le reste de cette section décrit la structure et la syntaxe d’un flux TNEF, le mappage entre les propriétés MAPI et les attributs TNEF, ainsi que des considérations importantes pour certains attributs TNEF.
  

