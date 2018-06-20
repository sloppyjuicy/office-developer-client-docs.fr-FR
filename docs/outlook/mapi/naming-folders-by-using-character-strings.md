---
title: Noms des dossiers à l’aide de chaînes de caractères
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a6ea37bf573dab996b5a8fd7886a76fddd5b98ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784908"
---
# <a name="naming-folders-by-using-character-strings"></a>Noms des dossiers à l’aide de chaînes de caractères

  
  
**S’applique à**: Outlook 
  
Si vous accédez à un ou plusieurs dossiers fréquemment pendant une session, envisagez d’attribution de noms aux dossiers avec la méthode [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) . Bien que **IMsgStore::SetReceiveFolder** est utilisé essentiellement pour établir des dossiers spéciaux pour recevoir les messages entrants pour les classes de message particulier, il peut également servir pour associer un dossier avec un nom. Le nom peut être identique à la classe de message, ou elle peut être une chaîne de caractères, personnalisée pour l’utilisation de votre client. Association d’un nom à un dossier réduit le temps que nécessaire pour rechercher et ouvrir le dossier. 
  

