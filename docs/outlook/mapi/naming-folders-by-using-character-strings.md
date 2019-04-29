---
title: Nommer des dossiers à l'aide de chaînes de caractères
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428311"
---
# <a name="naming-folders-by-using-character-strings"></a>Nommer des dossiers à l'aide de chaînes de caractères

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si vous accédez à un ou plusieurs dossiers fréquemment au cours d'une session, envisagez d'attribuer des noms aux dossiers à l'aide de la méthode [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) . Bien que **IMsgStore:: SetReceiveFolder** sert principalement à établir des dossiers spéciaux pour recevoir des messages entrants pour des classes de messages spécifiques, il peut également être utilisé pour associer un dossier à un nom. Le nom peut être identique à la classe de message ou peut être n'importe quelle chaîne de caractères, personnalisée pour l'utilisation de votre client. L'Association d'un nom à un dossier réduit le temps nécessaire à la recherche et à l'ouverture du dossier. 
  

