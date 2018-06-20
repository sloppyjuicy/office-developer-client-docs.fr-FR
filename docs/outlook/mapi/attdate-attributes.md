---
title: Attributs attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f3319c9ae49fa97a6179b0ee800bd5dd594aefab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782956"
---
# <a name="attdate-attributes"></a>Attributs attDate

  
  
**S’applique à**: Outlook 
  
Toutes les propriétés MAPI relatives aux dates et heures sont mappées aux attributs TNEF qui ont le préfixe **attDate** . Tous ces sont codées en tant que structures **DTR** . Les dates et heures pour les attributs des pièces jointes sont codées en tant que structures **DTR** également. 
  
Toutes les propriétés MAPI relatives aux dates et heures sont mappées aux attributs TNEF qui ont le préfixe **attDate** . Tous ces sont codées en tant que structures **DTR** . Les dates et heures pour les attributs des pièces jointes sont codées en tant que structures **DTR** également. 
  
Une structure **DTR** est très similaire à la structure **SYSTEMTIME** définie dans les fichiers d’en-tête Win32. La structure **DTR** est codée dans le flux TNEF en octets **sizeof(DTR)** commençant par le premier membre de la structure. La structure **DTR** est définie dans le format TNEF. Fichier d’en-tête H. 
  

