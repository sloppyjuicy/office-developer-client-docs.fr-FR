---
title: Attributs attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
ms.openlocfilehash: 8af383ae4427b4d0af83b731d93e6a2a35b746aa
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377287"
---
# <a name="attdate-attributes"></a>Attributs attDate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Toutes les propriétés MAPI relatives aux dates et heures sont mappées aux attributs TNEF qui ont le **préfixe attDate** . Toutes ces structures sont codées en tant que structures **DTR** . Les dates et heures des attributs de pièce jointe sont également codées en tant que structures **DTR** . 
  
Toutes les propriétés MAPI relatives aux dates et heures sont mappées aux attributs TNEF qui ont le **préfixe attDate** . Toutes ces structures sont codées en tant que structures **DTR** . Les dates et heures des attributs de pièce jointe sont également codées en tant que structures **DTR** . 
  
Une structure **DTR** est très similaire à la structure **SYSTEMTIME** définie dans les fichiers d’en-tête Win32. La structure **DTR** est codée dans le flux TNEF en tant qu’octets **sizeof(DTR)** en commençant par le premier membre de la structure. La structure **DTR** est définie dans le TNEF. Fichier d’en-tête H. 
  

