---
title: Attribution de noms à des dossiers à l’aide de chaînes de caractères
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
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="765b7-103">Attribution de noms à des dossiers à l’aide de chaînes de caractères</span><span class="sxs-lookup"><span data-stu-id="765b7-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="765b7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="765b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="765b7-105">Si vous accédez fréquemment à un ou plusieurs dossiers au cours d’une session, envisagez d’affecter des noms aux dossiers avec la méthode [IMsgStore::SetReceiveFolder.](imsgstore-setreceivefolder.md)</span><span class="sxs-lookup"><span data-stu-id="765b7-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="765b7-106">Bien que **IMsgStore::SetReceiveFolder** soit principalement utilisé pour établir des dossiers spéciaux pour recevoir des messages entrants pour des classes de messages particulières, il peut également être utilisé pour associer n’importe quel dossier à un nom.</span><span class="sxs-lookup"><span data-stu-id="765b7-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="765b7-107">Le nom peut être identique à la classe de message ou il peut s’agit d’une chaîne de caractères, personnalisée pour l’utilisation de votre client.</span><span class="sxs-lookup"><span data-stu-id="765b7-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="765b7-108">L’association d’un nom à un dossier réduit le temps qu’il faut pour rechercher et ouvrir le dossier.</span><span class="sxs-lookup"><span data-stu-id="765b7-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

