---
title: Affectation de noms aux dossiers avec des chaînes de caractères
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 93d959bf41b5d18610d77c6b5573895b0e3880d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594585"
---
# <a name="naming-folders-by-using-character-strings"></a>Affectation de noms aux dossiers avec des chaînes de caractères

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Si vous accédez à un ou plusieurs dossiers fréquemment pendant une session, envisagez d’attribution de noms aux dossiers avec la méthode [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) . Bien que **IMsgStore::SetReceiveFolder** est utilisé essentiellement pour établir des dossiers spéciaux pour recevoir les messages entrants pour les classes de message particulier, il peut également servir pour associer un dossier avec un nom. Le nom peut être identique à la classe de message, ou elle peut être une chaîne de caractères, personnalisée pour l’utilisation de votre client. Association d’un nom à un dossier réduit le temps que nécessaire pour rechercher et ouvrir le dossier. 
  

