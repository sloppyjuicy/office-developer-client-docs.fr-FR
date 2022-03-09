---
title: Attribution de noms à des dossiers à l’aide de chaînes de caractères
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
ms.openlocfilehash: af83d6cfaa293c08a7d59fb9b9d5fe23d7ff7492
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379373"
---
# <a name="naming-folders-by-using-character-strings"></a>Attribution de noms à des dossiers à l’aide de chaînes de caractères

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si vous accédez fréquemment à un ou plusieurs dossiers au cours d’une session, envisagez d’affecter des noms aux dossiers avec la méthode [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) . Bien que **IMsgStore::SetReceiveFolder** soit principalement utilisé pour établir des dossiers spéciaux pour recevoir des messages entrants pour des classes de messages particulières, il peut également être utilisé pour associer n’importe quel dossier à un nom. Le nom peut être identique à la classe de message ou il peut s’agit d’une chaîne de caractères, personnalisée pour l’utilisation de votre client. L’association d’un nom à un dossier réduit le temps qu’il faut pour rechercher et ouvrir le dossier. 
  

