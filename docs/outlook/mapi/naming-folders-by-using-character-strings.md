---
title: Attribution de noms à des dossiers à l’aide de chaînes de caractères
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 23fb125218923f823593c8d40694eb1337366289
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556020"
---
# <a name="naming-folders-by-using-character-strings"></a>Attribution de noms à des dossiers à l’aide de chaînes de caractères

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si vous accédez fréquemment à un ou plusieurs dossiers au cours d’une session, envisagez d’affecter des noms aux dossiers avec la méthode [IMsgStore::SetReceiveFolder.](imsgstore-setreceivefolder.md) Bien que **IMsgStore::SetReceiveFolder** soit principalement utilisé pour établir des dossiers spéciaux pour recevoir des messages entrants pour des classes de messages particulières, il peut également être utilisé pour associer n’importe quel dossier à un nom. Le nom peut être identique à la classe de message ou il peut s’agit d’une chaîne de caractères, personnalisée pour l’utilisation de votre client. L’association d’un nom à un dossier réduit le temps qu’il faut pour rechercher et ouvrir le dossier. 
  

