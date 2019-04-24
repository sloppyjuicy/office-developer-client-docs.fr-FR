---
title: Nommer des dossiers à l'aide de chaînes de caractères
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326249"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="ac4a0-103">Nommer des dossiers à l'aide de chaînes de caractères</span><span class="sxs-lookup"><span data-stu-id="ac4a0-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="ac4a0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac4a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac4a0-105">Si vous accédez à un ou plusieurs dossiers fréquemment au cours d'une session, envisagez d'attribuer des noms aux dossiers à l'aide de la méthode [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) .</span><span class="sxs-lookup"><span data-stu-id="ac4a0-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="ac4a0-106">Bien que **IMsgStore:: SetReceiveFolder** sert principalement à établir des dossiers spéciaux pour recevoir des messages entrants pour des classes de messages spécifiques, il peut également être utilisé pour associer un dossier à un nom.</span><span class="sxs-lookup"><span data-stu-id="ac4a0-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="ac4a0-107">Le nom peut être identique à la classe de message ou peut être n'importe quelle chaîne de caractères, personnalisée pour l'utilisation de votre client.</span><span class="sxs-lookup"><span data-stu-id="ac4a0-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="ac4a0-108">L'Association d'un nom à un dossier réduit le temps nécessaire à la recherche et à l'ouverture du dossier.</span><span class="sxs-lookup"><span data-stu-id="ac4a0-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

