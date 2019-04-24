---
title: Attributs attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318066"
---
# <a name="attdate-attributes"></a>Attributs attDate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Toutes les propriétés MAPI liées aux dates et heures sont mappées aux attributs TNEF qui ont le préfixe **attDate** . Ces éléments sont tous codés sous forme de structures **DTR** . Les dates et les heures des attributs de pièce jointe sont également codées en tant que structures **DTR** . 
  
Toutes les propriétés MAPI liées aux dates et heures sont mappées aux attributs TNEF qui ont le préfixe **attDate** . Ces éléments sont tous codés sous forme de structures **DTR** . Les dates et les heures des attributs de pièce jointe sont également codées en tant que structures **DTR** . 
  
Une structure **DTR** est très semblable à la structure **SystemTime** définie dans les fichiers d'en-tête Win32. La structure **DTR** est codée dans le flux TNEF en tant qu'octets **sizeof (DTR)** en commençant par le premier membre de la structure. La structure **DTR** est définie dans le format TNEF. Fichier d'en-tête H. 
  

