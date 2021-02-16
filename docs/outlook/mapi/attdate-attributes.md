---
title: Attributs attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408277"
---
# <a name="attdate-attributes"></a>Attributs attDate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Toutes les propriétés MAPI relatives aux dates et heures sont mappées aux attributs TNEF qui ont le **préfixe attDate.** Toutes ces structures sont codées en tant que structures **DTR.** Les dates et heures des attributs de pièce jointe sont également codées en tant que structures **DTR.** 
  
Toutes les propriétés MAPI relatives aux dates et heures sont mappées aux attributs TNEF qui ont le **préfixe attDate.** Toutes ces structures sont codées en tant que structures **DTR.** Les dates et heures des attributs de pièce jointe sont également codées en tant que structures **DTR.** 
  
Une structure **DTR** est très similaire à la structure **SYSTEMTIME** définie dans les fichiers d’en-tête Win32. La structure **DTR** est codée dans le flux TNEF en tant qu’octets **sizeof(DTR)** en commençant par le premier membre de la structure. La structure **DTR** est définie dans le TNEF. Fichier d’en-tête H. 
  

